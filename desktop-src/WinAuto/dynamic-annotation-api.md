---
title: API de anotación dinámica
description: Dynamic Annotation API es una extensión de Microsoft Active Accessibility que permite a los desarrolladores personalizar la compatibilidad de IAccessible existente sin tener que usar técnicas de subclase o ajuste propensas a errores.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994602"
---
# <a name="dynamic-annotation-api"></a>API de anotación dinámica

Dynamic Annotation API es una extensión de Microsoft Active Accessibility que permite a los desarrolladores personalizar la compatibilidad de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existente sin tener que usar técnicas de subclase o ajuste propensas a errores. Este mecanismo también permite a los desarrolladores pasar sugerencias u otra información útil a los servidores proxy de Oleacc.dll.

La anotación dinámica se usa normalmente para corregir o modificar una instancia inexacta de un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) expuesto por un proxy de Oleacc.dll existente. Por ejemplo, puede utilizarlo para invalidar las propiedades de [**nombre**](name-property.md) y [**función**](role-property.md) proporcionadas por el proxy predeterminado, y para proporcionar las propiedades de [**Descripción**](description-property.md) y [**ayuda**](help-property.md) (que es posible que el proxy predeterminado no proporcione).

Con Windows 7, los desarrolladores pueden usar la API de anotación dinámica para anotar las propiedades de automatización de la interfaz de usuario de Microsoft, así como las propiedades de Microsoft Active Accessibility de los objetos de proxy que crea Oleacc.dll para los controles estándar de Windows. Los objetos de proxy de Oleacc.dll atienden a los clientes de Microsoft Active Accessibility y de automatización de la interfaz de usuario.

## <a name="in-this-section"></a>En esta sección

-   [Información general](background-information.md)
-   [Alternativas a la anotación dinámica](alternatives-to-dynamic-annotation.md)
-   [Tipos de anotación dinámica](types-of-dynamic-annotation.md)
-   [Anotación directa](direct-annotation.md)
-   [Anotación de asignación de valores](value-map-annotation.md)
-   [Anotación de servidor](server-annotation.md)
-   [Problemas y limitaciones](issues-and-limitations.md)

 

 




