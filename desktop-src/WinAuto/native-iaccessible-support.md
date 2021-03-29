---
title: Compatibilidad con IAccessible nativo
description: Oleacc.dll implementa IAccIdentity en nombre de \_ los punteros de la interfaz de cliente de OBJID \ 160; IAccessible y sus elementos secundarios inmediatos del elemento simple.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606261a642f57c85f3f23a80257b7cdc498b927b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903616"
---
# <a name="native-iaccessible-support"></a>Compatibilidad con IAccessible nativo

Oleacc.dll implementa [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) en nombre de punteros de interfaz  [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del [**\_ cliente OBJID**](object-identifiers.md)y sus elementos secundarios inmediatos del elemento simple. Se devuelve un puntero a la interfaz  **IAccessible** del **\_ cliente de objid** cuando se envía el cliente de Windows, [**WM \_ GETOBJECT**](wm-getobject.md) con *lParam*  =  **\_ OBJID** a un **hWnd**, que representa el área cliente de la ventana o el control en su totalidad. El elemento primario de este puntero de interfaz **IAccessible** normalmente tendrá un rol de [**la \_ \_ ventana sistema de rol**](object-roles.md) y es el objeto **IAccessible** devuelto cuando se envía a un HWND la ventana **WM \_ GETOBJECT** con *lParam*  =  [**OBJID \_**](object-identifiers.md) .

Estos punteros de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suelen producirse cuando se subclase de un proxy Oleacc.dll, o cuando un control personalizado simple (como un **IAccessible** de contenedor más un nivel de elementos secundarios de elemento simple) proporciona una implementación nativa de **IAccessible** .

Las implementaciones de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativas más complicadas, como dónde existe una jerarquía de **IAccessible** s o donde se usan identificadores de objetos personalizados, deben implementar [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) .

 

 




