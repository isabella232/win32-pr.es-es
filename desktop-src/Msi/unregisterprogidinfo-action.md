---
description: La acción UnregisterProgIdInfo administra la anulación del registro de la información de OLE ProgId con el sistema.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Acción UnregisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6666e5648cba220dbb9bbc6e2d50c3959c1d73c98f97dcfd8c45cb3de8d94c82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786965"
---
# <a name="unregisterprogidinfo-action"></a>Acción UnregisterProgIdInfo

La acción UnregisterProgIdInfo administra la anulación del registro de la información de OLE ProgId con el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción UnregisterProgIdInfo debe ir después de la acción [InstallInitialize,](installinitialize-action.md) la acción [UnregisterClassInfo,](unregisterclassinfo-action.md) [la acción UnregisterExtensioninfo](unregisterextensioninfo-action.md) y antes de [la acción RegisterProgIdInfo.](registerprogidinfo-action.md)

[RemoveRegistryValues](removeregistryvalues-action.md) debe ir antes de UnregisterProgIdInfo en la secuencia.

La secuenciación de las acciones del siguiente grupo está restringida. Si algún subconjunto de estas acciones se produce junto en una tabla de secuencias, debe tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensioninfo](unregisterextensioninfo-action.md)
-   UnregisterProgIdInfo
-   [Anulación del registroMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, UnregisterProgIdInfo debe ir antes [de UnregisterMIMEInfo en](unregistermimeinfo-action.md) la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                |
|-------|-------------------------------------------|
| \[1\] | Identificador de programa del programa registrado. |



 

## <a name="remarks"></a>Comentarios

La acción UnregisterProgIdInfo quita la información de ProgId del Registro (tabla[ProgId](progid-table.md)) para las características que están conectadas a la información de extensión[(tabla](extension-table.md)de extensiones ) o a la información de clase[(](class-table.md)tabla de clases ) y actualmente están seleccionadas para desinstalarse.

 

 



