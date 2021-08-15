---
description: La mayoría de las extensiones de espacio de nombres son un subconjunto del espacio de nombres de Shell.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Mostrar una vista Self-Contained de una extensión de espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ea8ed12d4333ac2c4de7973410a822fefea827be769bbe7ccf754890712e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968844"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a>Mostrar una vista Self-Contained de una extensión de espacio de nombres

La mayoría de las extensiones de espacio de nombres son un subconjunto del espacio de nombres de Shell. Al crear un punto de unión, como se describe en Especificación de la ubicación de una extensión de espacio de nombres, el Explorador de Windows permite [a](nse-junction.md)los usuarios navegar dentro y fuera de la extensión de espacio de nombres como cualquier otra carpeta. Sin embargo, también es posible usar Windows Explorer para mostrar solo el contenido de la extensión de espacio de nombres. Esta opción de visualización se conoce a veces como vista *raíz.* Aunque no se usan normalmente, las vistas con raíz pueden ser preferibles a las vistas normales para algunos tipos de extensiones.

Con una vista raíz, se crea una nueva instancia de Windows Explorer que muestra el contenido de la extensión como un espacio de nombres independiente. La vista de árbol de una vista raíz muestra solo las carpetas que forman parte de la extensión. Los usuarios no pueden navegar desde una vista raíz a otras partes del espacio de nombres de Shell.

Las extensiones se implementan de la misma manera para las vistas raíz que para las vistas normales. La única diferencia radica en la forma en que el Explorador de Windows muestra el contenido de la extensión. Incluso es posible tener vistas normales y con raíz de la misma extensión.

Para abrir una vista de una extensión, debe iniciar una instancia de Explorer.exe con una marca /root. Hay varias maneras diferentes de iniciar una vista raíz, dependiendo de la naturaleza de la extensión.

-   [Cómo usar un punto de unión para abrir una vista raíz](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [Cómo usar un archivo de acceso directo para abrir una vista raíz](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [Cómo mostrar una vista raíz de un archivo](how-to-display-a-rooted-view-of-a-file.md)

 

 



