---
description: La acción RegisterExtensionInfo administra el registro de información relacionada con la extensión con el sistema.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Acción RegisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069696"
---
# <a name="registerextensioninfo-action"></a>Acción RegisterExtensionInfo

La acción RegisterExtensionInfo administra el registro de información relacionada con la extensión con el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterExtensionInfo debe ir después de [la acción InstallFiles](installfiles-action.md) y [la acción UnregisterExtensionInfo.](unregisterextensioninfo-action.md)

La secuenciación de las acciones del siguiente grupo está restringida. Si algún subconjunto de estas acciones se produce junto en una tabla de secuencias, debe tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [Anulación del registroMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   RegisterExtensionInfo
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, RegisterExtensionInfo debe ir después [de UnregisterMIMEInfo en](unregistermimeinfo-action.md) la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Extensión registrada.      |



 

## <a name="remarks"></a>Observaciones

Si el sistema admite la instalación a petición de los servidores [](extension-table.md) de extensiones, RegisterExtensionInfo registra todos los servidores de extensión en la tabla Extensión asociada a las características establecidas para la instalación o el anuncio. De lo contrario, esta acción solo registra los servidores de extensión asociados a las características establecidas en la instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedad ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



