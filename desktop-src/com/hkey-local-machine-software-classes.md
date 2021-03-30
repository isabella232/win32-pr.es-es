---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: Las subclaves y los valores del registro asociados a la \_ clave HKEY local \_ Machine \\ software \\ classes contienen información sobre una aplicación que es necesaria para admitir la funcionalidad com.
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c16fdbc97b32d01af9c96b5670cb5a19c09c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779633"
---
# <a name="hkey_local_machinesoftwareclasses"></a>HKEY \_ \_ clases de \\ software de máquina local \\

Las subclaves y los valores del registro asociados a la clave **HKEY \_ local \_ Machine \\ software \\ classes** contienen información sobre una aplicación que es necesaria para admitir la funcionalidad com. Esta información incluye temas como formatos de datos admitidos, información de compatibilidad, identificadores de programación, DCOM y controles.



| Subclave                                                                         | Descripción                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**AppID**](appid-key.md)                                                     | Opciones de configuración para aplicaciones basadas en COM.                                                                 |
| [**CLSID**](clsid-key-hklm.md)                                                | Opciones de configuración para las clases COM.                                                                            |
| [**<extensión de archivo \_>**](-file-extension--key.md)                        | Asocia una extensión de nombre de archivo a un ProgID.                                                                   |
| [**FileType**](filetype-key.md)                                               | Usado por [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) para comparar patrones con distintos bytes de archivo en un archivo no compuesto. |
| [**Interfaz**](interface-key.md)                                             | Asocia un nombre de interfaz a un identificador de interfaz (IID).                                                          |
| [**<ProgID>**](-progid--key.md)                                         | Identifica una clase. Tenga en cuenta que no se garantiza que el ProgID sea único globalmente, a diferencia de un CLSID.                 |
| [**ProgID independiente de la versión de<>**](-version-independent-progid--key.md) | Se utiliza para determinar la versión más reciente de una aplicación de objeto.                                                    |



 

 

 




