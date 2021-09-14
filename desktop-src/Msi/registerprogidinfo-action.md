---
description: La acción RegisterProgIdInfo administra el registro de información de OLE ProgId con el sistema.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Acción RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069688"
---
# <a name="registerprogidinfo-action"></a>Acción RegisterProgIdInfo

La acción RegisterProgIdInfo administra el registro de información de OLE ProgId con el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterProgIdInfo debe ir después de la acción [InstallFiles,](installfiles-action.md) la acción [UnregisterProgIdInfo,](unregisterprogidinfo-action.md) [la acción RegisterClassInfo](registerclassinfo-action.md) y [la acción RegisterExtensionInfo.](registerextensioninfo-action.md)

La secuenciación de las acciones del siguiente grupo está restringida. Si algún subconjunto de estas acciones se produce junto en una tabla de secuencias, debe tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [Anulación del registroMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   RegisterProgIdInfo
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, RegisterProgIdInfo debe ir después [de RegisterExtensionInfo en](registerextensioninfo-action.md) la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                |
|-------|-------------------------------------------|
| \[1\] | Identificador de programa del programa registrado. |



 

## <a name="remarks"></a>Observaciones

La acción RegisterProgIdInfo registra toda la información de ProgId de los servidores especificados en la tabla [ProgId](progid-table.md) y para los que se ha seleccionado el servidor de clases o el servidor de extensiones correspondiente para instalarse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla de clases](class-table.md)
</dt> <dt>

[Tabla de extensiones](extension-table.md)
</dt> </dl>

 

 



