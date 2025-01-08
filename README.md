# fyp-report
Report for my Final Year Project: `fyp`

## Project Description from Portal
Summary: You will study how robots can learn end-to-end control policies, whilst optimising the movement of the camera during execution of a task.

### Motivation

Imitation learning and reinforcement learning are the two most popular ways for robots to learn new tasks, such as interacting with objects using their hands. Here, robots usually have cameras mounted to their heads (e.g. in this project) or to their wrists (e.g. in this project), and sometimes both (e.g. in this project). A neural network is then trained to predict the optimal action given the image the robot observes. However, these cameras are usually rigidly mounted to the robot, whereas with humans, we are are continually moving our eyes (and our heads) in order to actively observe the world and gain the optimal viewpoint for a particular task. For example, if we are searching for an object inside a drawer, we will move our heads above the drawer to observe it from above, or if we are threading a needle, we will move our heads close to the needle to enable fine-grained visuomotor control of our hands. In this project, you will study if we can give robots this same ability.

### Your Research

There are several ideas I have for how we could approach this problem. So to begin with, we will have a deeper think about each one, formulate each mathematically (e.g. think about the underlying Markov Decision Process), and do some preliminary simulation experiments with some very simple tasks. After this, we can choose the most promising idea and develop this further. These three ideas are:

1. The robot learns a policy as normal (e.g. using imitation learning from human demonstrations). Then during policy execution, the robot uses 3D reasoning and forward planning, in order to predict its optimal pose such that the object of interest is clearly visible, and not occluded by other objects.
2. The robot randomly moves its camera around during policy learning (e.g. during the demonstrations provided by the human), in order to generate a range of different camera viewpoints (for the same robot state). When the policy is deployed, the uncertainty of the policy (e.g. using an ensemble method) can be used to guide the camera towards regions with low uncertainty.
3. In simulation, reinforcement learning is used to train a policy that directly controls the camera, for any given task and object, using randomly generated "pseudo-tasks". Then after training a robot on a task using human demonstrations in the real world, two policies will be deployed: the main policy controlling the robot's hand, and the policy controlling the robot's camera.


### Milestones

I am happy for the project to adapt as you progress, according to your own interests and my guidance. But for now, a tentative set of milestones is as follows:

1. Read and understand the recent papers in the field which study image-based imitation learning and reinforcement learning, as well as any papers you can find which study active vision for these.
2. Formulate the mathematical foundations of the three ideas proposed above.
3. Learn how to use a basic robot simulator (e.g. PyBullet).
4. Implement basic versions of the three ideas in simulation, for some toy 2D tasks.
5. Choose the most promising idea, and develop it further with some more realistic 3D tasks, but still in simulation.
6. (Optional) Evaluate the method you have developed on real-world everyday tasks in my lab, using one of our robots.


## Interim Report Structure

1. **Introduction:** (1-3 pages) It’s a good idea to try to write the introduction to your final report early on in the project. However, you will find it hard, as you won’t yet have a complete story and you won’t know what your main contributions are going to be. However, the exercise is useful as it will tell you what you don’t yet know and thus what questions your project should aim to answer. For the interim report this section should be a short, succinct, summary of the project’s main objectives. Some of this material may be re-usable in your final report, but the chances are that your final introduction will be quite different.  You are therefore advised to keep this part of the interim report short, focusing on the following questions: What is the problem, why is it interesting and what’s your main idea for solving it?  (DON'T use those three questions as subheadings however!  The answers should emerge from what you write.)

1. **Background:** (10-20 pages) This should form the bulk of the interim report. You should consider that your objective here is to produce a near final version of the background section, as it will appear in your final report.  All of this material should be re-usable, so it is worth getting it right at this stage of the project.  The details of what to include can be found in the Project Report guidelines.

1. **Project Plan:** (1-2 pages). You should explain what needs to be done in order to complete the project and roughly what you expect the timetable to be. Don’t forget to include the project write-up (the final report), as this is a major part of the exercise. It’s important to identify key milestones and also fall-back positions, in case you run out of time.  You should also identify what extensions could be added if time permits.  The plan should be complete and should include those parts that you have already addressed (make it clear how far you have progressed at the time of writing).  This material will not appear in the final report.

1. **Evaluation plan:** (1-2 pages). Project evaluation is very important, so it's important to think now about how you plan to measure success. For example, what functionality do you need to demonstrate?  What experiments to you need to undertake and what outcome(s) would constitute success?  What benchmarks should you use? How has your project extended the state of the art?  How do you measure qualitative aspects, such as ease of use?  These are the sort of questions that your project evaluation should address; this section should outline your plan.

1. **Ethical issues:** (where necessary - 1-2 pages). Are there wider ethical, legal, professional and societal issues surrounding your project and the accompanying research? If there are, please discuss these. You should use the ethics checklist as the basis for this discussion. 

1. **Bibliography/References.** DoC uses the Vancouver Referencing Format.