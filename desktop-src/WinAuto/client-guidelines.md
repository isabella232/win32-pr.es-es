---
title: Directrices de cliente
description: Los desarrolladores de cliente deben usar la siguiente funcionalidad para obtener información sobre los elementos de la interfaz de usuario.
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242937"
---
# <a name="client-guidelines"></a>Directrices de cliente

Los desarrolladores de cliente deben usar la siguiente funcionalidad para obtener información sobre los elementos de la interfaz de usuario:

-   Para obtener una [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para objetos, llame a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)o [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).
-   Para examinar y manipular objetos accesibles, use las propiedades y métodos [**IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
-   Para recibir [WinEvents,](winevents-overview.md)llame a [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) para registrar una función de devolución de llamada de WinEvent para los eventos que son relevantes para la aplicación cliente.

## <a name="in-this-section"></a>En esta sección

-   [Cómo obtienen los clientes los IDs secundarios](how-clients-obtain-child-ids.md)

 

 




