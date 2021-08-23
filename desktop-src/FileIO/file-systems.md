---
description: Administrar directorios con tabla de entrada de directorio, identificadores de directorio y puntos de rean aproximado.
title: Sistemas de archivos locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77aa77c1029ce4dc19529b148dde1798084acf91afcf6e4435adf8fb2ab266f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696235"
---
# <a name="local-file-systems"></a>Sistemas de archivos locales

Un *sistema de archivos* permite a las aplicaciones almacenar y recuperar archivos en dispositivos de almacenamiento. Los archivos se colocan en una estructura jerárquica. El sistema de archivos especifica convenciones de nomenclatura para los archivos y el formato para especificar la ruta de acceso a un archivo en la estructura de árbol.

Cada sistema de archivos consta de uno o varios controladores y bibliotecas de vínculos dinámicos que definen los formatos de datos y las características del sistema de archivos. Los sistemas de archivos pueden existir en muchos tipos diferentes de dispositivos de almacenamiento, incluidos discos duros, jukeboxes, discos ópticos extraíbles, unidades de copia de seguridad de cinta y tarjetas de memoria.

Todos los sistemas de archivos compatibles Windows tienen los siguientes componentes de almacenamiento:

-   Volúmenes. Un *volumen* es una colección de directorios y archivos.
-   Directorios. Un *directorio* es una colección jerárquica de directorios y archivos.
-   Archivos. Un *archivo* es una agrupación lógica de datos relacionados.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                | Descripción                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Administración de directorios](directory-management.md)<br/>          | Un *directorio* es una colección jerárquica de directorios y archivos. La única restricción en el número de archivos que se pueden contener en un único directorio es el tamaño físico del disco en el que se encuentra el directorio.<br/> |
| [Administración de discos](disk-management.md)<br/>                    | Un *disco duro* es un disco rígido dentro de un equipo que almacena y proporciona acceso relativamente rápido a grandes cantidades de datos. Es el tipo de almacenamiento que se usa con más frecuencia con Windows. El sistema también admite medios extraíbles.<br/>    |
| [Administración de archivos](file-management.md)<br/>                    | Un *objeto de* archivo proporciona una representación de un recurso (ya sea un dispositivo físico o un recurso ubicado en un dispositivo físico) que el sistema de E/S puede administrar.<br/>                                                            |
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

 

