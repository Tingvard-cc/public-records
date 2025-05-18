# Tingvard - Conflict of Interest (COI) Registry Data

This repository, specifically the `coi-registry.json` file, contains the public record of Conflict of Interest declarations for members of Tingvard associated with the Cardano Constitutional Committee.

## Purpose

The purpose of this registry is to ensure transparency and maintain the integrity of Tingvard's participation in governance activities by publicly documenting potential conflicts of interest.

## File: `conflict-of-interest/coi-registry.json`

This is the primary data file for the registry.

* **Format:** The file is in JSON (JavaScript Object Notation) format.
* **Structure:** It consists of a single JSON array `[]`, where each element in the array is an object `{}` representing one conflict of interest declaration.

### How to Read an Entry

Each entry (object) in the JSON array has the following fields (keys), typically in this order:

* **`id`**: (String)
    * A unique identifier automatically generated for the entry.
    * *Example:* `"jclp89xk1z6q8wfg0"`

* **`dateDeclared`**: (String)
    * The date on which the conflict of interest was formally declared.
    * *Format:* `YYYY-MM-DD` (e.g., "2025-05-18")

* **`member`**: (String)
    * The name of the Tingvard member associated with this declaration.
    * *Example:* `"Thomas Lindseth"`, `"Bjarne"`, etc.

* **`description`**: (String)
    * A detailed textual description of the nature of the potential conflict.
    * *Example:* `"Spouse holds a significant number of tokens in 'Project Alpha', which is seeking a grant..."`

* **`relatedEntity`**: (String)
    * The name of the external party, organization, project, or specific interest that the declared conflict pertains to.
    * *Example:* `"Project Alpha"`, `"Cardano Eco Solutions"`

* **`mitigationMeasures`**: (String)
    * A description of the steps taken, or proposed to be taken, to manage or mitigate the potential conflict. This might include recusal from certain decisions, disclosure, etc.
    * *Example:* `"Thomas will recuse himself from any discussion or vote related to Project Alpha's grant application..."`

* **`status`**: (String)
    * The current status of the declared conflict.
    * *Possible Values:* `"Active"`, `"Resolved"`, `"Under Review"`, `"Recused"`.
    * *Example:* `"Recused"`

### Example Entry Structure:

```json
{
  "id": "jclp89xk1z6q8wfg0",
  "dateDeclared": "2025-05-10",
  "member": "Thomas",
  "description": "Spouse holds a significant number of tokens in 'Project Alpha'...",
  "relatedEntity": "Project Alpha",
  "mitigationMeasures": "Thomas will recuse himself...",
  "status": "Recused"
}
