---
description: La mayoría de las extensiones de espacio de nombres son un subconjunto del espacio de nombres del shell.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Mostrar una vista de Self-Contained de una extensión de espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985663"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a>Mostrar una vista de Self-Contained de una extensión de espacio de nombres

La mayoría de las extensiones de espacio de nombres son un subconjunto del espacio de nombres del shell. Cuando se crea un punto de Unión, como se describe en [especificar la ubicación de una extensión de espacio de nombres](nse-junction.md), el explorador de Windows permite a los usuarios navegar dentro y fuera de la extensión de espacio de nombres como cualquier otra carpeta. Sin embargo, también es posible usar el explorador de Windows para mostrar solo el contenido de la extensión de espacio de nombres. Esta opción de presentación se denomina a veces *vista con raíz*. Aunque no se usa habitualmente, las vistas con raíz podrían ser preferibles a las vistas normales de algunos tipos de extensiones.

Con una vista con raíz, se crea una nueva instancia del explorador de Windows que muestra el contenido de la extensión como un espacio de nombres independiente. La vista de árbol de una vista con raíz muestra solo las carpetas que forman parte de la extensión. Los usuarios no pueden navegar desde una vista con raíz hasta otras partes del espacio de nombres del shell.

Las extensiones se implementan de la misma manera para las vistas con raíz que para las vistas normales. La única diferencia radica en la forma en que el explorador de Windows muestra el contenido de la extensión. Incluso es posible tener vistas normales y de raíz de la misma extensión.

Para abrir una vista de una extensión, debe iniciar una instancia de Explorer.exe con una marca/root. Hay varias maneras de iniciar una vista con raíz, en función de la naturaleza de la extensión.

-   [Cómo usar un punto de Unión para abrir una vista con raíz](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [Cómo usar un archivo de acceso directo para abrir una vista con raíz](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [Cómo mostrar una vista raíz de un archivo](how-to-display-a-rooted-view-of-a-file.md)

 

 



