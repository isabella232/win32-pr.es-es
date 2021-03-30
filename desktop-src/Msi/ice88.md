---
description: ICE88 valida que el directorio al que se hace referencia en la columna DirProperty de la tabla IniFile existe en el paquete de Windows Installer.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912305"
---
# <a name="ice88"></a>ICE88

ICE88 valida que el directorio al que se hace referencia en la columna DirProperty de la [tabla inifile](inifile-table.md) existe en el paquete de Windows Installer. ICE88 emite una advertencia si el valor de DirProperty no representa una propiedad en el directorio, AppSearch o las tablas de propiedades, ciertas [propiedades de carpeta del sistema](property-reference.md)o una propiedad establecida por una acción personalizada Type 51.

ICE88 examina las siguientes tablas y propiedades.

-   [Tabla de directorio](directory-table.md)
-   [Tabla AppSearch](appsearch-table.md)
-   [Tabla de propiedades](property-table.md)
-   [Tabla CustomAction](customaction-table.md) , donde la acción personalizada es un [tipo de acción personalizada 51](custom-action-type-51.md)
-   [**ProgramFilesFolder (propiedad)**](programfilesfolder.md)
-   [**Propiedad CommonFilesFolder**](commonfilesfolder.md)
-   [**Propiedad Carpetadelsistema**](systemfolder.md)
-   [**Propiedad ProgramFiles64Folder**](programfiles64folder.md)
-   [**Propiedad CommonFiles64Folder**](commonfiles64folder.md)
-   [**Propiedad System64Folder**](system64folder.md)

## <a name="result"></a>Resultado

ICE88 envía la siguiente advertencia.



| ADVERTENCIA de ICE88                                                                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En la entrada de tabla IniFile (IniFile =) \[ 3, \] DirProperty = \[ 1 \] no se encuentra en las tablas Directory/Property/AppSearch/CA-Type51 y no es una de las propiedades del instalador. | Para cada registro de la tabla IniFile, ICE88 lee el valor de la columna DirProperty. ICE88 busca el valor en la tabla de [directorios](directory-table.md), la [tabla AppSearch](appsearch-table.md)y la [tabla de propiedades](property-table.md) , además de examinar la lista de propiedades establecida por el instalador. ICE88 envía esta advertencia si el valor no se encuentra en el examen. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



