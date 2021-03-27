---
description: Una ventana secundaria es una ventana con el \_ estilo WS secundario o WS \_ CHILDWINDOW.
ms.assetid: d8110492-c1b9-4b49-9b34-587adb7c65c9
title: Región de actualización de la ventana secundaria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b92e6cba93c3be253b8ed8616bdcf9301e92494
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001531"
---
# <a name="child-window-update-region"></a>Región de actualización de la ventana secundaria

Una ventana secundaria es una ventana con el \_ estilo WS secundario o WS \_ CHILDWINDOW. Al igual que otros estilos de ventana, las ventanas secundarias reciben mensajes de [**WM \_ Paint**](wm-paint.md) para solicitar la actualización. Cada ventana secundaria tiene una región de actualización, que puede configurar el sistema o la aplicación para generar mensajes de la **\_ pintura de WM** eventuales.

La ventana primaria del elemento secundario afecta a las regiones de actualización y visible de una ventana secundaria. Esto no es cierto para ventanas de otros estilos. El sistema suele establecer la región de actualización de la ventana secundaria cuando establece la región de actualización de la ventana primaria, lo que hace que la ventana secundaria reciba mensajes de [**WM \_ Paint**](wm-paint.md) cuando la ventana primaria las recibe. El sistema limita la ubicación del área visible de la ventana secundaria a dentro del área cliente de la ventana primaria y recorta cualquier parte de la ventana secundaria que se ha despasado fuera de la ventana primaria.

El sistema establece la región de actualización de una ventana secundaria siempre que parte de la región de actualización de la ventana primaria incluya una parte de la ventana secundaria. En tales casos, el sistema envía primero un mensaje de [**\_ dibujo de WM**](wm-paint.md) a la ventana primaria y, a continuación, envía un mensaje a la ventana secundaria, lo que permite que el elemento secundario restaure las partes de la ventana que puede haber dibujado el elemento primario.

El sistema no establece la región de actualización del elemento primario cuando se establece el elemento secundario. Una aplicación no puede generar un mensaje de [**\_ dibujo de WM**](wm-paint.md) para la ventana primaria mediante la invalidación de la ventana secundaria. Del mismo modo, una aplicación no puede generar un mensaje de **\_ dibujo de WM** para el elemento secundario mediante la invalidación de una parte del área de cliente del elemento primario que se encuentra por completo en la ventana secundaria. En tales casos, ninguna ventana recibe un mensaje de **\_ dibujo de WM** .

Una aplicación puede impedir que la región de actualización de una ventana secundaria se establezca cuando el valor de la ventana primaria se establece especificando el \_ estilo WS CLIPCHILDREN al crear la ventana primaria. Cuando se establece este estilo, el sistema excluye las ventanas secundarias del área visible del elemento primario y, por tanto, omite cualquier parte de la región de actualización que pueda contener las ventanas secundarias. Cuando la aplicación pinta en la ventana primaria, se recorta cualquier dibujo que abarque la ventana secundaria, lo que convierte en innecesariamente un mensaje de [**\_ dibujo de WM**](wm-paint.md) posterior a la ventana secundaria.

Las regiones actualizadas y visibles de una ventana secundaria también se ven afectadas por los elementos del mismo nivel de la ventana secundaria. Las ventanas del mismo nivel son ventanas que tienen una ventana primaria común. Si las ventanas relacionadas se superponen, el establecimiento de la región de actualización de una afecta a la región de actualización de otra, lo que hace que se envíen mensajes de [**\_ pintura de WM**](wm-paint.md) a ambas ventanas. Si se compone una ventana de la cadena primaria (una ventana con WX \_ ex \_ composited), las ventanas del mismo nivel reciben mensajes de **\_ pintado de WM** en orden inverso a su posición en el orden Z. Dado esto, el mayor valor de la ventana en el orden Z (en la parte superior) recibe el mensaje de **\_ dibujo de WM** en último lugar y viceversa. Si no se compone una ventana de la cadena primaria, las ventanas del mismo nivel reciben mensajes de **\_ pintura de WM** en orden Z.

Las ventanas del mismo nivel no se recortan automáticamente. Un elemento relacionado puede dibujar sobre otro elemento relacionado superpuesto, incluso si la ventana que está dibujando tiene una posición inferior en el orden Z. Una aplicación puede evitar esto especificando el estilo WS \_ CLIPSIBLINGS al crear las ventanas. Cuando se establece este estilo, el sistema excluye todas las partes de una ventana relacionada superpuesta de la región visible de una ventana si la ventana relacionada superpuesta tiene una posición más alta en el orden Z.

> [!Note]  
> \_ \_ Sus ventanas principales no afectan a las regiones actualizadas y visibles de Windows que tienen el estilo WS Popup o WS POPUPWINDOW.

 

 

 



