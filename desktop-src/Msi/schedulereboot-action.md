---
description: Inserte la acción ScheduleReboot en la secuencia de acciones para pedir al usuario que reinicie el sistema al final de la instalación. Use la acción ForceReboot para solicitar un reinicio durante la instalación.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Acción ScheduleReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074303"
---
# <a name="schedulereboot-action"></a>Acción ScheduleReboot

Inserte la acción ScheduleReboot en la secuencia de acciones para pedir al usuario que reinicie el sistema al final de la instalación. Use la [acción ForceReboot para](forcereboot-action.md) solicitar un reinicio durante la instalación.

Si la instalación tiene una interfaz de usuario, el instalador muestra un cuadro de mensaje y un botón al final de la instalación que pregunta si el usuario desea reiniciar el sistema. El usuario debe responder a este aviso antes de completar la instalación. Si la instalación no tiene ninguna interfaz de usuario, el sistema se reinicia automáticamente al final.

Si el instalador determina que es necesario reiniciar, se solicita automáticamente al usuario que se reinicie al final de la instalación, independientemente de si hay o no alguna acción ForceReboot o ScheduleReboot en la secuencia. Por ejemplo, el instalador solicita automáticamente un reinicio si necesita reemplazar los archivos que están en uso durante la instalación.

Puede suprimir ciertas solicitudes de reinicio estableciendo la [**propiedad REBOOT.**](reboot.md)

Si el instalador de Windows encuentra la acción [ForceReboot](forcereboot-action.md) [](multiple-package-installations.md)o ScheduleReboot durante una instalación de varios paquetes, el instalador detendrá y revertirá la instalación. Se pueden instalar otros paquetes que pertenecen a la instalación de varios paquetes, que no contienen una acción ForceReboot o ScheduleReboot.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Observaciones

Por ejemplo, esta acción se puede usar para forzar al instalador a solicitar un reinicio después de instalar los controladores que requieren un reinicio. Si el instalador intenta reemplazar los archivos que están en uso, solicita automáticamente al usuario que se reinicie aunque no se haya usado ScheduleReboot.

La acción ScheduleReboot normalmente se coloca al final de la secuencia, pero se puede insertar en cualquier punto de la secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reinicios del sistema](system-reboots.md)
</dt> </dl>

 

 



