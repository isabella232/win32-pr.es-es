---
description: La acción UnregisterMIMEInfo anula el registro de la información del Registro relacionada con MIME del sistema. La acción anula el registro de la información MIME de los servidores de la tabla MIME para la que la característica correspondiente está seleccionada actualmente para desinstalarse.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Acción UnregisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e03ea1c50aa543615edc0ed875bd83b3338cdb261d09e01232e0fe76f7aa51ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810145"
---
# <a name="unregistermimeinfo-action"></a>Acción UnregisterMIMEInfo

La acción UnregisterMIMEInfo anula el registro de la información del Registro relacionada con MIME del sistema. La acción anula el registro de la información MIME de los servidores de la tabla [MIME](mime-table.md) para la que la característica correspondiente está seleccionada actualmente para desinstalarse.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción UnregisterMIMEInfo debe ir después de la acción [InstallInitialize,](installinitialize-action.md) la acción [UnregisterClassInfo,](unregisterclassinfo-action.md) [la acción UnregisterExtensionInfo](unregisterextensioninfo-action.md) y antes de [la acción RegisterMIMEInfo.](registermimeinfo-action.md)

[RemoveRegistryValues](removeregistryvalues-action.md) debe ir antes de UnregisterMIMEInfo en la secuencia.

La secuenciación de las acciones del siguiente grupo está restringida. Si algún subconjunto de estas acciones se produce junto en una tabla de secuencia, debe tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   Anulación del registroMIMEInfo
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, UnregisterMIMEInfo debe ir antes [que RegisterExtensionInfo en](registerextensioninfo-action.md) la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador del tipo de contenido MIME no registrado. |
| \[2\] | Extensión asociada al tipo de contenido MIME.  |



 

 

 



