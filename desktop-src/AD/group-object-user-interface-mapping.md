---
title: Asignación de objetos Interfaz de usuario grupo
description: En este tema se describen las hojas de propiedades de objetos Group Usuarios y equipos de Active Directory complemento. Hoja de propiedades generalMember of Property SheetMembers Property SheetManaged By Property Sheet
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- Group Object Interfaz de usuario Mapping AD
- Interfaz de usuario asignación de grupos, ad de objeto de grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 308b3bafc24f8b8419b23c351d981f4f01961885cd535ac2d24b96cd62e17633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188969"
---
# <a name="group-object-user-interface-mapping"></a>Asignación de objetos Interfaz de usuario grupo

En este tema se describen las hojas de propiedades de objetos Group Usuarios y equipos de Active Directory complemento.

-   [Hoja de propiedades general](#general-property-sheet)
-   [Miembro de la hoja de propiedades](#member-of-property-sheet)
-   [Hoja de propiedades Miembros](#members-property-sheet)
-   [Hoja de propiedades Administrada por](#managed-by-property-sheet)

## <a name="general-property-sheet"></a>Hoja de propiedades general

En la tabla siguiente se muestran las etiquetas de interfaz de usuario de la **hoja de** propiedades General.



| Etiqueta de interfaz de usuario                      | Atributo en Active Directory Domain Services     |
|-------------------------------|---------------------------------------------------|
| Nombre del grupo (Windows 2000) | [**SAM-Account-Name**](/windows/desktop/ADSchema/a-samaccountname) |
| Descripción                   | [**Descripción**](/windows/desktop/ADSchema/a-description)         |
| Correo electrónico                        | [**Direcciones de correo electrónico**](/windows/desktop/ADSchema/a-mail)           |
| Ámbito de grupo                   | [**Tipo de grupo**](/windows/desktop/ADSchema/a-grouptype)            |
| Tipo de grupo                    | [**Tipo de grupo**](/windows/desktop/ADSchema/a-grouptype)            |
| Notas                         | [**Comentario**](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a>Miembro de la hoja de propiedades

En la tabla siguiente se muestran las etiquetas de interfaz de usuario **de la hoja de propiedades Miembro** de .



| Etiqueta de interfaz de usuario  | Atributo en Active Directory Domain Services | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Miembro de | [**Is-Member-Of-DL**](/windows/desktop/ADSchema/a-memberof)    | Contiene los nombres distintivos de los grupos a los que pertenece este grupo. El atributo miembro de cada uno de los grupos de esta lista contiene el nombre distintivo de este objeto de grupo. La interfaz de usuario no modifica directamente el [**atributo Is-Member-Of-DL.**](/windows/desktop/ADSchema/a-memberof) Modifica el atributo [**Member**](/windows/desktop/ADSchema/a-member) en el objeto de grupo del que este objeto se ha hecho miembro. El Active Directory mantiene el **atributo Is-Member-Of-DL.**<br/> |



 

## <a name="members-property-sheet"></a>Hoja de propiedades Miembros

En la tabla siguiente se muestran las etiquetas de interfaz de usuario de **la hoja de propiedades** Miembros.



| Etiqueta de interfaz de usuario | Atributo en Active Directory Domain Services | Descripción                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| Miembros  | [**Miembro**](/windows/desktop/ADSchema/a-member)               | Contiene los nombres distintivos de los miembros de este objeto de grupo. |



 

## <a name="managed-by-property-sheet"></a>Hoja de propiedades Administrada por

En la tabla siguiente se muestran las etiquetas de interfaz de usuario **de la hoja de** propiedades Administrado por.



| Etiqueta de interfaz de usuario                           | Atributo en Active Directory Domain Services                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nombre                               | [**Administrado por**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| El administrador puede actualizar la lista de pertenencia | Ninguno. Se agrega una ACE con el permiso "Permitir - Escribir miembros" a la cuenta identificada por **Name**.                        |
| Office                             | Atributo [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) de la cuenta identificada por **Name**. |
| Calle                             | Atributo [**Street-Address**](/windows/desktop/ADSchema/a-street) de la cuenta identificada por **Name**.                                    |
| City (Ciudad)                               | Atributo [**Locality-Name**](/windows/desktop/ADSchema/a-l) de la cuenta identificada por **Name**.                                          |
| Estado o provincia                     | Atributo [**State-Or-Province-Name**](/windows/desktop/ADSchema/a-st) de la cuenta identificada por **Name**.                                |
| País o región                     | Atributo [**Country-Name**](/windows/desktop/ADSchema/a-c) de la cuenta identificada por **Name**.                                           |
| Número de teléfono                   | Atributo [**Telephone-Number**](/windows/desktop/ADSchema/a-telephonenumber) de la cuenta identificada por **Name**.                         |
| Número de fax                         | Atributo [**Facsimile-Telephone-Number**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) de la cuenta identificada por **Name**.      |



 

 

