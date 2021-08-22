---
title: Directrices de cliente
description: Los desarrolladores de cliente deben usar la siguiente funcionalidad para obtener información sobre los elementos de la interfaz de usuario.
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3cfa9a269d796d7071b2107bba2fde6717f42928b9c9dc8074f94afbdbe15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133948"
---
# <a name="client-guidelines"></a>Directrices de cliente

Los desarrolladores de cliente deben usar la siguiente funcionalidad para obtener información sobre los elementos de la interfaz de usuario:

-   Para obtener una [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para objetos, llame a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromEvent.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   Para examinar y manipular objetos accesibles, use las propiedades y métodos [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
-   Para recibir [WinEvents,](winevents-overview.md)llame a [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) para registrar una función de devolución de llamada de WinEvent para los eventos que son relevantes para la aplicación cliente.

## <a name="in-this-section"></a>En esta sección

-   [Cómo obtienen los clientes los iDs secundarios](how-clients-obtain-child-ids.md)

 

 




