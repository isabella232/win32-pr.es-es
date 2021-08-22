---
description: ICE35 valida que los componentes que contienen archivos comprimidos almacenados en un archivo de archivador no se establecen para ejecutarse desde el origen. Con Windows Installer 2.0 o posterior, se ha quitado esta restricción.
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ee42f97a049b165d41fef7391f0031836865dbf7bafec6b1b5e2fb868e75a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528565"
---
# <a name="ice35"></a>ICE35

ICE35 valida que los componentes que contienen archivos comprimidos almacenados en un archivo [de](cabinet-files.md) archivador no se establecen para ejecutarse desde el origen. Con Windows Installer 2.0 o posterior, se ha quitado esta restricción.

ICE35 consulta la columna Gabinete de la [tabla Multimedia](media-table.md) para determinar qué archivos se comprimen y almacenan en un archivo de archivador. Consulta la tabla [File para determinar](file-table.md) qué componentes contienen estos archivos. Por último, comprueba la [tabla Component para](component-table.md) determinar si los bits de ejecución desde el origen se establecen en la columna Atributos.

## <a name="result"></a>Resultado

ICE35 envía un mensaje de error si hay un archivo comprimido almacenado en un archivo contenedor que pertenece a un componente con el conjunto de bits msidbComponentAttributesSourceOnly en la columna Atributos de la tabla [Component](component-table.md). Con Windows Installer 2.0 o posterior, se cambia de un error a un mensaje de advertencia. Un paquete que solo admite Windows Installer 2.0 y versiones posteriores tiene la propiedad PID PAGECOUNT del flujo de información de resumen establecida en un valor de al menos \_ 200.

ICE35 envía un mensaje de advertencia si hay un archivo comprimido almacenado en un archivo contenedor que pertenece a un componente con el bit msidbComponentAttributesOptional establecido en la columna Atributos de la tabla [Component](component-table.md). Este mensaje de advertencia se ha quitado con Windows Installer 2.0 y versiones posteriores.

Si hay varios archivos en un componente en un archivo archivador, ICE35 notifica errores para cada archivo que tiene la ejecución desde el conjunto de bits de origen.

## <a name="example"></a>Ejemplo

ICE35 notifica los siguientes errores y advertencias para el ejemplo que se muestra con una versión anterior a Windows Installer versión 2.0.



| ICE35 Error                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR: Componente 3 no se puede ejecutar solo desde el origen, porque su archivo miembro "File3" está comprimido. | Hay un archivo comprimido almacenado en un archivo archivador y este archivo pertenece a un componente con el bit SourceOnly establecido en la columna Atributos de la [tabla Component](component-table.md). Para corregir este error, cambie los 2 bits inferiores del valor Atributos de Component2 a "00", es decir, Solo local, o quite File4 del archivo CAB.<br/>                                                                                                                                                                         |
| ERROR: Componente 3 no se puede ejecutar solo desde el origen, porque su archivo miembro "File3" está comprimido. | Hay un archivo comprimido almacenado en un archivo archivador y este archivo pertenece a un componente con el bit SourceOnly establecido en la columna Atributos de la [tabla Component](component-table.md). Dado que los archivos de un componente no tienen que originarse todos en el mismo medio, ICE35 notifica errores para cada archivo del componente que está en un archivador.<br/> Para corregir este error, cambie los 2 bits inferiores del valor Atributos de Component2 a "00", es decir, Solo local, o quite File4 del archivo CAB.<br/> |



 

[Tabla multimedia](media-table.md) (parcial)



| DiskID | LastSequence | Gabinete   |
|--------|--------------|-----------|
| 1      | 2            |           |
| 2      | 4            | One.cab   |
| 3      | 5            | \#Two.cab |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo  | Componente\_ | Secuencia |
|-------|-------------|----------|
| Archivo1 | Componente1  | 1        |
| Archivo2 | Componente 2  | 2        |
| File3 | Componente 2  | 3        |
| File4 | Componente 3  | 4        |
| File5 | Componente 3  | 5        |



 

[Tabla de componentes](component-table.md) (parcial)



| Componente  | Atributos |
|------------|------------|
| Componente1 | 0          |
| Componente 2 | 2          |
| Componente 3 | 1          |



 

[Tabla de métodos abreviados](shortcut-table.md) (parcial)



| Acceso directo  | Icono\_ |
|-----------|--------|
| Acceso directo1 | Icono2  |



 

Tenga en cuenta que los archivos también se pueden marcar como comprimidos mediante la propiedad [**Resumen**](word-count-summary.md) de recuento de palabras del [flujo de información de resumen](summary-information-stream.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




