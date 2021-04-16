---
description: Información acerca de la administración de archivos.
ms.assetid: cf4e69b9-86dd-43a4-9011-6209fc65f550
title: Acerca de la administración de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe8e5f53a0021d4a6fba90a31698d05971e7bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686824"
---
# <a name="about-file-management"></a>Acerca de la administración de archivos

Los temas siguientes contienen más información acerca de la administración de archivos.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                 | Descripción                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comparación de la funcionalidad del sistema de archivos](filesystem-functionality-comparison.md)<br/>            | Las tablas que enumeran la funcionalidad y las características admiten comparaciones para los cuatro sistemas de archivos de Windows principales, NTFS, exFAT, UDF y FAT32.<br/>                                                                           |
| [Archivos y clústeres](files-and-clusters.md)<br/>                                               | Un *archivo* es una unidad de datos del sistema de archivos a la que un usuario puede tener acceso y administrar.<br/>                                                                                                                              |
| [Crear, eliminar y mantener archivos](creating--deleting--and-maintaining-files.md)<br/> | Funciones que se van a usar para crear, eliminar y mantener archivos.<br/>                                                                                                                                                       |
| [Obtener y establecer información de archivos](obtaining-and-setting-file-information.md)<br/>       | Funciones que se van a usar para obtener y establecer información de archivo.<br/>                                                                                                                                                             |
| [Leer y escribir en archivos](reading-from-and-writing-to-files.md)<br/>                 | Una aplicación Lee y escribe en un archivo mediante las funciones [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)y [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) .<br/> |
| [Vinculación de archivos y directorios](file-and-directory-linking.md)<br/>                               | En el sistema de archivos NTFS se admiten dos tipos de vínculos: [vínculos físicos y uniones](hard-links-and-junctions.md).<br/>                                                                                     |
| [Clonación de bloques](block-cloning.md)<br/>                                                         | Una operación de *clonación de bloques* indica al sistema de archivos que copie un intervalo de bytes de archivo en nombre de una aplicación.<br/>                                                                                                |
| [Compresión y descompresión de archivos](file-compression-and-decompression.md)<br/>               | El sistema de archivos NTFS usa la compresión de Lempel-Ziv, que es un algoritmo de compresión sin pérdida.<br/>                                                                                                                  |
| [Cifrado de archivos](file-encryption.md)<br/>                                                     | El sistema de archivos cifrados (EFS) proporciona protección criptográfica de archivos individuales en volúmenes del sistema de archivos NTFS mediante un sistema de clave pública.<br/>                                                               |
| [Derechos de acceso y seguridad de archivos](file-security-and-access-rights.md)<br/>                     | Dado que los archivos son [objetos protegibles](/windows/desktop/SecAuthZ/securable-objects), el acceso a ellos está regulado por el modelo de control de acceso que rige el acceso a todos los demás objetos protegibles en Windows.<br/>                     |
| [Entrada y salida (e/s)](input-and-output--i-o-.md)<br/>                                       | Windows proporciona la capacidad de realizar operaciones de entrada y salida (e/s) en componentes de almacenamiento ubicados en equipos locales y remotos.<br/>                                                                        |
| [Archivos dispersos](sparse-files.md)<br/>                                                           | La compresión de archivos que contienen principalmente ceros hace un uso eficaz del espacio en disco.<br/>                                                                                                                        |
| [Vínculos simbólicos](symbolic-links.md)<br/>                                                       | Un vínculo simbólico es un objeto del sistema de archivos que apunta a otro objeto del sistema de archivos. El objeto al que apunta se denomina destino.<br/>                                                                          |



 

 

