---
description: La acción RegisterClassInfo administra el registro de información de clase COM con el sistema. Usa la tabla AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Acción RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069701"
---
# <a name="registerclassinfo-action"></a>Acción RegisterClassInfo

La acción RegisterClassInfo administra el registro de información de clase COM con el sistema. Usa la [tabla AppId](appid-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterClassInfo debe ir después de [la acción InstallFiles](installfiles-action.md) y [la acción UnregisterClassInfo.](unregisterclassinfo-action.md)

La secuenciación de las acciones del siguiente grupo está restringida. Si algún subconjunto de estas acciones se produce conjuntamente en una tabla de secuencias, deben tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   RegisterClassInfo
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, RegisterClassInfo debe ir después de [UnregisterMIMEInfo en](unregistermimeinfo-action.md) la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                          |
|-------|-----------------------------------------------------|
| \[1\] | Identificador de clase GUID del servidor COM registrado. |



 

## <a name="remarks"></a>Observaciones

Si el sistema admite la instalación a petición de servidores OLE, RegisterClassInfo registra todas las clases COM de la tabla [Class](class-table.md) asociada a una característica seleccionada para instalarse o anunciarse. De lo contrario, esta acción solo registra las clases COM asociadas a una característica seleccionada para la instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**OleAdvtSupport, propiedad**](oleadvtsupport.md)
</dt> </dl>

 

 



