<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Sowmiya p</h3>
<h3>Register Number: 212225240152</h3>
<h3>Date: 15/10/2026</h3>

<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Medicine prescribing agent:</h3>
<p>Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.</p>
<hr>
<h3>PEAS DESCRIPTION:</h3>
<table>
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
     <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
    <tr>
    <td><strong>Medicine prescribing agent</strong></td>
    <td><strong>Treating unhealthy, agent movement</strong></td>
     <td><strong>Rooms, Patient</strong></td>
    <td><strong>Medicine, Treatment</strong></td>
    <td><strong>Location, Temperature of patient</strong></td>
  </tr>
</table>
<hr>
<H3>DESIGN STEPS</H3>
<h3>STEP 1:Identifying the input:</h3>
<p>Temperature from patients, Location.</p>
<h3>STEP 2:Identifying the output:</h3>
<p>Prescribe medicine if the patient in a random has a fever.</p>
<h3>STEP 3:Developing the PEAS description:</h3>
<p>PEAS description is developed by the performance, environment, actuators, and sensors in an agent.</p>
<h3>STEP 4:Implementing the AI agent:</h3>
<p>Treat unhealthy patients in each room. And check for the unhealthy patients in random room</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented</p>

## Programm

```
class MedicineAgent:
    def __init__(self):
        self.performance = 0
        self.current_room = 1

    def check_patient(self, room, temperature):
        print("\nChecking Room", room)
        print("Patient Temperature:", temperature, "F")

        if temperature > 98.5:
            print("Patient has fever.")
            print("Medicine prescribed and treatment given.")
            self.performance += 10
        else:
            print("Patient is healthy. No medicine needed.")

    def move_to_room(self, room):
        if self.current_room != room:
            print("\nMoving from Room", self.current_room,
                  "to Room", room)
            self.performance -= 1
            self.current_room = room

    def run(self):
        print("Medicine Prescribing Agent")

        # Patient temperatures in two rooms
        room1_temp = float(input("Enter Room 1 patient temperature: "))
        room2_temp = float(input("Enter Room 2 patient temperature: "))

        # Check Room 1
        self.check_patient(1, room1_temp)

        # Move to Room 2
        self.move_to_room(2)
        self.check_patient(2, room2_temp)

        print("\nFinal Performance Score:", self.performance)


# Create and run the AI agent
agent = MedicineAgent()
agent.run()
```
## Output:
<img width="437" height="350" alt="Screenshot 2026-10-26 084914" src="https://github.com/user-attachments/assets/1ffed6da-b32b-457d-bd55-8d827cf9d721" />

