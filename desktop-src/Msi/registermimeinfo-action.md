---
description: La acción RegisterMIMEInfo registra información del registro relacionada con MIME con el sistema.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Acción RegisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813646"
---
# <a name="registermimeinfo-action"></a>Acción RegisterMIMEInfo

La acción RegisterMIMEInfo registra información del registro relacionada con MIME con el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterMIMEInfo debe aparecer después de la acción [InstallFiles](installfiles-action.md) , la acción [UnregisterMIMEInfo](unregistermimeinfo-action.md) , la acción [RegisterClassInfo](registerclassinfo-action.md) y la acción [RegisterExtensionInfo](registerextensioninfo-action.md) .

La secuenciación de las acciones del grupo siguiente está restringida. Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   RegisterMIMEInfo

Por ejemplo, RegisterMIMEInfo debe aparecer después de [UnregisterMIMEInfo](unregistermimeinfo-action.md) en la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                   |
|-------|----------------------------------------------|
| \[1\] | Identificador del tipo de contenido MIME registrado.  |
| \[2\] | Extensión asociada al tipo de contenido MIME. |



 

## <a name="remarks"></a>Observaciones

La acción RegisterMIMEInfo registra toda la información de MIME para los servidores de la [tabla MIME](mime-table.md) para la que se ha seleccionado el servidor de clase o el servidor de extensiones correspondiente para su instalación.

 

 



