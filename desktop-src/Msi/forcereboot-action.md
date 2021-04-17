---
description: La acción ForceReboot solicita al usuario que se reinicie el sistema durante la instalación.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: Acción ForceReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bab474f1faacfbc7684797b7a0b7b74f354d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667792"
---
# <a name="forcereboot-action"></a>Acción ForceReboot

La acción ForceReboot solicita al usuario que se reinicie el sistema durante la instalación. La acción ForceReboot es diferente de la [acción ScheduleReboot](schedulereboot-action.md) en que la acción ScheduleReboot se usa para programar una solicitud de reinicio al final de la instalación.

Si la instalación tiene una interfaz de usuario, el instalador muestra un cuadro de diálogo en cada acción de ForceReboot que solicita al usuario que reinicie el sistema. El usuario debe responder a este mensaje antes de continuar con la instalación. Si la instalación no tiene ninguna interfaz de usuario, el sistema se reiniciará automáticamente en la acción ForceReboot.

Si el instalador determina que se necesita un reinicio, automáticamente solicita al usuario que reinicie al final de la instalación, independientemente de si hay alguna acción de ForceReboot o ScheduleReboot en la secuencia. Por ejemplo, el instalador solicita automáticamente un reinicio si es necesario reemplazar los archivos que se usan durante la instalación.

Para suprimir ciertas solicitudes de reinicio, establezca la propiedad [**reboot**](reboot.md) .

Si el Windows Installer encuentra la acción ForceReboot o [ScheduleReboot](schedulereboot-action.md) durante una [instalación de varios paquetes](multiple-package-installations.md), el instalador se detendrá y revertirá la instalación. Se pueden instalar otros paquetes que pertenezcan a la instalación de varios paquetes que no contengan una acción ForceReboot o ScheduleReboot.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Las siguientes acciones suelen producirse juntas como un grupo en la secuencia de acciones. Se recomienda programar la acción ForceReboot para que aparezca después de este grupo. Si la acción ForceReboot está programada antes de la [acción RegisterProduct](registerproduct-action.md), el instalador necesita de nuevo el origen del paquete de instalación después del reinicio. Por lo tanto, la secuencia preferida para ForceReboot está inmediatamente después de esta secuencia de acción.

-   [RegisterProduct](registerproduct-action.md)
-   [RegisterUser](registeruser-action.md)
-   [PublishProduct](publishproduct-action.md)
-   [PublishFeatures](publishfeatures-action.md)
-   [CreateShortcuts](createshortcuts-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)

La acción ForceReboot debe estar entre [InstallInitialize](installinitialize-action.md) y [InstallFinalize](installfinalize-action.md) en la secuencia de acción de la [tabla InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay mensajes ActionData.

## <a name="remarks"></a>Observaciones

La acción ForceReboot siempre debe usarse con una instrucción condicional de modo que el instalador desencadene un reinicio solo cuando sea necesario. Por ejemplo, un reinicio solo puede ser necesario si se reemplaza un archivo determinado o si se instala un componente determinado. Cada instalación de producto es única y es posible que sea necesaria una acción personalizada para determinar si es necesario reiniciar. Normalmente, la condición de la acción ForceReboot hace uso de la propiedad [**AFTERREBOOT**](afterreboot.md) .

ForceReboot ejecuta operaciones del sistema generadas por acciones anteriores antes de solicitar un reinicio o un reinicio. Por ejemplo, las operaciones del sistema generadas por [InstallFiles](installfiles-action.md) y [WriteRegistryValues](writeregistryvalues-action.md) se ejecutan antes de un reinicio.

La acción ForceReboot escribe una clave del registro que hace que el instalador se inicie después de reiniciar. La ubicación de esta clave es **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reinicios del sistema](system-reboots.md)
</dt> </dl>

 

 



