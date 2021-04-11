---
description: El administrador del sistema puede establecer cuotas para usuarios específicos en un volumen. Además, el administrador puede establecer cuotas predeterminadas para el volumen.
ms.assetid: e8fa6a7b-f4b9-48af-9538-d41c12b7c3b6
title: Administración de las cuotas de disco en el nivel de sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4987becce54b75f2bc06710dce85500813520f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275572"
---
# <a name="system-level-administration-of-disk-quotas"></a>Administración de las cuotas de disco en el nivel de sistema

El administrador del sistema puede establecer cuotas para usuarios específicos en un volumen. Además, el administrador puede establecer cuotas predeterminadas para el volumen. Un nuevo usuario del volumen recibe la cuota predeterminada a menos que el administrador haya establecido una cuota específicamente para ese usuario.

El administrador puede consultar el nivel de seguimiento y cumplimiento de la cuota (o Estados de cuota), los límites de cuota predeterminados y la información de cuota por usuario. La información de cuota por usuario contiene el límite de cuota máxima del usuario, el umbral de advertencia y el uso de la cuota. El administrador también puede habilitar o deshabilitar la aplicación de cuotas.

Hay tres Estados de cuota, tal como se muestra en la tabla siguiente.



| Estado          | Descripción                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cuota deshabilitada | No se realiza el seguimiento de los cambios de uso de cuota, pero los límites de cuota no se quitan. En este estado, el rendimiento no se ve afectado por las cuotas de disco. Este es el estado predeterminado.                         |
| Cuota de seguimiento  | Se realiza un seguimiento de los cambios de uso de cuota, pero no se aplican los límites de cuota. En este estado, no se genera ningún evento de infracción de cuota y no se produce un error en las operaciones de archivo debido a infracciones de cuota de disco. |
| Cuota aplicada | Se realiza un seguimiento de los cambios de uso de cuota y se aplican los límites de cuota.                                                                                                                           |



 

 

 



