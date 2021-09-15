---
title: Crear objetos proxy
description: Además de diseñar clases que implementan métodos y propiedades IAccessible, es posible que los desarrolladores de servidores también necesiten diseñar objetos proxy que supervisen la duración de los objetos accesibles.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466125"
---
# <a name="creating-proxy-objects"></a>Crear objetos proxy

Además de diseñar clases que implementan métodos y propiedades [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) es posible que los desarrolladores de servidores también necesiten diseñar objetos *proxy* que supervisen la duración de los objetos accesibles. Si un objeto accesible en una aplicación está disponible todo el tiempo que se ejecuta la aplicación, no es necesario crear un objeto proxy. Si es posible destruir el objeto accesible mientras se ejecuta la aplicación, debe crear un objeto proxy.

## <a name="in-this-section"></a>En esta sección

-   [¿Qué son los objetos proxy?](what-are-proxy-objects.md)
-   [Por qué se necesitan objetos proxy](why-proxy-objects-are-needed.md)
-   [Consideraciones de diseño para objetos proxy](design-considerations-for-proxy-objects.md)

 

 




