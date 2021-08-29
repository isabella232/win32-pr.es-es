---
description: La propiedad REBOOT suprime ciertas solicitudes de reinicio del sistema.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Propiedad REBOOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1de2dbba173d40d59be4ece4578267aa1f2829d62f6583c0ce05ef94598fa491
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913045"
---
# <a name="reboot-property"></a>Propiedad REBOOT

La **propiedad REBOOT** suprime ciertas solicitudes de reinicio del sistema. Normalmente, un administrador usa esta propiedad con una serie de instalaciones para instalar varios productos al mismo tiempo con solo un reinicio al final. Para obtener más información, vea [Reinicios del sistema.](system-reboots.md)

Las [acciones ForceReboot](forcereboot-action.md) y [ScheduleReboot](schedulereboot-action.md) informan al instalador de que pida al usuario que reinicie el sistema. El instalador también puede determinar que es necesario reiniciar si hay alguna acción ForceReboot o ScheduleReboot en la secuencia. Por ejemplo, el instalador solicita automáticamente un reinicio si necesita reemplazar los archivos en uso durante la instalación.

Puede suprimir ciertas solicitudes de reinicio estableciendo la **propiedad REBOOT** como se indica a continuación.



| Valor REBOOT   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Force          | Solicite siempre un reinicio al final de la instalación. La interfaz de usuario siempre solicita al usuario una opción para reiniciar al final. Si no hay ninguna interfaz de usuario y no se trata de una instalación de [varios](multiple-package-installations.md)paquetes, el sistema se reinicia automáticamente al final de la instalación. Si se trata de una instalación de varios paquetes, no hay ningún reinicio automático del sistema y el instalador devuelve ERROR \_ SUCCESS \_ REBOOT \_ REQUIRED. |
| Suprimir       | Suprime las solicitudes de reinicio al final de la instalación. El instalador sigue solicitando al usuario una opción para reiniciar durante la instalación cada vez que encuentra la [acción ForceReboot](forcereboot-action.md). Si no hay ninguna interfaz de usuario, el sistema se reinicia automáticamente en cada ForceReboot. Se suprimen los reinicios al final de la instalación (por ejemplo, causados por un intento de instalar un archivo en uso).                                    |
| ReallySuppress | Suprima todos los reinicios y los mensajes de reinicio iniciados por ForceReboot durante la instalación. Suprimir todos los reinicios y los mensajes de reinicio al final de la instalación. Tanto el símbolo del sistema de reinicio como el propio reinicio se suprimen. Por ejemplo, se suprimen los reinicios al final de la instalación, causados por un intento de instalar un archivo en uso.                                                                                                                    |



 

## <a name="remarks"></a>Comentarios

El instalador solo evalúa el primer carácter de la **propiedad REBOOT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte Windows [Installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[**Propiedad REBOOTPROMPT**](rebootprompt.md)
</dt> <dt>

[Reinicios del sistema](system-reboots.md)
</dt> </dl>

 

 




