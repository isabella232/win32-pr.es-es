---
description: ICE35 valida que los componentes que contienen archivos comprimidos almacenados en un archivo. cab no estén configurados para ejecutarse desde el origen. Con Windows Installer 2,0 o posterior, esta restricción se ha quitado.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002252"
---
# <a name="ice35"></a>ICE35

ICE35 valida que los componentes que contienen archivos comprimidos almacenados en un [archivo. cab](cabinet-files.md) no estén configurados para ejecutarse desde el origen. Con Windows Installer 2,0 o posterior, esta restricción se ha quitado.

ICE35 consulta la columna Cabinet de la [tabla de medios](media-table.md) para determinar qué archivos se comprimen y almacenan en un archivo. cab. Consulta la [tabla de archivos](file-table.md) para determinar qué componentes contienen estos archivos. Finalmente, comprueba la [tabla de componentes](component-table.md) para determinar si los bits de origen de ejecución se establecen en la columna de atributos.

## <a name="result"></a>Resultado

ICE35 envía un mensaje de error si hay un archivo comprimido almacenado en un archivo. cab que pertenece a un componente con el bit msidbComponentAttributesSourceOnly establecido en la columna Attributes de la [tabla Component](component-table.md). Con Windows Installer 2,0 o posterior, se cambia de un error a un mensaje de advertencia. Un paquete que solo admite Windows Installer 2,0 y versiones posteriores tiene la \_ propiedad de PID PAGECOUNT de la secuencia de información de Resumen establecida en un valor de al menos 200.

ICE35 envía un mensaje de advertencia si hay un archivo comprimido almacenado en un archivo. cab que pertenece a un componente con el bit msidbComponentAttributesOptional establecido en la columna atributos de la [tabla componente](component-table.md). Este mensaje de advertencia se ha quitado con Windows Installer 2,0 y versiones posteriores.

Si hay varios archivos en un componente en un archivo. cab, ICE35 informa de los errores de cada archivo que tiene el conjunto de bits de origen ejecutado.

## <a name="example"></a>Ejemplo

ICE35 notifica los siguientes errores y advertencias para el ejemplo que se muestra con una versión anterior a Windows Installer versión 2,0.



| Error ICE35                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR: el componente Component3 no se puede ejecutar solo desde el origen, porque su archivo de miembro ' Archivo3 ' está comprimido. | Hay un archivo comprimido almacenado en un archivo. cab y este archivo pertenece a un componente con el bit SourceOnly establecido en la columna Attributes de la [tabla de componentes](component-table.md). Para corregir este error, cambie los 2 bits inferiores del valor de los atributos Component2's a "00", lo que significa solo local o quite File4 del archivo. CAB.<br/>                                                                                                                                                                         |
| ERROR: el componente Component3 no se puede ejecutar solo desde el origen, porque su archivo de miembro ' Archivo3 ' está comprimido. | Hay un archivo comprimido almacenado en un archivo. cab y este archivo pertenece a un componente con el bit SourceOnly establecido en la columna Attributes de la [tabla de componentes](component-table.md). Dado que no todos los archivos de un componente tienen que proceder de los mismos medios, ICE35 informa de los errores de cada archivo del componente que se encuentra en un archivo. cab.<br/> Para corregir este error, cambie los 2 bits inferiores del valor de los atributos Component2's a "00", lo que significa solo local o quite File4 del archivo. CAB.<br/> |



 

[Tabla de medios](media-table.md) (parcial)



| DiskID | LastSequence | Archiva   |
|--------|--------------|-----------|
| 1      | 2            |           |
| 2      | 4            | One.cab   |
| 3      | 5            | \#Two.cab |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ | Secuencia |
|-------|-------------|----------|
| Archivo1 | Component1  | 1        |
| Archivo2 | Component2  | 2        |
| File3 | Component2  | 3        |
| File4 | Component3  | 4        |
| File5 | Component3  | 5        |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Atributos |
|------------|------------|
| Component1 | 0          |
| Component2 | 2          |
| Component3 | 1          |



 

[Tabla de acceso directo](shortcut-table.md) (parcial)



| Acceso directo  | Icono\_ |
|-----------|--------|
| Shortcut1 | Icon2  |



 

Tenga en cuenta que los archivos también se pueden marcar como comprimidos mediante la propiedad [**recuento de palabras**](word-count-summary.md) de la [secuencia de información de Resumen](summary-information-stream.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




