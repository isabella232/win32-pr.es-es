---
description: Información sobre la administración de archivos.
ms.assetid: cf4e69b9-86dd-43a4-9011-6209fc65f550
title: Acerca de la administración de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2544d31ecb95029053987a3d64e80f4cdf8c0f3170b3a679b542e145ca262947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766375"
---
# <a name="about-file-management"></a>Acerca de la administración de archivos

Los temas siguientes contienen más información sobre la administración de archivos.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                 | Descripción                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comparación de la funcionalidad del sistema de archivos](filesystem-functionality-comparison.md)<br/>            | Las tablas que muestran la funcionalidad y las características admiten comparaciones para los cuatro sistemas de archivos Windows principales, NTFS, exUF, UDF y FAT32.<br/>                                                                           |
| [Archivos y clústeres](files-and-clusters.md)<br/>                                               | Un *archivo* es una unidad de datos del sistema de archivos a la que un usuario puede acceder y administrar.<br/>                                                                                                                              |
| [Crear, eliminar y mantener archivos](creating--deleting--and-maintaining-files.md)<br/> | Funciones que se usan para crear, eliminar y mantener archivos.<br/>                                                                                                                                                       |
| [Obtención y configuración de la información del archivo](obtaining-and-setting-file-information.md)<br/>       | Funciones que se usarán para obtener y establecer la información del archivo.<br/>                                                                                                                                                             |
| [Leer y escribir en archivos](reading-from-and-writing-to-files.md)<br/>                 | Una aplicación lee y escribe en un archivo mediante las funciones [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx,**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)y [**WriteFileEx.**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)<br/> |
| [Vinculación de archivos y directorios](file-and-directory-linking.md)<br/>                               | Hay dos tipos de vínculos admitidos en el sistema de archivos NTFS: [vínculos duros y uniones](hard-links-and-junctions.md).<br/>                                                                                     |
| [Clonación de bloques](block-cloning.md)<br/>                                                         | Una *operación de clonación* de bloque indica al sistema de archivos que copie un intervalo de bytes de archivo en nombre de una aplicación.<br/>                                                                                                |
| [Compresión y descompresión de archivos](file-compression-and-decompression.md)<br/>               | El sistema de archivos NTFS usa Lempel-Ziv compresión, que es un algoritmo de compresión sin pérdida.<br/>                                                                                                                  |
| [Cifrado de archivos](file-encryption.md)<br/>                                                     | El sistema de archivos cifrado (EFS) proporciona protección criptográfica de archivos individuales en volúmenes del sistema de archivos NTFS mediante un sistema de clave pública.<br/>                                                               |
| [Derechos de acceso y seguridad de archivos](file-security-and-access-rights.md)<br/>                     | Dado que los archivos [son objetos](/windows/desktop/SecAuthZ/securable-objects)protegibles, el acceso a ellos está regulado por el modelo de control de acceso que rige el acceso a todos los demás objetos protegibles de Windows.<br/>                     |
| [Entrada y salida (E/S)](input-and-output--i-o-.md)<br/>                                       | Windows permite realizar operaciones de entrada y salida (E/S) en componentes de almacenamiento ubicados en equipos locales y remotos.<br/>                                                                        |
| [Archivos dispersos](sparse-files.md)<br/>                                                           | La compresión de archivos de archivos que contienen principalmente ceros hace un uso eficaz del espacio en disco.<br/>                                                                                                                        |
| [Vínculos simbólicos](symbolic-links.md)<br/>                                                       | Un vínculo simbólico es un objeto del sistema de archivos que apunta a otro objeto del sistema de archivos. El objeto al que se apunta se denomina destino.<br/>                                                                          |



 

 

