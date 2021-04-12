---
description: La acción UnregisterMIMEInfo anula el registro de la información del registro relacionada con MIME del sistema. La acción anula el registro de la información de MIME para los servidores de la tabla MIME para la que está seleccionada actualmente la característica correspondiente para desinstalarla.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: Acción UnregisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c1ca7c0cd12d9ec6236a0c0298ba793713f5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279479"
---
# <a name="unregistermimeinfo-action"></a>Acción UnregisterMIMEInfo

La acción UnregisterMIMEInfo anula el registro de la información del registro relacionada con MIME del sistema. La acción anula el registro de la información de MIME para los servidores de la [tabla MIME](mime-table.md) para la que está seleccionada actualmente la característica correspondiente para desinstalarla.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción UnregisterMIMEInfo debe aparecer después de la acción [InstallInitialize](installinitialize-action.md) , la acción [UnregisterClassInfo](unregisterclassinfo-action.md) , la acción [UnregisterExtensionInfo](unregisterextensioninfo-action.md) y antes de la acción [RegisterMIMEInfo](registermimeinfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) debe estar delante de UnregisterMIMEInfo en la secuencia.

La secuenciación de las acciones del grupo siguiente está restringida. Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   UnregisterMIMEInfo
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, UnregisterMIMEInfo debe estar antes de [RegisterExtensionInfo](registerextensioninfo-action.md) en la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                    |
|-------|-----------------------------------------------|
| \[1\] | Identificador del tipo de contenido MIME no registrado. |
| \[2\] | Extensión asociada al tipo de contenido MIME.  |



 

 

 



