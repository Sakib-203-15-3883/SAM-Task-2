# Creating a Watch Face Using Tag Expressions

In this session, we are going to learn how to create a watch face using Tag Expressions. That means today we are going to create a watch face for smartwatches that run on the Wear OS operating system. 

## Prerequisites

Before we start, we need to understand some concepts:

1. **Watch Face Studio**  
   Watch Face Studio is a development tool where we can build a watch face without any code. However, we can use tag expressions to apply common logic to dynamically change the UI and state of the watch face.

2. **Smartwatch Modes**  
   There are two types of modes in a smartwatch:
   - **Always-On Mode**: This mode is visible all the time, so we will minimize and remove extra elements from the watch face to ensure battery efficiency.
   - **Normal Mode**: In this mode, we will implement more features and visual elements compared to Always-On Mode.

## What We Are Building

Today, we are going to create an **analog watch face** that includes:
- **Index components**
- **Analog hand components**

Additionally, we will implement a feature where the **battery level icon color changes to red** when the charge level is less than or equal to 20%. This logic will be implemented using the `BATT_PER` tag, which will be explained later in this documentation.

## Demonstration

Below, I will demonstrate the result of the watch face in different modes that we will create in today’s session for better visibility.

normal mode and greater than 20% charge

![normal mode and greater than 20% charge](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/result/Normal_Mode%20%26%26%20%20enough_charge.png)

normal mode and less than 20% charge

![normal mode and less than 20% charge](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/result/normal_mode%20%26%26%20less_charge.png)

always on mode mode and greater than 20% charge

![always on mode mode and greater than 20% charge](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/result/always_on_mode%20%26%26%20enough_charge.png)

always on mode mode and less than 20% charge

![always on mode mode and less than 20% charge](https://github.com/Sakib-203-15-3883/SAM-Task-2/blob/main/result/always_on_mode%20%26%26%20less_charge%20.png)


