---
description: La acción UnregisterClassInfo administra la eliminación de la información de clase COM del registro del sistema. Usa la tabla AppId.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Acción UnregisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ee701925e07e4f74439efb45da00d430d90304
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171597"
---
# <a name="unregisterclassinfo-action"></a>Acción UnregisterClassInfo

La acción UnregisterClassInfo administra la eliminación de la información de clase COM del registro del sistema. Usa la [tabla AppId](appid-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción UnregisterClassInfo debe ir después de [la acción InstallInitialize](installinitialize-action.md) y antes de [la acción RegisterClassInfo.](registerclassinfo-action.md)

[RemoveRegistryValues](removeregistryvalues-action.md) debe ir antes que UnregisterClassInfo en la secuencia.

La secuenciación de las acciones del siguiente grupo está restringida. Si algún subconjunto de estas acciones se produce conjuntamente en una tabla de secuencias, deben producirse en la misma secuencia relativa como se muestra en la tabla siguiente:

-   UnregisterClassInfo
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, [RegisterExtensionInfo](registerextensioninfo-action.md) debe ir antes que UnregisterClassInfo en la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | GUID de clase COM no registrada. |



 

## <a name="remarks"></a>Observaciones

El instalador establece la [**propiedad OLEAdvtSupport**](oleadvtsupport.md) en true cuando se ha actualizado el sistema del usuario actual para que funcione con instalación a petición a través de COM. Si el sistema no admite la instalación a petición a través de COM, UnregisterClassInfo quita todas las clases COM enumeradas en la tabla Clase asociadas a características desinstaladas o características instaladas como se anuncia desde el registro del sistema. [](class-table.md) De lo contrario, esta acción quita solo las clases COM asociadas a las características seleccionadas para desinstalarse del Registro del sistema.

 

 



