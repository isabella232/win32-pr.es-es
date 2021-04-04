---
title: Asignación de interfaz de usuario de objetos de grupo
description: En este tema se describen las hojas de propiedades de objetos de grupo del complemento usuarios y equipos de Active Directory. Propiedad general SheetMember de la propiedad SheetMembers de propiedad SheetManaged por hoja de propiedades
ms.assetid: c0cd73f0-f09f-4645-966d-6149888ce482
ms.tgt_platform: multiple
keywords:
- Asignación de la interfaz de usuario de objetos de grupo AD
- Asignación de interfaz de usuario, objeto de grupo AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2277c24f621f8e32f46b9e9571d0d0d4de9cfc
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077513"
---
# <a name="group-object-user-interface-mapping"></a>Asignación de interfaz de usuario de objetos de grupo

En este tema se describen las hojas de propiedades de objetos de grupo del complemento usuarios y equipos de Active Directory.

-   [Hoja de propiedades general](#general-property-sheet)
-   [Miembro de la hoja de propiedades](#member-of-property-sheet)
-   [Miembros (hoja de propiedades)](#members-property-sheet)
-   [Administrado por hoja de propiedades](#managed-by-property-sheet)

## <a name="general-property-sheet"></a>Hoja de propiedades general

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **General** .



| Etiqueta de la interfaz de usuario                      | Atributo en Active Directory Domain Services     |
|-------------------------------|---------------------------------------------------|
| Nombre de grupo (anterior a Windows 2000) | [**Nombre de cuenta SAM**](/windows/desktop/ADSchema/a-samaccountname) |
| Descripción                   | [**Descripción**](/windows/desktop/ADSchema/a-description)         |
| Correo electrónico                        | [**Direcciones de correo electrónico**](/windows/desktop/ADSchema/a-mail)           |
| Ámbito de grupo                   | [**Tipo de grupo**](/windows/desktop/ADSchema/a-grouptype)            |
| Tipo de grupo                    | [**Tipo de grupo**](/windows/desktop/ADSchema/a-grouptype)            |
| Notas                         | [**Comentario**](/windows/desktop/ADSchema/a-info)                    |



 

## <a name="member-of-property-sheet"></a>Miembro de la hoja de propiedades

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario del **miembro de** la hoja de propiedades.



| Etiqueta de la interfaz de usuario  | Atributo en Active Directory Domain Services | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-----------|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Miembro de | [**Is-member-of-DL**](/windows/desktop/ADSchema/a-memberof)    | Contiene los nombres distintivos de los grupos a los que pertenece este grupo. El atributo miembro de cada uno de los grupos de esta lista contiene el nombre distintivo de este objeto de grupo. La interfaz de usuario no modifica directamente el atributo [**is-member-of-DL**](/windows/desktop/ADSchema/a-memberof) . Modifica el atributo de [**miembro**](/windows/desktop/ADSchema/a-member) en el objeto de grupo del que este objeto es miembro. El servidor de Active Directory mantiene el atributo **is-member-of-DL** .<br/> |



 

## <a name="members-property-sheet"></a>Miembros (hoja de propiedades)

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **miembros** .



| Etiqueta de la interfaz de usuario | Atributo en Active Directory Domain Services | Descripción                                                           |
|----------|-----------------------------------------------|-----------------------------------------------------------------------|
| Miembros  | [**Miembro**](/windows/desktop/ADSchema/a-member)               | Contiene los nombres distintivos de los miembros de este objeto de grupo. |



 

## <a name="managed-by-property-sheet"></a>Administrado por hoja de propiedades

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **administrado por** .



| Etiqueta de la interfaz de usuario                           | Atributo en Active Directory Domain Services                                                                                   |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nombre                               | [**Administrado: por**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| El administrador puede actualizar la lista de pertenencia | Ninguno. Una ACE con el permiso "permitir-escribir miembros" se agrega a la cuenta identificada por el **nombre**.                        |
| Office                             | El atributo [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) de la cuenta identificada por **Name**. |
| Calle                             | El atributo [**calle-dirección**](/windows/desktop/ADSchema/a-street) de la cuenta identificada por **nombre**.                                    |
| City (Ciudad)                               | El atributo [**localidad-nombre**](/windows/desktop/ADSchema/a-l) de la cuenta identificada por **nombre**.                                          |
| Estado o provincia                     | El atributo [**State-or-provincia-Name**](/windows/desktop/ADSchema/a-st) de la cuenta identificada por **Name**.                                |
| País/región                     | El atributo [**Country-name**](/windows/desktop/ADSchema/a-c) de la cuenta identificada por **Name**.                                           |
| Número de teléfono                   | El atributo de [**número de teléfono**](/windows/desktop/ADSchema/a-telephonenumber) de la cuenta identificada por **nombre**.                         |
| Número de fax                         | El atributo [**facsímil-Phone-Number**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) de la cuenta identificada por **Name**.      |



 

 

