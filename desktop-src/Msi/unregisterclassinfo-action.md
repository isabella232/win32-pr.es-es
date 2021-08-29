---
description: La acción UnregisterClassInfo administra la eliminación de información de clase COM del registro del sistema. Usa la tabla AppId.
ms.assetid: 579a69ee-92cd-4d4c-a007-998ec042f9fc
title: Acción UnregisterClassInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c2116d67231e915adc1c4ad792dfd577c7fa50d4982c526f0c3f1b14b8abe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810255"
---
# <a name="unregisterclassinfo-action"></a>Acción UnregisterClassInfo

La acción UnregisterClassInfo administra la eliminación de información de clase COM del registro del sistema. Usa la [tabla AppId](appid-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción UnregisterClassInfo debe ir después de [la acción InstallInitialize](installinitialize-action.md) y antes de [la acción RegisterClassInfo.](registerclassinfo-action.md)

[RemoveRegistryValues](removeregistryvalues-action.md) debe ir antes que UnregisterClassInfo en la secuencia.

La secuenciación de las acciones del siguiente grupo está restringida. Si algún subconjunto de estas acciones se produce junto en una tabla de secuencia, debe producirse en la misma secuencia relativa que se muestra en la tabla siguiente:

-   UnregisterClassInfo
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [Anulación del registroMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, [RegisterExtensionInfo](registerextensioninfo-action.md) debe ir antes que UnregisterClassInfo en la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción      |
|-------|---------------------------------|
| \[1\] | GUID de la clase COM no registrada. |



 

## <a name="remarks"></a>Comentarios

El instalador establece la [**propiedad OLEAdvtSupport**](oleadvtsupport.md) en true cuando se ha actualizado el sistema del usuario actual para que funcione con la instalación a petición a través de COM. Si el sistema no admite la instalación a petición a través de COM, UnregisterClassInfo quita todas las clases COM enumeradas en la tabla Clase asociadas a características o características desinstaladas instaladas como se anuncia desde el registro del sistema. [](class-table.md) De lo contrario, esta acción quita solo las clases COM asociadas a las características seleccionadas para desinstalarse del registro del sistema.

 

 



