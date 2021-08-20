---
title: API de anotación dinámica
description: La API de anotación dinámica es una extensión de Microsoft Active Accessibility que permite a los desarrolladores personalizar la compatibilidad existente con IAccessible sin tener que usar subclases propensas a errores o técnicas de ajuste.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca8b95d1175d4a6bd894e79c55f6798a73165fab2d6e6da40e3b952e68824d50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115325"
---
# <a name="dynamic-annotation-api"></a>API de anotación dinámica

La API de anotación dinámica es una extensión para Microsoft Active Accessibility que permite a los desarrolladores personalizar la compatibilidad existente con [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sin tener que usar técnicas de subclases o ajuste propensas a errores. Este mecanismo también permite a los desarrolladores pasar sugerencias u otra información útil a los Oleacc.dll proxy.

La anotación dinámica se usa normalmente para corregir o modificar una instancia inexacta de un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) expuesto por un proxy Oleacc.dll existente. Por ejemplo, puede usarlo para invalidar [](role-property.md) las propiedades [**Nombre**](name-property.md) y Rol [](description-property.md) proporcionadas [](help-property.md) por el proxy predeterminado y para proporcionar las propiedades Descripción y Ayuda (que puede no proporcionar el proxy predeterminado).

Con Windows 7, los desarrolladores pueden usar la API de anotación dinámica para anotar las propiedades de Microsoft Automatización de la interfaz de usuario, así como las propiedades de Microsoft Active Accessibility de los objetos proxy que Oleacc.dll crea para los controles Windows estándar. Los Oleacc.dll proxy de servicio a los clientes Microsoft Active Accessibility y Automatización de la interfaz de usuario cliente.

## <a name="in-this-section"></a>En esta sección

-   [Información general](background-information.md)
-   [Alternativas a la anotación dinámica](alternatives-to-dynamic-annotation.md)
-   [Tipos de anotación dinámica](types-of-dynamic-annotation.md)
-   [Anotación directa](direct-annotation.md)
-   [Anotación de mapa de valores](value-map-annotation.md)
-   [Anotación del servidor](server-annotation.md)
-   [Problemas y limitaciones](issues-and-limitations.md)

 

 




