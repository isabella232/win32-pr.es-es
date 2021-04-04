---
title: Escribir código de evento
description: Escribir código de evento
ms.assetid: ce29aa81-1db8-4aea-a3bd-86c6b559fff7
keywords:
- Máscaras de Media Player de Windows, escribir código
- máscaras, escribir código
- eventos, escribir código
- escribir código para máscaras, acerca de
- Aspectos de Windows Media Player, eventos
- máscaras, eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d994f4ee111795b8fd2b498d26ab65b8bd44dea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076329"
---
# <a name="writing-event-code"></a>Escribir código de evento

Los eventos se tratan de forma similar a los atributos. Debe proporcionar un valor al evento y el valor es el código que desea ejecutar cuando se produce el evento. La palabra "ON" se agrega al principio del nombre del evento; por ejemplo, el evento click pasará a ser **onclick**.

El valor del evento está entre comillas y empieza por la palabra JScript seguido de un signo de dos puntos. El código que desea ejecutar aparece después, seguido de un punto y coma y las comillas dobles de cierre. Por ejemplo, para detener la reproducción cuando el usuario haga clic en un botón, escriba lo siguiente como un atributo en el código del elemento de **botón** :


```C++
onclick = "JScript: player.Controls.Stop() ; "
```



Si tiene un código que requiere comillas, use comillas simples. Se debe tener cuidado al usar comillas para que se equilibren correctamente. Este es un ejemplo del uso de ambos tipos:


```C++
onclick = "JScript: player.URL = 'https://proseware.com/laure.wma' ; "
```



También puede cambiar los atributos de la máscara al controlar un evento externo. Por ejemplo, para cerrar una vista denominada mi vista, podría escribir:


```C++
onclick = "JScript: myView.close() ;"
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Controlar eventos**](handling-events.md)
</dt> </dl>

 

 




