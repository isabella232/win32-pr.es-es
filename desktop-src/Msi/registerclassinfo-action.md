---
description: La acción RegisterClassInfo administra el registro de información de clase COM con el sistema. Usa la tabla AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Acción RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd916772bc236dfc86df336347514c10d5dfbce7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677762"
---
# <a name="registerclassinfo-action"></a>Acción RegisterClassInfo

La acción RegisterClassInfo administra el registro de información de clase COM con el sistema. Usa la [tabla AppID](appid-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterClassInfo debe aparecer después de la acción [InstallFiles](installfiles-action.md) y la acción [UnregisterClassInfo](unregisterclassinfo-action.md) .

La secuenciación de las acciones del grupo siguiente está restringida. Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   RegisterClassInfo
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, RegisterClassInfo debe aparecer después de [UnregisterMIMEInfo](unregistermimeinfo-action.md) en la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                          |
|-------|-----------------------------------------------------|
| \[1\] | Identificador de clase GUID del servidor COM registrado. |



 

## <a name="remarks"></a>Observaciones

Si el sistema admite la instalación a petición para los servidores OLE, RegisterClassInfo registra todas las clases COM en la [tabla de clases](class-table.md) asociada a una característica seleccionada que se va a instalar o anunciar. De lo contrario, esta acción solo registra las clases COM asociadas a una característica seleccionada para su instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedad OLEAdvtSupport**](oleadvtsupport.md)
</dt> </dl>

 

 



