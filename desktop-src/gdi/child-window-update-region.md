---
description: Una ventana secundaria es una ventana con el estilo CHILD \_ o WS \_ CHILDWINDOW de WS.
ms.assetid: d8110492-c1b9-4b49-9b34-587adb7c65c9
title: Región de actualización de ventana secundaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf702855e506424a08e5be6c6b0cfe514035f1c54348306475140fb7fc440a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105900"
---
# <a name="child-window-update-region"></a>Región de actualización de ventana secundaria

Una ventana secundaria es una ventana con el estilo CHILD \_ o WS \_ CHILDWINDOW de WS. Al igual que otros estilos de ventana, las ventanas secundarias [**reciben mensajes \_ WM PAINT**](wm-paint.md) para solicitar la actualización. Cada ventana secundaria tiene una región de actualización, que el sistema o la aplicación pueden establecer para generar mensajes **WM \_ PAINT** finales.

Las regiones visibles y de actualización de una ventana secundaria se ven afectadas por la ventana primaria del elemento secundario. esto no es cierto para ventanas de otros estilos. A menudo, el sistema establece la región de actualización de la ventana secundaria cuando establece la región de actualización de la ventana primaria, lo que hace que la ventana secundaria reciba mensajes [**\_ WM PAINT**](wm-paint.md) cuando la ventana primaria los recibe. El sistema limita la ubicación de la región visible de la ventana secundaria a dentro del área de cliente de la ventana primaria y recorta cualquier parte de la ventana secundaria que se mueve fuera de la ventana primaria.

El sistema establece la región de actualización de una ventana secundaria siempre que una parte de la región de actualización de la ventana primaria incluya una parte de la ventana secundaria. En tales casos, el sistema envía primero un mensaje [**\_ WM PAINT**](wm-paint.md) a la ventana primaria y, a continuación, envía un mensaje a la ventana secundaria, lo que permite al elemento secundario restaurar cualquier parte de la ventana que el elemento primario pueda haber dibujado.

El sistema no establece la región de actualización del elemento primario cuando se establece el elemento secundario. Una aplicación no puede generar un [**mensaje \_ WM PAINT**](wm-paint.md) para la ventana primaria invalidando la ventana secundaria. De forma similar, una aplicación no puede generar un mensaje **\_ WM PAINT** para el elemento secundario invalidando una parte del área de cliente del elemento primario que se encuentra completamente debajo de la ventana secundaria. En tales casos, ninguna ventana recibe un **mensaje \_ WM PAINT.**

Una aplicación puede impedir que se establezca la región de actualización de una ventana secundaria cuando se establece la ventana primaria especificando el estilo CLIPCHILDREN de WS al crear \_ la ventana primaria. Cuando se establece este estilo, el sistema excluye las ventanas secundarias de la región visible del elemento primario y, por tanto, omite cualquier parte de la región de actualización que pueda contener las ventanas secundarias. Cuando la aplicación pinta en la ventana primaria, se recorta cualquier dibujo que cubriría la ventana secundaria, lo que hace innecesario un mensaje [**WM \_ PAINT**](wm-paint.md) posterior a la ventana secundaria.

La actualización y las regiones visibles de una ventana secundaria también se ven afectadas por los elementos del mismo nivel de la ventana secundaria. Las ventanas del mismo nivel son las ventanas que tienen una ventana primaria común. Si las ventanas del mismo nivel se superponen, establecer la región de actualización para una afecta a la región de actualización de otra, lo que hace que los [**mensajes \_ WM PAINT**](wm-paint.md) se envíen a ambas ventanas. Si se compone una ventana de la cadena primaria (una ventana con WX EX COMPOSITED), las ventanas del mismo nivel reciben mensajes WM PAINT en el orden inverso de su posición en el \_ \_ orden Z. **\_** Dado esto, la ventana más alta en el orden Z (en la parte superior) recibe su mensaje **\_ WM PAINT** en último lugar y viceversa. Si no se compone una ventana de la cadena primaria, las ventanas del mismo nivel reciben **mensajes WM \_ PAINT** en orden Z.

Las ventanas del mismo nivel no se recortan automáticamente. Un elemento relacionado puede dibujar sobre otro elemento relacionado superpuesto incluso si la ventana que está dibujando tiene una posición inferior en el orden Z. Una aplicación puede evitar esto especificando el estilo WS \_ CLIPSIBLINGS al crear las ventanas. Cuando se establece este estilo, el sistema excluye todas las partes de una ventana del mismo nivel superpuesta de la región visible de una ventana si la ventana del mismo nivel superpuesta tiene una posición superior en el orden Z.

> [!Note]  
> Las ventanas primarias no afectan a las regiones de actualización y visibles de las ventanas que tienen el estilo POPUP de WS o \_ WS \_ POPUPWINDOW.

 

 

 



