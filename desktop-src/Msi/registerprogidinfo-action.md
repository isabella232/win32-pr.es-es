---
description: La acción RegisterProgIdInfo administra el registro de información de identificador de ensamblado OLE con el sistema.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Acción RegisterProgIdInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652667"
---
# <a name="registerprogidinfo-action"></a>Acción RegisterProgIdInfo

La acción RegisterProgIdInfo administra el registro de información de identificador de ensamblado OLE con el sistema.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RegisterProgIdInfo debe aparecer después de la acción [InstallFiles](installfiles-action.md) , la acción [UnregisterProgIdInfo](unregisterprogidinfo-action.md) , la acción [RegisterClassInfo](registerclassinfo-action.md) y la acción [RegisterExtensionInfo](registerextensioninfo-action.md) .

La secuenciación de las acciones del grupo siguiente está restringida. Si un subconjunto de estas acciones se produce juntos en una tabla de secuencia, deben tener el mismo orden de secuencia relativo que se muestra:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   RegisterProgIdInfo
-   [RegisterMIMEInfo](registermimeinfo-action.md)

Por ejemplo, RegisterProgIdInfo debe aparecer después de [RegisterExtensionInfo](registerextensioninfo-action.md) en la tabla de secuencia.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción                |
|-------|-------------------------------------------|
| \[1\] | Identificador de programa del programa registrado. |



 

## <a name="remarks"></a>Observaciones

La acción RegisterProgIdInfo registra toda la información de ProgId para los servidores que se especifican en la [tabla ProgID](progid-table.md) y para los que se ha seleccionado el servidor de la clase o el servidor de extensiones correspondiente para su instalación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tabla de clases](class-table.md)
</dt> <dt>

[Tabla de extensión](extension-table.md)
</dt> </dl>

 

 



