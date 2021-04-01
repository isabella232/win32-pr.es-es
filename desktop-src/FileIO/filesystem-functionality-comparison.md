---
description: Las tablas que enumeran la funcionalidad y las características admiten comparaciones para los cuatro sistemas de archivos de Windows principales, NTFS, exFAT, UDF y FAT32.
ms.assetid: 28cf2805-f1ce-46b4-bf08-a329f67f4d99
title: Comparación de la funcionalidad del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7547e48ff68a8fdab195087904a47a535aa3464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811324"
---
# <a name="file-system-functionality-comparison"></a>Comparación de la funcionalidad del sistema de archivos

En las tablas siguientes se enumeran las comparaciones de funcionalidad y características de las cuatro principales sistemas de archivos de Windows, NTFS, exFAT, UDF y FAT32:

-   [Funcionalidad](#file-system-functionality-comparison)
-   [Límites](#limits)
-   [Registro en diario y registro de cambios](#journaling-and-change-log)
-   [Características de asignación de bloques](#block-allocation-features)
-   [Seguridad](#security)
-   [Compresión](#compression)
-   [Cuotas](#quotas)
-   [Almacén de instancia única](#single-instance-store)
-   [Temas relacionados](#related-topics)

## <a name="functionality"></a>Funcionalidad



| Característica                             | NTFS                           | exFAT          | UDF                           | FAT32                      |
|-------------------------------------|--------------------------------|----------------|-------------------------------|----------------------------|
| Marcas de tiempo de creación<br/>     | Sí<br/>                 | Sí<br/> | Sí<br/>                | Sí<br/>             |
| Marcas de tiempo de último acceso<br/>  | No (vea la siguiente nota)<br/> | Sí<br/> | Sí<br/>                | Sí (solo fecha)<br/> |
| Marcas de tiempo de último cambio<br/>  | Sí<br/>                 | Sí<br/> | Sí<br/>                | Sí<br/>             |
| Últimas marcas de tiempo de archivo<br/> | No<br/>                  | No<br/>  | No<br/>                 | No<br/>              |
| Distingue mayúsculas y minúsculas<br/>           | Sí (opción)<br/>        | No<br/>  | Sí<br/>                | No<br/>              |
| Conservar las mayúsculas y minúsculas<br/>          | Sí<br/>                 | Sí<br/> | Sí<br/>                | Sí<br/>             |
| Vínculos físicos<br/>               | Sí<br/>                 | No<br/>  | Sí<br/>                | No<br/>              |
| Enlaces simbólicos<br/>               | Sí<br/>                 | No<br/>  | No<br/>                 | No<br/>              |
| Archivos dispersos<br/>             | Sí<br/>                 | No<br/>  | Sí<br/>                | No<br/>              |
| Secuencias con nombre<br/>            | Sí<br/>                 | No<br/>  | Sí<br/>                | No<br/>              |
| Oplocks<br/>                  | Sí<br/>                 | Sí<br/> | Sí<br/>                | Sí<br/>             |
| Atributos ampliados<br/>      | Sí<br/>                 | No<br/>  | Sí (solo en disco)<br/> | No<br/>              |
| Flujos de datos alternativos<br/>   | Sí<br/>                 | No<br/>  | Sí<br/>                | No<br/>              |
| Puntos de montaje<br/>             | Sí<br/>                 | No<br/>  | No<br/>                 | No<br/>              |



 

**Windows Server 2003 y Windows XP:** Se actualiza el campo de marca de tiempo de último acceso de NTFS.

## <a name="limits"></a>Límites



| Característica                             | NTFS                                                                                      | exFAT                                                                                     | UDF                                                                                       | FAT32                                                                                     |
|-------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Longitud máxima del nombre del archivo<br/> | 255 caracteres Unicode<br/>                                                         | 255 caracteres Unicode<br/>                                                         | 127 caracteres ASCII Unicode o 254<br/>                                            | 255 caracteres Unicode<br/>                                                         |
| Longitud máxima del nombre de la ruta<br/> | 32.760 caracteres Unicode con cada componente de ruta de acceso con un máximo de 255 caracteres<br/> | 32.760 caracteres Unicode con cada componente de ruta de acceso con un máximo de 255 caracteres<br/> | 32.760 caracteres Unicode con cada componente de ruta de acceso con un máximo de 255 caracteres<br/> | 32.760 caracteres Unicode con cada componente de ruta de acceso con un máximo de 255 caracteres<br/> |
| Tamaño de archivo máximo<br/>        | 2 ^ 64 1 bytes<br/>                                                                   | 2 ^ 64 1 bytes<br/>                                                                   | 2 ^ 64 1 bytes<br/>                                                                   | 4 GiB<br/>                                                                          |
| Tamaño máximo del volumen<br/>      | 16 TB (tamaño de clúster de 4 KB) o 256TB (tamaño de clúster de 64 KB)<br/>                        | 2 ^ 32 1 clústeres (tamaño máximo del clúster = 2 ^ 25 1)<br/>                               | 2 ^ 32 bloques<br/>                                                                    | 2 ^ 32 bloques<br/>                                                                    |



 

## <a name="journaling-and-change-log"></a>Registro en diario y registro de cambios



| Característica                             | NTFS           | exFAT         | UDF           | FAT32         |
|-------------------------------------|----------------|---------------|---------------|---------------|
| Registro en diario solo de metadatos<br/> | Sí<br/> | No<br/> | No<br/> | No<br/> |
| Registro de cambios de archivo<br/>          | Sí<br/> | No<br/> | No<br/> | No<br/> |



 

## <a name="block-allocation-features"></a>Características de asignación de bloques



| Característica                        | NTFS                                                                        | exFAT         | UDF            | FAT32         |
|--------------------------------|-----------------------------------------------------------------------------|---------------|----------------|---------------|
| Empaquetado de colas<br/>        | Sí (los archivos pequeños se hacen residentes en el descriptor de la secuencia de MFT)<br/> | No<br/> | No<br/>  | No<br/> |
| Extents<br/>             | Sí<br/>                                                              | No<br/> | Sí<br/> | No<br/> |
| Tamaño de bloque variable<br/> | No (establecido por el volumen)<br/>                                           | No<br/> | No<br/>  | No<br/> |



 

## <a name="security"></a>Seguridad



| Característica                                  | NTFS                                                 | exFAT               | UDF                 | FAT32         |
|------------------------------------------|------------------------------------------------------|---------------------|---------------------|---------------|
| Seguimiento del propietario del archivo<br/>              | Sí<br/>                                       | No<br/>       | No<br/>       | No<br/> |
| Permisos de archivo POSIX<br/>        | No (disponible en la característica de subsistema POSIX)<br/> | No<br/>       | Sí<br/>      | No<br/> |
| Listas de control de acceso<br/>          | Sí<br/>                                       | No<br/>       | No<br/>       | No<br/> |
| Cifrado de nivel de sistema de archivos<br/> | Sí<br/>                                       | No<br/>       | No<br/>       | No<br/> |
| Suma de comprobación/ECC<br/>                  | No<br/>                                        | Metadatos<br/> | Metadatos<br/> | No<br/> |



 

## <a name="compression"></a>Compresión



| Característica                         | NTFS           | exFAT         | UDF           | FAT32         |
|---------------------------------|----------------|---------------|---------------|---------------|
| Compresión integrada<br/> | Sí<br/> | No<br/> | No<br/> | No<br/> |



 

## <a name="quotas"></a>Cuotas



| Característica                               | NTFS                           | exFAT         | UDF           | FAT32         |
|---------------------------------------|--------------------------------|---------------|---------------|---------------|
| Espacio en disco en el nivel de usuario<br/>      | Sí<br/>                 | No<br/> | No<br/> | No<br/> |
| Espacio en disco en el nivel de directorio<br/> | No (vea la siguiente nota)<br/> | No<br/> | No<br/> | No<br/> |



 

**Nota:**  La característica de cuotas de espacio en disco en el nivel de directorio de NTFS está disponible a través del servidor de archivos Administrador de recursos.

## <a name="single-instance-store"></a>Single-Instance Store



| Característica               | NTFS                           | exFAT         | UDF           | FAT32         |
|-----------------------|--------------------------------|---------------|---------------|---------------|
| Nivel de archivo<br/> | No (vea la siguiente nota)<br/> | No<br/> | No<br/> | No<br/> |



 

**Nota:**  El almacén de instancia única para NTFS está disponible como parte de la característica de almacenamiento de instancia única en Windows Server.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la administración de archivos](about-file-management.md)
</dt> <dt>

[Almacenamiento de instancia única y copia de seguridad de SIS](/windows/desktop/Backup/single-instance-store-and-sis-backup)
</dt> </dl>

 

