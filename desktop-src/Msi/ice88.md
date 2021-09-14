---
description: ICE88 valida que el directorio al que se hace referencia en la columna DirProperty de la tabla IniFile existe en el paquete Windows Installer.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074516"
---
# <a name="ice88"></a>ICE88

ICE88 valida que el directorio al que se hace referencia en la columna DirProperty de la tabla [IniFile](inifile-table.md) existe en el paquete Windows Installer. ICE88 emite una advertencia si el valor DirProperty no representa una propiedad en [](property-reference.md)las tablas Directory, AppSearch o Property, determinadas propiedades de carpeta del sistema o una propiedad establecida por una acción personalizada de tipo 51.

ICE88 examina las siguientes tablas y propiedades.

-   [Tabla de directorios](directory-table.md)
-   [Tabla de AppSearch](appsearch-table.md)
-   [Tabla de propiedades](property-table.md)
-   [CustomAction Table](customaction-table.md) , donde la acción personalizada es un [tipo de acción personalizada 51](custom-action-type-51.md)
-   [**Propiedad ProgramFilesFolder**](programfilesfolder.md)
-   [**Propiedad CommonFilesFolder**](commonfilesfolder.md)
-   [**Propiedad SystemFolder**](systemfolder.md)
-   [**Propiedad ProgramFiles64Folder**](programfiles64folder.md)
-   [**Propiedad CommonFiles64Folder**](commonfiles64folder.md)
-   [**Propiedad System64Folder**](system64folder.md)

## <a name="result"></a>Resultado

ICE88 publica la advertencia siguiente.



| Advertencia de ICE88                                                                                                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En la entrada de la tabla IniFile (IniFile=) 3, DirProperty= 1 no se encuentra en las tablas \[ \] \[ Directory/Property/AppSearch/CA-Type51 y no es una de las propiedades del \] instalador. | Para cada registro de la tabla IniFile, ICE88 lee el valor de la columna DirProperty. ICE88 busca el valor en la tabla de [](property-table.md) directorios, [](directory-table.md)la tabla de [AppSearch](appsearch-table.md)y la tabla de propiedades y también examina la lista de propiedades establecidas por el instalador. ICE88 envía esta advertencia si no se encuentra el valor en el examen. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



