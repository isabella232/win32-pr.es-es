---
description: Inserte la acción ScheduleReboot en la secuencia de acciones para solicitar al usuario que se reinicie el sistema al final de la instalación. Use la acción ForceReboot para solicitar un reinicio durante la instalación.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Acción ScheduleReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909814"
---
# <a name="schedulereboot-action"></a>Acción ScheduleReboot

Inserte la acción ScheduleReboot en la secuencia de acciones para solicitar al usuario que se reinicie el sistema al final de la instalación. Use la [acción ForceReboot](forcereboot-action.md) para solicitar un reinicio durante la instalación.

Si la instalación tiene una interfaz de usuario, el instalador muestra un cuadro de mensaje y un botón al final de la instalación preguntándole si el usuario desea reiniciar el sistema. El usuario debe responder a este mensaje antes de completar la instalación. Si la instalación no tiene ninguna interfaz de usuario, el sistema se reiniciará automáticamente al final.

Si el instalador determina que es necesario reiniciar, solicita automáticamente al usuario que reinicie al final de la instalación, si hay alguna acción ForceReboot o ScheduleReboot en la secuencia. Por ejemplo, el instalador solicita automáticamente un reinicio si es necesario reemplazar los archivos que se están usando durante la instalación.

Puede suprimir determinados mensajes para los reinicios estableciendo la propiedad [**reboot**](reboot.md) .

Si el Windows Installer encuentra la acción [ForceReboot](forcereboot-action.md) o ScheduleReboot durante una [instalación de varios paquetes](multiple-package-installations.md), el instalador se detendrá y revertirá la instalación. Se pueden instalar otros paquetes que pertenezcan a la instalación de varios paquetes que no contengan una acción ForceReboot o ScheduleReboot.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

Por ejemplo, esta acción se puede usar para obligar al instalador a solicitar un reinicio después de instalar los controladores que requieren un reinicio. Si el instalador intenta reemplazar archivos que están en uso, automáticamente solicita al usuario que se reinicie aunque no se haya utilizado ScheduleReboot.

La acción ScheduleReboot normalmente se coloca al final de la secuencia, pero se puede insertar en cualquier punto de la secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reinicios del sistema](system-reboots.md)
</dt> </dl>

 

 



