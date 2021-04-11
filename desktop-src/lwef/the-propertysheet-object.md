---
title: El objeto hoja
description: El objeto hoja
ms.assetid: 9d15d198-a4fe-4c05-a7be-0807a179cd9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ae4ded2625440ba34170df605b60287f105800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148790"
---
# <a name="the-propertysheet-object"></a>El objeto hoja

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El objeto [**hoja**](https://www.bing.com/search?q=**PropertySheet**) proporciona varias propiedades que puede usar si desea manipular el carácter relativo a la hoja de propiedades del agente de Microsoft (también conocido como la ventana Opciones de carácter avanzadas).

-   [**Height**](height-property-pso.md)
-   [**Salido**](left-property-pso.md)
-   [**Página**](page-property.md)
-   [**Arriba**](top-property-pso.md)
-   [**Visible**](visible-property.md)
-   [**Width**](width-property-pso.md)

Si consulta las propiedades de [**alto**](height-property-pso.md), [**izquierda**](left-property-pso.md), [**superior**](top-property-pso.md)y [**ancho**](width-property-pso.md) antes de que se haya mostrado alguna vez la hoja de propiedades, sus valores devuelven el valor cero (0). Una vez que se muestran, estas propiedades devuelven la última posición y el tamaño de la ventana (con respecto a la resolución de pantalla actual).

 

 




