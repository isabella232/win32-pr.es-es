---
description: La acción RegisterMIMEInfo registra información del Registro relacionada con MIME con el sistema.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Acción RegisterMIMEInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369f35eab4e6d4228167bfbeda48cf21249ea6a63297f5a9e893b84dcc4ed5bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041745"
---
# <a name="registermimeinfo-action"></a>Acción RegisterMIMEInfo

La acción RegisterMIMEInfo registra información del Registro relacionada con MIME con el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterMIMEInfo debe ir después de la acción [InstallFiles,](installfiles-action.md) la acción [UnregisterMIMEInfo,](unregistermimeinfo-action.md) [la acción RegisterClassInfo](registerclassinfo-action.md) y [la acción RegisterExtensionInfo.](registerextensioninfo-action.md)

La secuenciación de las acciones del siguiente grupo está restringida. Si algún subconjunto de estas acciones se produce junto en una tabla de secuencias, debe tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [Anulación del registroMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   RegisterMIMEInfo

Por ejemplo, RegisterMIMEInfo debe ir después [de UnregisterMIMEInfo en](unregistermimeinfo-action.md) la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                   |
|-------|----------------------------------------------|
| \[1\] | Identificador del tipo de contenido MIME registrado.  |
| \[2\] | Extensión asociada al tipo de contenido MIME. |



 

## <a name="remarks"></a>Comentarios

La acción RegisterMIMEInfo registra toda la información MIME de los servidores de la tabla [MIME](mime-table.md) para la que se ha seleccionado el servidor de clases o el servidor de extensiones correspondientes para instalarse.

 

 



