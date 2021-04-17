---
description: Describe dos tipos de límites de cuota de disco y cómo se miden los límites de cuota de disco.
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Límites de cuota de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667700"
---
# <a name="disk-quota-limits"></a>Límites de cuota de disco

El espacio en disco que utiliza cada archivo se cobra directamente al usuario que posee el archivo. El propietario de un archivo se identifica mediante el identificador de seguridad (SID) en la información de seguridad del archivo. El espacio total en disco que se carga a un usuario es la suma de la longitud de todos los flujos de datos. En otras palabras, los flujos de conjuntos de propiedades y los flujos de datos de usuario residentes afectan a la cuota del usuario.

La cuota no se cobra por puntos de reanálisis, descriptores de seguridad u otros metadatos asociados a los archivos. La compresión o descompresión de archivos no afecta al espacio en disco indicado para los archivos. Por lo tanto, la configuración de cuota de un volumen puede compararse con la configuración de otro volumen.

Hay dos tipos de límites de cuota de disco, tal como se muestra en la tabla siguiente.



| Límite                        | Descripción                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Umbral de advertencia<br/> | Puede configurar el sistema para que genere una entrada de archivo de registro del sistema cuando el espacio en disco que se carga al usuario supere este valor.<br/>                                                                                                                                         |
| Cuota máxima<br/>        | Puede configurar el sistema para que genere una entrada de archivo de registro del sistema cuando el espacio en disco que se carga al usuario supere este valor. También puede configurar el sistema para que deniegue espacio en disco adicional al usuario cuando el espacio en disco que se carga al usuario supere este valor.<br/> |



 

El sistema de archivos NTFS crea automáticamente una entrada de cuota de usuario la primera vez que un usuario escribe en el volumen. A las entradas creadas automáticamente se les asignan los valores de umbral de advertencia y límite de cuota máxima predeterminados para el volumen.

 

 




