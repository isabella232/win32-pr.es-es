---
title: Asignación de objetos Interfaz de usuario equipo
description: En las tablas siguientes se muestran los elementos de las hojas de propiedades de objetos Computer Usuarios y equipos de Active Directory complemento.
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061590"
---
# <a name="computer-object-user-interface-mapping"></a>Asignación de objetos Interfaz de usuario equipo

En las tablas siguientes se muestran los elementos de las hojas de propiedades de objetos Computer Usuarios y equipos de Active Directory complemento.

## <a name="general-property-sheet"></a>Hoja de propiedades general

En la tabla siguiente se enumeran las etiquetas de interfaz de usuario de la **hoja de** propiedades General.



| Etiqueta de interfaz de usuario                         | Active Directory Domain Services atributo | Comentarios                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| Nombre del equipo (Windows 2000) | sAMAccountName                             |                                                  |
| Nombre DNS                         | dNSHostName                                |                                                  |
| Rol                             | userAccountControl                         | Alterna un bit en la máscara de bits userAccountControl. |
| Descripción                      | description                                |                                                  |
| Confiar en el equipo para la delegación    | userAccountControl                         | Alterna un bit en la máscara de bits userAccountControl. |



 

## <a name="location-property-sheet"></a>Hoja de propiedades de ubicación

En la tabla siguiente se enumeran las etiquetas de interfaz de usuario de **la hoja de** propiedades Ubicación.



| Etiqueta de interfaz de usuario | Active Directory Domain Services atributo |
|----------|--------------------------------------------|
| Ubicación | ubicación                                   |



 

## <a name="member-of-property-sheet"></a>Miembro de la hoja de propiedades

En la tabla siguiente se enumeran las etiquetas de interfaz de usuario **de la hoja de propiedades Miembro** de .



| Etiqueta de interfaz de usuario          | Active Directory Domain Services atributo | Comentarios                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Miembro de         | memberOf                                   | Incluye todos los grupos de la lista de interfaz de usuario, excepto el grupo principal, que se representa en AD a través del [**atributo primaryGroupId.**](/windows/desktop/ADSchema/a-primarygroupid) |
| Establecer grupo principal | primaryGroupID                             | LDAP: asociado a [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del grupo principal.                                                                                  |



 

## <a name="operating-system-property-sheet"></a>Hoja de propiedades del sistema operativo

En la tabla siguiente se enumeran las etiquetas de interfaz de usuario de la **hoja de propiedades del sistema** operativo.



| Etiqueta de interfaz de usuario     | Active Directory Domain Services atributo |
|--------------|--------------------------------------------|
| Nombre         | operatingSystem                            |
| Version      | operatingSystemVersion                     |
| Service Pack | operatingSystemServicePack                 |



 

 

 