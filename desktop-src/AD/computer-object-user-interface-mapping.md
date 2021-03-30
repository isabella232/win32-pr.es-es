---
title: Asignación de interfaz de usuario de objetos de equipo
description: En las tablas siguientes se enumeran los elementos de las hojas de propiedades de objetos de equipo en el complemento usuarios y equipos de Active Directory.
ms.assetid: e2a7a42d-e854-43fc-a36b-f3031c1685a7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2a2b3ed4ec8cbf3c1af59e024fc5e04bc68ae8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789610"
---
# <a name="computer-object-user-interface-mapping"></a>Asignación de interfaz de usuario de objetos de equipo

En las tablas siguientes se enumeran los elementos de las hojas de propiedades de objetos de equipo en el complemento usuarios y equipos de Active Directory.

## <a name="general-property-sheet"></a>Hoja de propiedades general

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **General** .



| Etiqueta de la interfaz de usuario                         | Active Directory Domain Services atributo) | Comentarios                                         |
|----------------------------------|--------------------------------------------|--------------------------------------------------|
| Nombre del equipo (anterior a Windows 2000) | sAMAccountName                             |                                                  |
| Nombre DNS                         | dNSHostName                                |                                                  |
| Role                             | userAccountControl                         | Alterna un bit en la máscara de bits de userAccountControl. |
| Descripción                      | description                                |                                                  |
| Confiar en equipo para delegación    | userAccountControl                         | Alterna un bit en la máscara de bits de userAccountControl. |



 

## <a name="location-property-sheet"></a>Ubicación (hoja de propiedades)

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **Location** .



| Etiqueta de la interfaz de usuario | Active Directory Domain Services atributo) |
|----------|--------------------------------------------|
| Location | ubicación                                   |



 

## <a name="member-of-property-sheet"></a>Miembro de la hoja de propiedades

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario del **miembro de** la hoja de propiedades.



| Etiqueta de la interfaz de usuario          | Active Directory Domain Services atributo) | Comentarios                                                                                                                                                                   |
|-------------------|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Miembro de         | memberOf                                   | Incluye todos los grupos de la lista de interfaz de usuario, excepto el grupo principal, que se representa en el AD mediante el atributo [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) . |
| Establecer grupo principal | primaryGroupID                             | LDAP: vinculado a [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del grupo principal.                                                                                  |



 

## <a name="operating-system-property-sheet"></a>Hoja de propiedades del sistema operativo

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **del sistema operativo** .



| Etiqueta de la interfaz de usuario     | Active Directory Domain Services atributo) |
|--------------|--------------------------------------------|
| Nombre         | operatingSystem                            |
| Versión      | operatingSystemVersion                     |
| Service Pack | operatingSystemServicePack                 |



 

 

 