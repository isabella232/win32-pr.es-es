---
title: Escribir código de evento
description: Escribir código de evento
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Reproductor de Windows Media máscaras, escribir código
- máscaras, escribir código
- events,writing code
- escribir código para máscaras, acerca de
- Reproductor de Windows Media máscaras,eventos
- máscaras, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39c35864151db1671c2f7fa94caea803f0a33cc1082a3ae44082a90f7bddafb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760575"
---
# <a name="writing-event-code"></a>Escribir código de evento

Los eventos se tratan de forma similar a los atributos. Debe proporcionar al evento un valor y el valor es el código que desea ejecutar cuando se produce el evento. La palabra "on" se agrega al frente del nombre del evento; Por ejemplo, el evento click se convertirá en **onclick**.

El valor del evento está entre comillas dobles y comienza con la palabra JScript seguido de dos puntos. El código que quiere ejecutar viene a continuación, seguido de un punto y coma y las comillas dobles de cierre. Por ejemplo, para detener la reproducción cuando el usuario hace clic en un botón, escriba lo siguiente como atributo en el código **del elemento BUTTON:**


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



Si tiene un código que requiere comillas, use comillas simples. Se debe tener cuidado al usar comillas para que estén equilibradas correctamente. Este es un ejemplo del uso de ambos tipos:


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



También puede cambiar los atributos de la máscara al controlar un evento externo. Por ejemplo, para cerrar una vista denominada myView, podría escribir:


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Control de eventos**](handling-events.md)
</dt> </dl>

 

 




