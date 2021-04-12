---
title: Navegar a otras tiendas en línea
description: Navegar a otras tiendas en línea
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Windows Media Player tiendas en línea, navegar
- tiendas en línea, navegar
- Escriba 2 tiendas en línea, navegación
- navegar por las tiendas en línea de tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8456954d5a7197a054098320b35fb38409ba62
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356676"
---
# <a name="navigating-to-other-online-stores"></a>Navegar a otras tiendas en línea

Puede crear vínculos a otras tiendas en línea que posea o entre vínculos cruzados de tiendas en línea proporcionadas por otros usuarios. Para ello, debe conocer el nombre de la clave de la tienda en línea a la que desea desplazarse.

En el ejemplo de código siguiente se muestra HTML que crea un vínculo para cambiar de la tienda en línea de Proseware a la característica "ServiceTask2" de la tienda Southridge video online:


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



Cuando el usuario hace clic en el vínculo, Windows Media Player solicita al usuario que cambie al almacén de vídeo Southridge. Si el usuario lo permite, el reproductor cambia los almacenes y navega al panel de tareas especificado, anexando los parámetros de la cadena de consulta. Los parámetros de cadena de consulta que se muestran en el ejemplo anterior son parámetros personalizados. Esto significa que la tienda en línea que cambia a debe esperar estos valores y controlarlos. La tienda en línea (y cualquier tienda a la que cambie) puede usar los parámetros de cadena de consulta de la forma que elija.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Desplazarse entre los paneles de tareas de servicio**](navigating-between-service-task-panes.md)
</dt> <dt>

[**Navegación para las tiendas en línea de tipo 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




