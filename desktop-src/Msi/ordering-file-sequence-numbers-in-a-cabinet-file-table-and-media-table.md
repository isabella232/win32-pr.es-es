---
description: La tabla File contiene una lista completa de todos los archivos de origen para la instalación.
ms.assetid: 481fdc45-82db-4128-93de-388562f636e9
title: Ordenar números de secuencia de archivo en un archivador, una tabla de archivos y una tabla multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07f9cd530d90fb0ef4d805b8ff2c96398cd97e55
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251006"
---
# <a name="ordering-file-sequence-numbers-in-a-cabinet-file-table-and-media-table"></a>Ordenar números de secuencia de archivo en un archivador, una tabla de archivos y una tabla multimedia

La [tabla File](file-table.md) contiene una lista completa de todos los archivos de origen para la instalación. Los archivos se pueden almacenar en el medio de origen como archivos individuales o comprimirse dentro de [archivos de archivo .](cabinet-files.md) Los números de secuencia de la columna Secuencia de la tabla Archivo, junto con el campo LastSequence de la tabla [Media](media-table.md), especifican el orden de instalación de los archivos y los medios de origen en los que se encuentra cada archivo. Cada registro de la tabla Media identifica el disco de origen que contiene todos los archivos con números de secuencia menores o iguales que el valor mostrado en la columna LastSequence y mayor que el valor LastSequence del disco anterior.

Por ejemplo, suponga que un archivo tiene un número de secuencia de 92 especificado en la columna Secuencia de la tabla Archivo. Para determinar en qué disco de origen reside este archivo, el instalador comprueba en el registro de la tabla Media la entrada con el valor Más pequeño de LastSequence mayor que 92. La columna DiskId es la clave principal de la tabla Media y este campo identifica de forma única el disco de la tabla.

El límite máximo en el número de archivos que se pueden enumerar en la tabla Archivo de un paquete Windows Installer es de 32767 archivos. Para crear un paquete Windows Installer que contenga más archivos, vea [Creación de un paquete grande.](authoring-a-large-package.md)

Los autores de paquetes pueden reducir el tamaño de sus paquetes de instalación comprimiendo los archivos de origen e incluyéndolos en archivos de archivo. La imagen de archivo de origen se puede comprimir, descomprimir o una combinación de ambos tipos. Para obtener más información sobre los orígenes comprimidos y sin comprimir, vea [Orígenes comprimidos y sin comprimir.](compressed-and-uncompressed-sources.md) Los archivos de origen comprimidos deben almacenarse dentro de un archivo de archivador. Los archivos comprimidos dentro de un gabinete tienen sus propios números de secuencia internos. No es necesario que los valores de estos números de secuencia internos coincidan con el valor de los números de secuencia de la tabla File. Sin embargo, la secuencia de los archivos especificados en la tabla File debe ser idéntica a la secuencia real de los archivos dentro de los archivadores. Los números de secuencia de archivos sin comprimir no deben ser únicos. Por ejemplo, si todos los archivos están descomprimidos y residen en un disco, todos los archivos pueden tener el mismo número de secuencia en la tabla Archivo.

En la tabla Multimedia se describe el conjunto de discos que forma el medio de origen para la instalación. La primera entrada de la tabla Media siempre debe tener un 1 en el campo DiskId. Los archivos deben organizarse en los medios de origen de forma que todos los archivos del disco 1 tengan números de secuencia de tabla de archivos menores que los números de secuencia de los archivos del disco 2, y todos los números de secuencia del disco 2 deben ser menores que en el disco 3, y así sucesivamente. Este requisito también se aplica a un disco que contiene orígenes comprimidos y sin comprimir. Por ejemplo, si los orígenes de medios para la instalación se encuentran en dos discos de origen y si el disco 1 contiene archivos sin comprimir y un archivo de archivador, los archivos sin comprimir y los archivos del archivador deben tener números de secuencia menores que el número de secuencia de archivo más pequeño de cualquier archivo almacenado en el disco 2. Si todos los archivos del disco 1 se comprimen en un archivo archivador, se podría crear la tabla Multimedia como se muestra en la tabla siguiente.

[Tabla multimedia](media-table.md) (parcial)



| DiskId | LastSequence | DiskPrompt | Gabinete   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          | mycab.cab | Disco 1      |
| 2      | 10           | 2          |           | Disco 2      |



 

Si algunos archivos del disco 1 se comprimen en un archivador y otros están descomprimidos, la tabla Multimedia podría crearse como se muestra a continuación.

[Tabla multimedia](media-table.md) (parcial)



| DiskId | LastSequence | DiskPrompt | Gabinete   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disco 1      |
| 2      | 10           | 1          | mycab.cab | Disco 1      |
| 3      | 15           | 2          |           | Disco 2      |



 

Tenga en cuenta que la creación en la tabla Multimedia siguiente es incorrecta porque especifica algunos números de secuencia de archivo en el disco 2 que son más pequeños que algunos archivos dentro del archivador del disco 1.

[Tabla multimedia](media-table.md)



| DiskId | LastSequence | DiskPrompt | Gabinete   | VolumeLabel |
|--------|--------------|------------|-----------|-------------|
| 1      | 5            | 1          |           | Disco 1      |
| 2      | 10           | 2          |           | Disco 2      |
| 3      | 15           | 1          | mycab.cab | Disco 1      |



 

Los archivos grandes se pueden dividir entre dos o más archivos archivadores. No puede haber más de 15 archivos en un archivo de archivador que se extiende al siguiente archivo de archivador. Por ejemplo, si tiene tres archivos de gabinete, el primer gabinete puede tener 15 archivos que abarcan el segundo archivo de gabinete y el segundo gabinete puede tener 15 archivos que abarcan el tercer archivo de gabinete. Al agregar un registro a la tabla Archivo para varios archivadores de un archivo, use la primera parte del archivo para especificar el número de secuencia de archivo que especifique en la columna Secuencia.

Las tablas Archivo y Multimedia se pueden crear de la siguiente manera si hay tres archivos, dos archivadores y dos discos. En este ejemplo, c1.cab reside en disk1 y c2.cab reside en disk2. El archivo f2 abarca ambos gabinetes. El c1.cab contiene todo el archivo f1 y la primera parte del archivo f2. El c2.cab contiene la segunda parte de f2 y todo el archivo f3.

[Tabla multimedia](media-table.md) (parcial)



| DiskId | LastSequence | DiskPrompt | Gabinete | VolumeLabel |
|--------|--------------|------------|---------|-------------|
| 1      | 5            | 1          | c1.cab  | Disco 1      |
| 2      | 10           | 2          | c2.cab  | Disco 2      |



 

[Tabla de archivos](file-table.md) (parcial)



| Archivo | Secuencia |
|------|----------|
| f1   | 1        |
| f2   | 2        |
| f3   | 6        |



 

 

 



