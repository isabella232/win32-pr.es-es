---
description: La acción UnregisterExtensionInfo administra la eliminación de la información relacionada con la extensión del registro del sistema.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Acción UnregisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d069a686c5f0e517a0cc9556634895216dd8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653074"
---
# <a name="unregisterextensioninfo-action"></a>Acción UnregisterExtensionInfo

La acción UnregisterExtensionInfo administra la eliminación de la información relacionada con la extensión del registro del sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción UnregisterExtensionInfo debe aparecer después de la acción [InstallInitialize](installinitialize-action.md) y antes de la acción [RegisterExtensionInfo](registerextensioninfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) debe estar delante de UnregisterExtensionInfo en la secuencia.

La secuenciación de las acciones del grupo siguiente está restringida. Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   UnregisterExtensionInfo
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, UnregisterExtensionInfo debe estar antes de [UnregisterProgIdInfo](unregisterprogidinfo-action.md) en la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Extensión quitada.         |



 

## <a name="remarks"></a>Observaciones

Si el sistema no admite la instalación a petición de servidores de extensión, UnregisterExtensionInfo quita todos los servidores de extensión de la [tabla de extensión](extension-table.md) asociados a una característica desinstalada o a una característica instalada como anunciada desde el registro. De lo contrario, esta acción quita los servidores de extensión asociados a una característica que está seleccionada para quitarse del registro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedad ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



