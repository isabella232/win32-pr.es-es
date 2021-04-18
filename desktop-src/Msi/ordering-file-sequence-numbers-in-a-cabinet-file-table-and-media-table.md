---
description: La tabla de archivos contiene una lista completa de todos los archivos de origen de la instalación.
ms.assetid: 481fdc45-82db-4128-93de-388562f636e9
title: Orden de los números de secuencia de archivo en un archivo. cab, tabla de archivos y tabla de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07f9cd530d90fb0ef4d805b8ff2c96398cd97e55
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105653125"
---
# <a name="ordering-file-sequence-numbers-in-a-cabinet-file-table-and-media-table"></a>Orden de los números de secuencia de archivo en un archivo. cab, tabla de archivos y tabla de medios

La [tabla de archivos](file-table.md) contiene una lista completa de todos los archivos de origen de la instalación. Los archivos se pueden almacenar en el medio de origen como archivos individuales o comprimirse dentro de [los archivos. cab](cabinet-files.md). Los números de secuencia de la columna secuencia de la tabla de archivos, junto con el campo LastSequence de la [tabla de medios](media-table.md), especifican el orden de instalación de los archivos y el medio de origen en el que se encuentra cada archivo. Cada registro de la tabla de medios identifica el disco de origen que contiene todos los archivos con números de secuencia menores o iguales que el valor mostrado en la columna LastSequence y mayor que el valor LastSequence del disco anterior.

Por ejemplo, supongamos que un archivo tiene un número de secuencia de 92 especificado en la columna secuencia de la tabla archivo. Para determinar en qué disco de origen reside este archivo, el instalador comprueba el registro de la tabla de medios para la entrada con el menor valor de LastSequence mayor que 92. La columna dipatine es la clave principal de la tabla de medios y este campo identifica de forma única el disco en la tabla.

El límite máximo del número de archivos que se pueden enumerar en la tabla de archivos de un paquete Windows Installer es 32767 archivos. Para crear un paquete de Windows Installer que contenga más archivos, consulte [crear un paquete de gran tamaño](authoring-a-large-package.md).

Los autores de paquetes pueden reducir el tamaño de los paquetes de instalación mediante la compresión de los archivos de origen y su inclusión en los archivos. cab. La imagen del archivo de origen se puede comprimir, descomprimir o una mezcla de ambos tipos. Para obtener más información acerca de los orígenes comprimidos y sin comprimir, vea [orígenes comprimidos y sin comprimir](compressed-and-uncompressed-sources.md). Los archivos de código fuente comprimidos deben almacenarse en un archivo. cab. Los archivos comprimidos dentro de un archivo. cab tienen sus propios números de secuencia internos. No es necesario que los valores de estos números de secuencia internos coincidan con el valor de los números de secuencia de la tabla de archivos. Sin embargo, la secuencia de los archivos especificados en la tabla de archivos debe ser idéntica a la secuencia real de los archivos dentro de los contenedores. Los números de secuencia de archivos sin comprimir no deben ser únicos. Por ejemplo, si todos los archivos se descomprimen y residen en un disco, todos los archivos pueden tener el mismo número de secuencia en la tabla de archivos.

En la tabla de medios se describe el conjunto de discos que componen el medio de origen para la instalación. La primera entrada de la tabla de medios debe tener siempre un 1 en el campo de despatín. Los archivos se deben organizar en el medio de origen de tal forma que todos los archivos del disco 1 tengan números de secuencia de la tabla de archivos menores que los números de secuencia de los archivos del disco 2, y todos los números de secuencia del disco 2 deben ser menores que en el disco 3, y así sucesivamente. Este requisito también se aplica a un disco que contiene orígenes comprimidos y sin comprimir. Por ejemplo, si los orígenes multimedia para la instalación se encuentran en dos discos de origen y el disco 1 contiene archivos sin comprimir y un archivo. cab, los dos archivos sin comprimir y los archivos del archivo. cab deben tener números de secuencia menores que el número de secuencia de archivo más pequeño de cualquier archivo almacenado en el disco 2. Si todos los archivos del disco 1 se comprimen en un archivo. cab, la tabla de medios podría crearse tal como se muestra en la tabla siguiente.

[Tabla de medios](media-table.md) (parcial)



| Detectaron | LastSequence | DiskPrompt | Archiva   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          | mycab.cab | Disco 1      |
| 2      | 10           | 2          |           | Disco 2      |



 

Si algunos archivos del disco 1 se comprimen en un archivo contenedor y otros se descomprimen, la tabla de medios podría crearse como se indica a continuación.

[Tabla de medios](media-table.md) (parcial)



| Detectaron | LastSequence | DiskPrompt | Archiva   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disco 1      |
| 2      | 10           | 1          | mycab.cab | Disco 1      |
| 3      | 15           | 2          |           | Disco 2      |



 

Tenga en cuenta que la creación de la siguiente tabla multimedia es incorrecta porque especifica algunos números de secuencia de archivos en el disco 2 que son más pequeños que algunos archivos dentro del archivo. cab del disco 1.

[Tabla de medios](media-table.md)



| Detectaron | LastSequence | DiskPrompt | Archiva   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disco 1      |
| 2      | 10           | 2          |           | Disco 2      |
| 3      | 15           | 1          | mycab.cab | Disco 1      |



 

Los archivos grandes pueden dividirse entre dos o más archivos. cab. No puede haber más de 15 archivos en un archivo contenedor que abarque al siguiente archivo. cab. Por ejemplo, si tiene tres archivos contenedores, el primero puede tener 15 archivos que abarcan el segundo archivo. cab y el segundo puede tener 15 archivos que abarcan el tercer archivo. cab. Al agregar un registro a la tabla de archivos para un archivo con varios contenedores, use la primera parte del archivo para especificar el número de secuencia de archivo que especifique en la columna secuencia.

Las tablas de archivos y medios pueden crearse de la siguiente manera si hay tres archivos, dos gabinetes y dos discos. En este ejemplo, c1.cab reside en Disk1 y c2.cab reside en Disk2. El archivo F2 abarca ambos gabinetes. El archivo. cab de c1.cab contiene el archivo F1 completo y la primera parte del archivo F2. El contenedor de c2.cab contiene la segunda parte de F2 y el archivo de F3 completo.

[Tabla de medios](media-table.md) (parcial)



| Detectaron | LastSequence | DiskPrompt | Archiva | VolumeLabel |
|--------|--------------|------------|---------|-------------|
| 1      | 5            | 1          | c1.cab  | Disco 1      |
| 2      | 10           | 2          | c2.cab  | Disco 2      |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo | Secuencia |
|------|----------|
| tecla   | 1        |
| C2   | 2        |
| Ctrl   | 6        |



 

 

 



