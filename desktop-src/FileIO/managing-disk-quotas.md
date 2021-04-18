---
description: Los administradores pueden controlar la cantidad de datos que cada usuario puede almacenar en un volumen del sistema de archivos NTFS.
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: Administración de cuotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688456"
---
# <a name="managing-disk-quotas"></a>Administración de cuotas de disco

El sistema de archivos NTFS admite *cuotas de disco*, lo que permite a los administradores controlar la cantidad de datos que cada usuario puede almacenar en un volumen del sistema de archivos NTFS. Los administradores pueden configurar opcionalmente el sistema para registrar un evento cuando los usuarios están cerca de su cuota y para denegar más espacio en disco a los usuarios que superan su cuota. Los administradores también pueden generar informes y usar el monitor de eventos para realizar el seguimiento de los problemas de cuota.

Puede determinar si un sistema de archivos admite cuotas de disco llamando a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examinando la marca de bits de **\_ \_ cuotas de volumen de archivo** .

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                   | Descripción                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Administración de las cuotas de disco en el nivel de usuario](user-level-administration-of-disk-quotas.md)<br/>     | Cómo obtener más espacio libre en disco después de superar la asignación de cuota.<br/>                                                                  |
| [Administración de las cuotas de disco en el nivel de sistema](system-level-administration-of-disk-quotas.md)<br/> | El administrador del sistema puede establecer cuotas para usuarios específicos en un volumen. Además, el administrador puede establecer cuotas predeterminadas para el volumen.<br/> |
| [Límites de cuota de disco](disk-quota-limits.md)<br/>                                                   | Describe dos tipos de límites de cuota de disco y cómo se miden los límites de cuota de disco.<br/>                                                      |
| [Interfaces de cuota de disco](disk-quota-interfaces.md)<br/>                                           | Interfaces utilizadas con cuotas de disco.<br/>                                                                                                     |



 

 

 




