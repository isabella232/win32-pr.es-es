---
description: La acción UnregisterExtensionInfo administra la eliminación de información relacionada con la extensión del registro del sistema.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Acción UnregisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8dae707bc4dd517402d8a85fb64402637a815f8249d4677f18818c855ba4e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810235"
---
# <a name="unregisterextensioninfo-action"></a>Acción UnregisterExtensionInfo

La acción UnregisterExtensionInfo administra la eliminación de información relacionada con la extensión del registro del sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción UnregisterExtensionInfo debe ir después de [la acción InstallInitialize](installinitialize-action.md) y antes de [la acción RegisterExtensionInfo.](registerextensioninfo-action.md)

[RemoveRegistryValues](removeregistryvalues-action.md) debe ir antes que UnregisterExtensionInfo en la secuencia.

La secuenciación de las acciones del siguiente grupo está restringida. Si algún subconjunto de estas acciones se produce junto en una tabla de secuencia, debe tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   UnregisterExtensionInfo
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, UnregisterExtensionInfo debe ir antes [que UnregisterProgIdInfo en](unregisterprogidinfo-action.md) la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Se ha quitado la extensión.         |



 

## <a name="remarks"></a>Comentarios

Si el sistema no admite la instalación a petición de servidores de extensiones, [](extension-table.md) UnregisterExtensionInfo quita todos los servidores de extensiones de la tabla De extensión asociados a una característica desinstalada o a una característica instalada como se anuncia desde el Registro. De lo contrario, esta acción quita los servidores de extensión asociados a una característica que se selecciona para quitarse del Registro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedad ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



