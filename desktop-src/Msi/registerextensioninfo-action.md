---
description: La acción RegisterExtensionInfo administra el registro de información relacionada con la extensión con el sistema.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Acción RegisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0541fc512c2300b0cb37f4a23305a3d312a4e60208890507fb7c6112e00c94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519385"
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



 

## <a name="remarks"></a>Comentarios

Si el sistema admite la instalación a petición para los servidores [](extension-table.md) de extensiones, RegisterExtensionInfo registra todos los servidores de extensiones en la tabla De extensión asociada a las características establecidas para la instalación o el anuncio. De lo contrario, esta acción solo registra los servidores de extensión asociados a las características establecidas en la instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedad ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



