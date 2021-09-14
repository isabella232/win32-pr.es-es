---
description: La propiedad REBOOT suprime ciertas solicitudes de reinicio del sistema.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Reboot, propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362318"
---
# <a name="reboot-property"></a>Reboot, propiedad

La **propiedad REBOOT** suprime ciertas solicitudes de reinicio del sistema. Normalmente, un administrador usa esta propiedad con una serie de instalaciones para instalar varios productos al mismo tiempo con un solo reinicio al final. Para obtener más información, vea [Reinicios del sistema.](system-reboots.md)

Las [acciones ForceReboot](forcereboot-action.md) y [ScheduleReboot](schedulereboot-action.md) informan al instalador de que pida al usuario que reinicie el sistema. El instalador también puede determinar que es necesario reiniciar si hay alguna acción ForceReboot o ScheduleReboot en la secuencia. Por ejemplo, el instalador solicita automáticamente un reinicio si necesita reemplazar los archivos en uso durante la instalación.

Puede suprimir determinados avisos de reinicio estableciendo la **propiedad REBOOT** como se indica a continuación.



| Valor REBOOT   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Force          | Solicite siempre un reinicio al final de la instalación. La interfaz de usuario siempre solicita al usuario una opción para reiniciarse al final. Si no hay ninguna interfaz de [](multiple-package-installations.md)usuario y no se trata de una instalación de varios paquetes, el sistema se reinicia automáticamente al final de la instalación. Si se trata de una instalación de varios paquetes, no hay ningún reinicio automático del sistema y el instalador devuelve ERROR \_ SUCCESS \_ REBOOT \_ REQUIRED. |
| Suprimir       | Suprime las solicitudes de reinicio al final de la instalación. El instalador sigue solicitando al usuario una opción para reiniciar durante la instalación cada vez que encuentra la [acción ForceReboot](forcereboot-action.md). Si no hay ninguna interfaz de usuario, el sistema se reinicia automáticamente en cada ForceReboot. Los reinicios al final de la instalación (por ejemplo, causados por un intento de instalar un archivo en uso) se suprimen.                                    |
| ReallySuppress | Suprimir todos los reinicios y las solicitudes de reinicio iniciadas por ForceReboot durante la instalación. Suprimir todos los reinicios y los mensajes de reinicio al final de la instalación. Tanto el símbolo del sistema de reinicio como el propio reinicio se suprimen. Por ejemplo, los reinicios al final de la instalación, causados por un intento de instalar un archivo en uso, se suprimen.                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

El instalador solo evalúa el primer carácter de la **propiedad REBOOT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**Propiedad REBOOTPROMPT**](rebootprompt.md)
</dt> <dt>

[Reinicios del sistema](system-reboots.md)
</dt> </dl>

 

 




