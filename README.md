# Revit Wall & Floor Layer Separation

A Revit add-in developed in C# to automate the separation of compound Walls and Floors into individual layer elements, supporting BIM workflows that require more detailed element modeling.

Designed primarily for **Autodesk Revit 2021**, the tool processes elements level by level, creates individual elements for the original compound structure's layers, transfers original element parameters, and optionally attempts to restore wall joins between compatible layers.

## Overview

Compound Walls and Floors in Revit can contain multiple material layers within a single element. In workflows that require individual layer elements, separating these compound structures manually can involve substantial repetitive work.

This add-in automates that process by creating new elements corresponding to the original compound element's layers, positioning them at the original location, and removing the original element.

The tool also provides options to control selected operations during processing and reports execution results to the user.

## Key Features

- **Wall Layer Separation:** Separates existing compound Walls into individual layer elements.
- **Floor Layer Separation:** Applies the same layer-separation workflow to existing compound Floors.
- **Level-Based Processing:** Filters elements by their associated Level, allowing users to limit processing scope and helping reduce the risk of long-running operations on older hardware.
- **Configurable Layer Naming:** Allows users to define default names for the different layer types found in the original compound elements.
- **Parameter Transfer:** Copies the original element's parameters to newly created layer elements, excluding parameters that affect geometry.
- **Geometry Preservation:** Creates individual layer elements at the corresponding original layer locations, preserving the original layer geometry.
- **Conditional Wall-Join Restoration:** Attempts to restore joins between walls that were joined before separation, joining compatible layers where possible.
- **Configurable Processing Operations:** Allows users to choose which supported operations to perform during the separation process.
- **Execution Reporting:** Reports processing results to the user.

## How It Works

1. **Select a Level:** Choose the Level whose associated elements should be processed.
2. **Configure Layer Names:** Define default names for the layer types identified in the original compound elements.
3. **Choose the Element Type:** Select whether to process Walls or Floors.
4. **Configure Processing Options:** Choose which supported operations to perform during separation.
5. **Create Individual Layer Elements:** The add-in creates new elements corresponding to the original compound element's layers, positioning them to preserve the original layer geometry.
6. **Transfer Parameters:** Copies applicable parameters from the original element to the newly created layer elements, excluding geometry-affecting parameters.
7. **Restore Wall Joins Where Applicable:** For Walls that were joined before separation, the add-in attempts to restore joins between compatible corresponding layers.
8. **Remove Original Elements:** Removes the original compound elements as part of the replacement workflow.
9. **Review Execution Results:** Displays a report of the processing results.

## Technical Highlights

- **Language:** C#
- **Platform:** Autodesk Revit API
- **User Interface:** Windows Presentation Foundation (WPF)
- **Primary Target Version:** Autodesk Revit 2021
- **Element Processing:** Level-based filtering using each element's associated Level.
- **Parameter Management:** Transfers non-geometry-affecting parameters from original elements to generated layer elements.
- **Geometry Handling:** Preserves the original layer geometry when generating individual elements.
- **Wall-Join Handling:** Attempts to restore original wall-join relationships between compatible layers when the original walls were joined.
- **Performance Considerations:** Allows users to restrict processing to a selected Level, helping keep operations manageable on older hardware.

## Results and Impact

The add-in automates the separation of compound Walls and Floors into individual layer elements, reducing repetitive manual modeling work.

**Reported productivity improvement: approximately 75% time saved** across the Wall and Floor separation workflows.

This is an approximate, workflow-specific result based on the reported experience with the tool, rather than a universal performance benchmark.

## Compatibility

- **Primary target:** Autodesk Revit 2021.
- Compatibility with other Revit versions has not yet been established in this documentation.

## Demonstration

Screenshots and a short video demonstration will be added to illustrate:

- The add-in interface and processing options.
- The selection of a Level and configuration of layer names.
- A compound Wall before and after separation.
- A compound Floor before and after separation.
- Parameter transfer and wall-join restoration, where applicable.
- The execution report.


## Source Code

The application source code is not included in this public repository.

This repository serves as a portfolio case study documenting the tool's functionality, technical approach, and demonstrated value.

## Notes

This project demonstrates practical BIM automation using the Revit API, with a focus on automating repetitive modeling tasks, preserving relevant element information, and managing processing scope.

*Screenshots, demonstration media, and further technical documentation will be added as the portfolio entry is completed.*
