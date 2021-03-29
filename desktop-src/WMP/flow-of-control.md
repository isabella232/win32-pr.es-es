---
title: Flujo de control
description: Flujo de control
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- visualizaciones, flujo de programa
- visualizaciones personalizadas, flujo de programa
- visualizaciones, flujo de control
- visualizaciones personalizadas, flujo de control
- visualizaciones, eventos con tiempo
- visualizaciones personalizadas, eventos con tiempo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- visualizaciones, función RenderWindow
- visualizaciones personalizadas, función RenderWindow
- Función render, flujo de programa de visualización
- RenderWindow función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993988"
---
# <a name="flow-of-control"></a>Flujo de control

Los datos de audio entran en Windows Media Player continuamente a través de un archivo o una secuencia. Esos datos se pasan a la visualización. Dibuja en una superficie definida y pasa esa superficie de nuevo a Windows Media Player. Este intercambio se produce varias veces al segundo y, al usuario, el resultado es una animación agradable que se mueve en el tiempo a la música.

Esta es la secuencia específica del flujo del programa de visualización:

1.  En un intervalo de tiempo, Windows Media Player toma una instantánea del audio que se está reproduciendo.
2.  Windows Media Player proporciona los datos de esa instantánea a la visualización a través de la función **Render** y la función **RenderWindowed** .
3.  Debe escribir código que se ejecutará cuando se llame a **Render** y **RenderWindowed** . El código dibuja mediante el uso de un contexto de dispositivo definido por Windows Media Player cuando se representa sin ventana, o bien mediante una ventana que se crea cuando se representa en la ventana.
4.  En una región especificada por la máscara actual, Windows Media Player muestra lo que dibujó el código.
5.  Este proceso se repite varias veces por segundo, lo que crea animaciones gráficas que se transtimen a la música. Cuando la música deja de reproducirse, la visualización se detiene.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general para desarrolladores**](developer-overview.md)
</dt> </dl>

 

 




