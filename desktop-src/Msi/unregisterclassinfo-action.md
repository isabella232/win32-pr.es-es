---
description: La acción UnregisterClassInfo administra la eliminación de la información de la clase COM del registro del sistema. Usa la tabla AppId.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Acción UnregisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653076"
---
# <a name="unregisterclassinfo-action"></a>Acción UnregisterClassInfo

La acción UnregisterClassInfo administra la eliminación de la información de la clase COM del registro del sistema. Usa la [tabla AppID](appid-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción UnregisterClassInfo debe aparecer después de la acción [InstallInitialize](installinitialize-action.md) y antes de la acción [RegisterClassInfo](registerclassinfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) debe estar delante de UnregisterClassInfo en la secuencia.

La secuenciación de las acciones del grupo siguiente está restringida. Si un subconjunto de estas acciones se produce en una tabla de secuencia, debe aparecer en la misma secuencia relativa, tal y como se muestra en la tabla siguiente:

-   UnregisterClassInfo
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, [RegisterExtensionInfo](registerextensioninfo-action.md) debe estar antes de UnregisterClassInfo en la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | GUID de clase COM no registrada. |



 

## <a name="remarks"></a>Observaciones

El instalador establece la propiedad [**OLEAdvtSupport**](oleadvtsupport.md) en true cuando el sistema del usuario actual se ha actualizado para que funcione con la instalación a petición a través de com. Si el sistema no admite la instalación a petición a través de COM, UnregisterClassInfo quita todas las clases COM enumeradas en la [tabla de clases](class-table.md) asociada a las características o características desinstaladas que se han instalado como se anuncian desde el registro del sistema. De lo contrario, esta acción solo quita las clases COM asociadas a las características seleccionadas que se van a desinstalar del registro del sistema.

 

 



