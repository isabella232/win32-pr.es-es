---
description: La acción RegisterClassInfo administra el registro de información de clase COM con el sistema. Usa la tabla AppId.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: Acción RegisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a0983b77c517cb2084b21d6d1500ec9b2a54b45d403c43f65bcc29505e2afe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912895"
---
# <a name="registerclassinfo-action"></a>Acción RegisterClassInfo

La acción RegisterClassInfo administra el registro de información de clase COM con el sistema. Usa la [tabla AppId](appid-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterClassInfo debe ir después de [la acción InstallFiles](installfiles-action.md) y [la acción UnregisterClassInfo.](unregisterclassinfo-action.md)

La secuenciación de las acciones del siguiente grupo está restringida. Si algún subconjunto de estas acciones se produce junto en una tabla de secuencias, debe tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [Anulación del registroMIMEInfo](unregistermimeinfo-action.md)
-   RegisterClassInfo
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, RegisterClassInfo debe ir después [de UnregisterMIMEInfo en](unregistermimeinfo-action.md) la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                          |
|-------|-----------------------------------------------------|
| \[1\] | Identificador de clase GUID del servidor COM registrado. |



 

## <a name="remarks"></a>Comentarios

Si el sistema admite la instalación a petición de servidores OLE, [](class-table.md) RegisterClassInfo registra todas las clases COM de la tabla Clase asociada a una característica seleccionada para instalarse o anunciarse. De lo contrario, esta acción solo registra las clases COM asociadas a una característica seleccionada para la instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedad OLEAdvtSupport**](oleadvtsupport.md)
</dt> </dl>

 

 



