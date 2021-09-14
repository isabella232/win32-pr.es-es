---
title: Flow de control
description: Flow de control
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
- Función de representación, flujo de programa de visualización
- Función RenderWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170585"
---
# <a name="flow-of-control"></a>Flow de control

Los datos de audio Reproductor de Windows Media continuamente a través de un archivo o una secuencia. Estos datos se pasan a la visualización. Dibuje en una superficie definida y vuelva a pasar esa superficie a Reproductor de Windows Media. Este intercambio se produce varias veces por segundo y, para el usuario, el resultado es una animación animada que se mueve a tiempo a la música.

Esta es la secuencia específica del flujo del programa de visualización:

1.  En un intervalo de tiempo, Reproductor de Windows Media toma una instantánea del audio que se reproduce.
2.  Reproductor de Windows Media proporciona los datos de esa instantánea a la visualización mediante la **función Render** y la **función RenderWindowed.**
3.  Debe escribir código que se ejecutará cuando se llame a **Render** y **RenderWindowed.** El código se dibuja mediante un contexto de dispositivo definido por Reproductor de Windows Media al representar sin ventanas o mediante una ventana que se crea al representar ventanas.
4.  En una región especificada por la máscara actual, Reproductor de Windows Media muestra lo que ha dibujado el código.
5.  Este proceso se repite varias veces por segundo, creando animaciones gráficas a las que se ha pasado el tiempo de la música. Cuando la música deja de reproducirse, la visualización se detiene.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general para desarrolladores**](developer-overview.md)
</dt> </dl>

 

 




