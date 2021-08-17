---
title: Crear objetos proxy
description: Además de diseñar clases que implementan métodos y propiedades IAccessible, es posible que los desarrolladores de servidores también necesiten diseñar objetos proxy que supervisen la duración de los objetos accesibles.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49abceb3b38b4495d871605634c8f95353c35b4b6bcd0c54dda374c75572fbea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133898"
---
# <a name="creating-proxy-objects"></a>Crear objetos proxy

Además de diseñar clases que implementan métodos y propiedades [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) es posible que los desarrolladores de servidores también necesiten diseñar objetos *proxy* que supervisen la duración de los objetos accesibles. Si un objeto accesible en una aplicación está disponible todo el tiempo que se ejecuta la aplicación, no es necesario crear un objeto proxy. Si es posible destruir el objeto accesible mientras se ejecuta la aplicación, debe crear un objeto proxy.

## <a name="in-this-section"></a>En esta sección

-   [¿Qué son los objetos proxy?](what-are-proxy-objects.md)
-   [Por qué se necesitan objetos proxy](why-proxy-objects-are-needed.md)
-   [Consideraciones de diseño para objetos proxy](design-considerations-for-proxy-objects.md)

 

 




