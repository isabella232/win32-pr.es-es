---
description: Administrar directorios con tabla de entradas de directorio, identificadores de directorio, puntos de reanálisis.
title: Sistemas de archivos locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812518"
---
# <a name="local-file-systems"></a>Sistemas de archivos locales

Un *sistema de archivos* permite a las aplicaciones almacenar y recuperar archivos en dispositivos de almacenamiento. Los archivos se colocan en una estructura jerárquica. El sistema de archivos especifica las convenciones de nomenclatura de los archivos y el formato para especificar la ruta de acceso a un archivo en la estructura de árbol.

Cada sistema de archivos consta de uno o varios controladores y bibliotecas de vínculos dinámicos que definen los formatos de datos y las características del sistema de archivos. Los sistemas de archivos pueden existir en muchos tipos diferentes de dispositivos de almacenamiento, incluidos discos duros, gramolas, discos ópticos extraíbles, unidades de copia de seguridad en cinta y tarjetas de memoria.

Todos los sistemas de archivos compatibles con Windows tienen los siguientes componentes de almacenamiento:

-   Volumen. Un *volumen* es una colección de directorios y archivos.
-   Directorio. Un *directorio* es una colección jerárquica de directorios y archivos.
-   Archivos. Un *archivo* es una agrupación lógica de datos relacionados.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                | Descripción                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Administración de directorios](directory-management.md)<br/>          | Un *directorio* es una colección jerárquica de directorios y archivos. La única restricción del número de archivos que pueden estar contenidos en un único directorio es el tamaño físico del disco en el que se encuentra el directorio.<br/> |
| [Administración de discos](disk-management.md)<br/>                    | Un *disco duro* es un disco rígido dentro de un equipo que almacena y proporciona acceso relativamente rápido a grandes cantidades de datos. Es el tipo de almacenamiento que se usa con más frecuencia con Windows. El sistema también admite medios extraíbles.<br/>    |
| [Administración de archivos](file-management.md)<br/>                    | Un *objeto de archivo* proporciona una representación de un recurso (un dispositivo físico o un recurso ubicado en un dispositivo físico) que se puede administrar mediante el sistema de e/s.<br/>                                                            |
| [NTFS transaccional (TxF)](transactional-ntfs-portal.md)<br/> | NTFS transaccional (TxF) permite realizar operaciones de archivo en un volumen del sistema de archivos NTFS en una transacción.<br/>                                                                                                                 |
| [Administración del volumen](volume-management.md)<br/>                | El nivel más alto de organización en el sistema de archivos es el *volumen*. Un sistema de archivos reside en un volumen.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia técnica de FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))
</dt> <dt>

[Tecnologías de sistemas de archivos](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))
</dt> <dt>

[Referencia técnica de NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

