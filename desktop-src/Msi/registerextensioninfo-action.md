---
description: La acción RegisterExtensionInfo administra el registro de información relacionada con la extensión con el sistema.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: Acción RegisterExtensionInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652669"
---
# <a name="registerextensioninfo-action"></a>Acción RegisterExtensionInfo

La acción RegisterExtensionInfo administra el registro de información relacionada con la extensión con el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterExtensionInfo debe aparecer después de la acción [InstallFiles](installfiles-action.md) y la acción [UnregisterExtensionInfo](unregisterextensioninfo-action.md) .

La secuenciación de las acciones del grupo siguiente está restringida. Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   RegisterExtensionInfo
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, RegisterExtensionInfo debe aparecer después de [UnregisterMIMEInfo](unregistermimeinfo-action.md) en la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción |
|-------|----------------------------|
| \[1\] | Extensión registrada.      |



 

## <a name="remarks"></a>Observaciones

Si el sistema admite la instalación a petición para los servidores de extensión, RegisterExtensionInfo registra todos los servidores de extensión en la [tabla de extensión](extension-table.md) asociada a las características establecidas para la instalación o el anuncio. De lo contrario, esta acción solo registra los servidores de extensión asociados a las características establecidas en instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedad ShellAdvtSupport**](shelladvtsupport.md)
</dt> </dl>

 

 



