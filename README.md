# Revit Wall & Floor Layer Separation

A Revit add-in developed in C# to automate the separation of compound Walls and Floors into individual layer elements, supporting BIM workflows that require more detailed element modeling.

Designed primarily for **Autodesk Revit 2021**, the tool processes elements level by level, creates individual elements for the original compound structure's layers, transfers original element parameters, and optionally attempts to restore wall joins between compatible layers.

## Overview

Compound Walls and Floors in Revit can contain multiple material layers within a single element. In workflows that require individual layer elements, separating these compound structures manually can involve substantial repetitive work.

This add-in automates that process by creating new elements corresponding to the original compound element's layers, positioning them at the original location, and removing the original element.

The tool also provides options to control selected operations during processing and reports execution results to the user.

## Key Features

- **Wall Layer Separation:** Separates existing compound Walls into individual layer elements.
- **Floor Layer Separation:** Applies the separation workflow to existing compound Floors.
- **Level-Based Processing:** Allows users to select a Level to process, limiting the scope of operations and helping avoid long-running tasks on older hardware.
- **Configurable Layer Naming:** Allows users to define default names for the different layer types found in the original compound elements.
- **Parameter Transfer:** Copies parameters from the original element to newly created layer elements.
- **Wall Join Restoration:** Attempts to restore joins between walls that were originally joined, joining compatible layers where possible.
- **Configurable Processing Operations:** Lets users choose which supported operations to perform during separation.
- **Execution Reporting:** Reports processing results to the user.

## How It Works

1. **Select a Level:** Choose the Level whose elements should be processed.
2. **Configure Layer Names:** Define default names for the layer types identified in the original compound elements.
3. **Choose the Operation:** Select whether to separate Walls or Floors.
4. **Configure Processing Options:** Enable or disable the supported operations, such as parameter transfer and wall-join restoration.
5. **Execute Separation:** The add-in creates individual elements for the compound structure's layers at their corresponding original locations.
6. **Replace Original Elements:** After processing, the original compound elements are removed.
7. **Review the Results:** The add-in reports the execution results.

## Technical Highlights

- **Language:** C#
- **Platform:** Autodesk Revit API
- **User Interface:** Windows Presentation Foundation (WPF)
- **Primary Target Version:** Autodesk Revit 2021
- **BIM Automation:** Automated element creation, parameter transfer, and wall-join handling.
- **Performance Considerations:** Level-based processing to limit the scope of operations and reduce the risk of unresponsive behavior on older machines.

## Results and Impact

The add-in was developed to reduce the manual effort involved in converting compound Wall and Floor elements into individual layer elements.

**Reported productivity improvement: approximately 75% time saved** in the relevant wall-separation workflow.

This figure reflects the reported result and should be treated as an approximate workflow-specific measurement rather than a universal benchmark.

## Demonstration

Screenshots and a short video demonstration will be added to illustrate:

- The add-in interface and processing options.
- The selection of a Level and configuration of layer names.
- A compound Wall before and after separation.
- A compound Floor before and after separation.
- Parameter transfer and wall-join restoration, where applicable.
- The execution report.

## Compatibility

- **Primary target:** Autodesk Revit 2021.
- The add-in was designed primarily for Revit 2021. Compatibility with other Revit versions has not yet been established in this documentation.

## Source Code

The application source code is not included in this public repository.

This repository serves as a portfolio case study documenting the tool's functionality, technical approach, and demonstrated value.

## Notes

This project demonstrates practical BIM automation using the Revit API, with a focus on automating repetitive modeling tasks, preserving relevant element information, and managing processing scope.

*Screenshots, demonstration media, and further technical documentation will be added as the portfolio entry is completed.*
