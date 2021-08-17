---
description: La acción ForceReboot solicita al usuario que reinicie el sistema durante la instalación.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: Acción ForceReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41af6b656222a31ab75c9df3f2fa9f94af415f94d6d0b50010c0b25c5742502
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636076"
---
# <a name="forcereboot-action"></a>Acción ForceReboot

La acción ForceReboot solicita al usuario que reinicie el sistema durante la instalación. La acción ForceReboot es diferente de la acción [ScheduleReboot](schedulereboot-action.md) en que la acción ScheduleReboot se usa para programar un aviso de reinicio al final de la instalación.

Si la instalación tiene una interfaz de usuario, el instalador muestra un cuadro de diálogo en cada acción ForceReboot que solicita al usuario que reinicie el sistema. El usuario debe responder a este aviso antes de continuar con la instalación. Si la instalación no tiene ninguna interfaz de usuario, el sistema se reinicia automáticamente en la acción ForceReboot.

Si el instalador determina que es necesario reiniciar, se solicita automáticamente al usuario que se reinicie al final de la instalación, independientemente de si hay o no alguna acción ForceReboot o ScheduleReboot en la secuencia. Por ejemplo, el instalador solicita automáticamente un reinicio si necesita reemplazar los archivos usados durante la instalación.

Suprimir determinados mensajes de reinicio estableciendo la [**propiedad REBOOT.**](reboot.md)

Si el instalador Windows encuentra la acción ForceReboot o [](multiple-package-installations.md) [ScheduleReboot](schedulereboot-action.md) durante una instalación de varios paquetes, el instalador detendrá y revertirá la instalación. Se pueden instalar otros paquetes que pertenezcan a la instalación de varios paquetes, que no contengan una acción ForceReboot o ScheduleReboot.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Las siguientes acciones normalmente se producen juntas como un grupo en la secuencia de acciones. Se recomienda programar la acción ForceReboot después de este grupo. Si la acción ForceReboot está programada antes de la acción [RegisterProduct](registerproduct-action.md), el instalador requiere de nuevo el origen del paquete de instalación después del reinicio. Por lo tanto, la secuencia preferida para ForceReboot sigue inmediatamente esta secuencia de acciones.

-   [RegisterProduct](registerproduct-action.md)
-   [RegisterUser](registeruser-action.md)
-   [PublishProduct](publishproduct-action.md)
-   [PublishFeatures](publishfeatures-action.md)
-   [CreateShortcuts](createshortcuts-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)

La acción ForceReboot debe estar entre [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md) en la secuencia de acciones de la [tabla InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Mensajes ActionData

No hay ningún mensaje ActionData.

## <a name="remarks"></a>Comentarios

La acción ForceReboot siempre debe usarse con una instrucción condicional de modo que el instalador desencadene un reinicio solo cuando sea necesario. Por ejemplo, solo puede ser necesario reiniciar si se reemplaza un archivo determinado o se instala un componente determinado. Cada instalación de producto es única y puede ser necesaria una acción personalizada para determinar si es necesario reiniciar. La condición de la acción ForceReboot normalmente usa la [**propiedad AFTERREBOOT.**](afterreboot.md)

ForceReboot ejecuta las operaciones del sistema generadas por las acciones anteriores antes de solicitar un reinicio o un reinicio. Por ejemplo, las operaciones del sistema [generadas por InstallFiles](installfiles-action.md) y [WriteRegistryValues](writeregistryvalues-action.md) se ejecutan antes de reiniciar.

La acción ForceReboot escribe una clave del Registro que hace que el instalador se inicie después de reiniciarse. La ubicación de esta clave es **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Reinicios del sistema](system-reboots.md)
</dt> </dl>

 

 



