---
description: La acción UnregisterProgIdInfo administra la anulación del registro de información de identificador de programa OLE con el sistema.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: Acción UnregisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff880c1d339fc3db3db50bd34d3afb828f65ec07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913654"
---
# <a name="unregisterprogidinfo-action"></a>Acción UnregisterProgIdInfo

La acción UnregisterProgIdInfo administra la anulación del registro de información de identificador de programa OLE con el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción UnregisterProgIdInfo debe aparecer después de la acción [InstallInitialize](installinitialize-action.md) , la acción [UnregisterClassInfo](unregisterclassinfo-action.md) , la acción [UnregisterExtensioninfo](unregisterextensioninfo-action.md) y antes de la acción [RegisterProgIdInfo](registerprogidinfo-action.md) .

[RemoveRegistryValues](removeregistryvalues-action.md) debe estar delante de UnregisterProgIdInfo en la secuencia.

La secuenciación de las acciones del grupo siguiente está restringida. Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensioninfo](unregisterextensioninfo-action.md)
-   UnregisterProgIdInfo
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, UnregisterProgIdInfo debe estar antes de [UnregisterMIMEInfo](unregistermimeinfo-action.md) en la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                |
|-------|-------------------------------------------|
| \[1\] | Identificador de programa del programa registrado. |



 

## <a name="remarks"></a>Observaciones

La acción UnregisterProgIdInfo quita la información de ProgId del registro ([tabla ProgID](progid-table.md)) para las características que están conectadas a la información de la extensión ([tabla de extensión](extension-table.md)) o a la información de clase (tabla de[clases](class-table.md)) y están seleccionadas actualmente para desinstalarse.

 

 



