# Software Requirements Specification

[This software requirements specification](https://github.com/JanssenSimon/OpenAPICheck/blob/main/docs/SoftwareRequirementsSpec.md) by the OpenAPICheck team is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

## Introduction

### Purpose
The purpose of this document is to give the collaborators who are responsible for creating the OpenAPICheck software all of the information necessary to design, develop, and test the software.

### Scope
This document contains a complete description of the functionality of the OpenAPICheck software. It consists of use cases, functional requirements, and nonfunctional requirements, which, taken together, form the complete description.

### System Overview
The OpenAPICheck software is a command line tool for validating OpenAPI documents and for performing simple validations on an HTTP API endpoint based on a provided OpenAPI document.

### References
- *[OpenAPI Specification v3.1.1](https://spec.openapis.org/oas/v3.1.1.html)* / Darrel Miller et al. – the Linux Foundation, 2024.

## Definitions

**API**: Application programming interface, in the context of this document, REST APIs served over HTTP
**REST API**: A type of API that uses the representational state transfer (REST) architectural style
**HTTP**: Hypertext transfer protocol, a protocol used to transfer hypertext documents (generally) over the internet
**manpage**: Manual page structured in the format used by the `man` unix utility.

## Use cases

The OpenAPICheck software has 3 main use cases, namely providing documentation of itself, validating and OpenAPI document, or checking whether an HTTP REST API is compliant with a given OpenAPI document.

| Name                   | UC-1: Help                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| Summary                | To display documentation                                                                       |
| Rationale              | Users will want documentation to learn or to refresh their knowledge on how the program works. |
| Users                  | Any user                                                                                       |
| Basic course of events | 1. The user invokes the program in their shell while passing the help flag  2. The program displays the help page |
| Alternative paths      | 1. The user invokes `man` to see the man page for the program  2. The man page is displayed    |

| Name                   | UC-2: Validation of OpenAPI document                                                           |
|------------------------|------------------------------------------------------------------------------------------------|
| Summary                | To validate an OpenAPI document                                                                |
| Rationale              | Users will want to ensure that an OpenAPI document is well-formed, using our tool to know if there are errors (and if so, where). |
| Users                  | Any user                                                                                       |
| Basic course of events | 1. The user invokes the program with a provided file location (system path or URL)  2. The program outputs whether the document is well-formed, and if not, what and where the errors are |

| Name                   | UC-3: Testing of API using OpenAPI document                                                    |
|------------------------|------------------------------------------------------------------------------------------------|
| Summary                | To test an HTTP REST API endpoint, making sure it agrees with a provided OpenAPI document      |
| Rationale              | Given an OpenAPI description, simple verifications to ensure an API's compliance with the description are beneficial when developing the API |
| Users                  | Any user                                                                                       |
| Basic course of events | 1. The user invokes the program with a provided API endpoint location (URL)  2. The program fetches the OpenAPI document for the API by requesting the OpenAPI.json or OpenAPI.yaml file  3. If the OpenAPI document is well-formed, the program performs checks on the API to ensure its compliance with the OpenAPI description |

## Functional requirements

The functional requirements are yet to be determined.

## Nonfunctional requirements

There are no nonfunctional requirements aside from, perhaps, composability; the OpenAPICheck software should compose well with other unix utilities using pipes, if appropriate.
