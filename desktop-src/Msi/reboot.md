---
description: La propiedad reboot suprime determinados mensajes para reiniciar el sistema.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Reboot (propiedad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94b08a04f3e95d873f6fc233185ce623cafc25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653733"
---
# <a name="reboot-property"></a>Reboot (propiedad)

La propiedad **REboot** suprime determinados mensajes para reiniciar el sistema. Normalmente, un administrador usa esta propiedad con una serie de instalaciones para instalar varios productos al mismo tiempo con un solo reinicio al final. Para obtener más información, consulte [reinicios del sistema](system-reboots.md).

Las acciones [ForceReboot](forcereboot-action.md) y [ScheduleReboot](schedulereboot-action.md) informan al instalador de que pida al usuario que reinicie el sistema. El instalador también puede determinar que es necesario reiniciar si hay alguna acción de ForceReboot o ScheduleReboot en la secuencia. Por ejemplo, el instalador solicita automáticamente un reinicio si es necesario reemplazar los archivos que se usan durante la instalación.

Puede suprimir determinados mensajes para los reinicios si establece la propiedad **reboot** como se indica a continuación.



| Valor de reinicio   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Force          | Pida siempre un reinicio al final de la instalación. La interfaz de usuario siempre solicita al usuario una opción para reiniciarla al final. Si no hay ninguna interfaz de usuario y no se trata de una [instalación de varios paquetes](multiple-package-installations.md), el sistema se reiniciará automáticamente al final de la instalación. Si se trata de una instalación de varios paquetes, no se reinicia automáticamente el sistema y el instalador devuelve el ERROR \_ se \_ requiere un reinicio correcto \_ . |
| Suprimir       | Suprima los mensajes para un reinicio al final de la instalación. El instalador sigue solicitando al usuario que se reinicie durante la instalación cada vez que encuentra la [acción ForceReboot](forcereboot-action.md). Si no hay ninguna interfaz de usuario, el sistema se reinicia automáticamente en cada ForceReboot. Los reinicios al final de la instalación (por ejemplo, debido a un intento de instalar un archivo en uso) se suprimen.                                    |
| ReallySuppress | Suprimir todos los reinicios y reiniciar los mensajes iniciados por ForceReboot durante la instalación. Suprima todos los reinicios y los mensajes de reinicio al final de la instalación. Se suprimen el mensaje de reinicio y el reinicio. Por ejemplo, los reinicios al final de la instalación, causados por un intento de instalar un archivo en uso, se suprimen.                                                                                                                    |



 

## <a name="remarks"></a>Observaciones

El instalador solo evalúa el primer carácter de la propiedad de **reinicio** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**Propiedad REBOOTPROMPT**](rebootprompt.md)
</dt> <dt>

[Reinicios del sistema](system-reboots.md)
</dt> </dl>

 

 




