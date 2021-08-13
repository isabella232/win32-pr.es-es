---
title: Compatibilidad nativa con IAccessible
description: Oleacc.dll implementa IAccIdentity en nombre de OBJID CLIENT \ 160;Punteros de interfaz IAccessible y sus elementos secundarios \_ de elemento simple inmediatos.
ms.assetid: 98c6d68b-b64d-44d4-93c3-6c7c6732d59d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad499b96c668349cc481efd388a780ba094eff2ef6eb4ae52ab041aabea70fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565059"
---
# <a name="native-iaccessible-support"></a>Compatibilidad nativa con IAccessible

Oleacc.dll implementa [**IAccIdentity en**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) nombre de los punteros de interfaz [**OBJID \_ CLIENT**](object-identifiers.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) y sus elementos secundarios de elemento simple inmediatos. Se devuelve un puntero de interfaz **OBJID \_ CLIENT** **IAccessible** cuando [**WM \_ GETOBJECT**](wm-getobject.md) con *lParam*  =  **OBJID \_ CLIENT** se envía a un **HWND**, que representa el área de cliente de la ventana o el control en su conjunto. El elemento primario de este tipo de puntero de interfaz **IAccessible** normalmente tendrá un rol de [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) y es el objeto **IAccessible** devuelto cuando **WM \_ GETOBJECT** con *lParam*  =  [**OBJID \_ WINDOW**](object-identifiers.md) se envía a un hwnd.

Estos punteros de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suelen producirse cuando se subclasifica un proxy de Oleacc.dll o donde un control personalizado simple (por ejemplo, un contenedor **IAccessible** más un nivel de elementos secundarios simples) proporciona una implementación **nativa de IAccessible.**

Las implementaciones [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativas más complicadas, como donde existe una jerarquía de **IAccessible** o donde se usan los ID de objeto personalizados, deben implementar [**IAccIdentity.**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity)

 

 




