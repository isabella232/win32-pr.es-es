---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: Las subclaves y los valores del Registro asociados a la clave HKEY LOCAL MACHINE SOFTWARE Classes contienen información sobre una aplicación necesaria para \_ \_ admitir la funcionalidad \\ \\ COM.
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9a79c417c48c5392fe5ceea3e99cce5e874bc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973638"
---
# <a name="hkey_local_machinesoftwareclasses"></a>Clases HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\

Las subclaves y los valores del Registro asociados a la clave **HKEY \_ LOCAL MACHINE SOFTWARE \_ \\ \\ Classes** contienen información sobre una aplicación necesaria para admitir la funcionalidad COM. Esta información incluye temas como formatos de datos admitidos, información de compatibilidad, identificadores de programación, DCOM y controles.



| Subclave                                                                         | Descripción                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**Appid**](appid-key.md)                                                     | Opciones de configuración para aplicaciones basadas en COM.                                                                 |
| [**CLSID**](clsid-key-hklm.md)                                                | Opciones de configuración para clases COM.                                                                            |
| [**<extensión \_ de archivo>**](-file-extension--key.md)                        | Asocia una extensión de nombre de archivo a un ProgID.                                                                   |
| [**FileType**](filetype-key.md)                                               | [**GetClassFile lo usa para**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) hacer coincidir patrones con varios bytes de archivo en un archivo no compuesto. |
| [**Interfaz**](interface-key.md)                                             | Asocia un nombre de interfaz a un identificador de interfaz (IID).                                                          |
| [**&lt;ProgID&gt;**](-progid--key.md)                                         | Identifica una clase. Tenga en cuenta que no se garantiza que el ProgID sea único globalmente, a diferencia de un CLSID.                 |
| [**<progID independiente de la versión>**](-version-independent-progid--key.md) | Se usa para determinar la versión más reciente de una aplicación de objeto.                                                    |



 

 

 




