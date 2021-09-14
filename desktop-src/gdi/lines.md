---
description: 'Una línea es un conjunto de píxeles resaltados en una pantalla de trama (o un conjunto de puntos en una página impresa) identificados por dos puntos: un punto inicial y un punto final.'
ms.assetid: 538aa3c3-e13a-40dc-b977-3e353a7e9893
title: Líneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cd678f782567e98d32ab7f8786d5b87aab1918
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072479"
---
# <a name="lines"></a>Líneas

Una línea es un conjunto de píxeles resaltados en una pantalla de trama (o un conjunto de puntos en una página impresa) identificados por dos puntos: un punto inicial y un punto final. El píxel situado en el punto inicial siempre se incluye en la línea y el píxel situado en el punto final siempre se excluye. (Este tipo de línea a veces se denomina inclusivo-exclusivo).

Cuando una aplicación llama a una de las funciones de dibujo de línea, la interfaz del dispositivo gráfico (GDI) o, en algunos casos, un controlador de dispositivo, determina qué píxeles se deben resaltar. GDI es una biblioteca de vínculos dinámicos (DLL) que procesa llamadas de función de gráficos desde una aplicación y pasa esas llamadas a un controlador de dispositivo. Un controlador de dispositivo es un archivo DLL que recibe la entrada de GDI, convierte la entrada en comandos de dispositivo y pasa esos comandos al dispositivo adecuado. GDI usa un analizador diferencial digital (DDA) para determinar el conjunto de píxeles que definen una línea. Un DDA determina el conjunto de píxeles examinando cada punto de la línea e identificando esos píxeles en la superficie de presentación (o puntos en una página impresa) que corresponden a los puntos. En la ilustración siguiente se muestra una línea, su punto inicial, su punto final y los píxeles resaltados mediante un DDA simple.

![ilustración que muestra una cuadrícula de píxeles, puntos iniciales y finales, una línea y sombreado en los píxeles que se encuentran a lo largo de la línea](images/cslcv-01.png)

El DDA más sencillo y más común es el DDA bresenham, o incremental. Una versión modificada de este algoritmo dibuja líneas en Windows. El DDA incremental se destaca por su simplicidad, pero también se destaca por su imprecisión. Dado que redondea al valor entero más cercano, a veces no puede representar la línea original solicitada por la aplicación. El DDA usado por GDI no se redondea al entero más cercano. Como resultado, este nuevo DDA genera una salida que a veces es mucho más cercana en apariencia a la línea original solicitada por la aplicación.

> [!Note]  
> Si una aplicación requiere una salida de línea que no se puede lograr con el nuevo DDA, puede dibujar sus propias líneas llamando a la función [**LineDDA**](/windows/desktop/api/Wingdi/nf-wingdi-linedda) y suministrando un DDA privado [**(LineDDAProc).**](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc) Sin embargo, la **función LineDDA** dibuja líneas mucho más lentas que las funciones de dibujo de líneas. No use esta función dentro de una aplicación si la velocidad es un problema principal.

 

Una aplicación puede usar el nuevo DDA para dibujar líneas únicas y varios segmentos de línea conectados. Una aplicación puede dibujar una sola línea llamando a la [**función LineTo.**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) Esta función dibuja una línea desde la posición actual hasta un punto final especificado, pero sin incluirlo. Una aplicación puede dibujar una serie de segmentos de línea conectados mediante una llamada a la función [**Polyline,**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) que proporciona una matriz de puntos que especifican el punto final de cada segmento de línea. Una aplicación puede dibujar varias series de segmentos de línea conectados separados llamando a la función [**PolyPolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) y suministrando los puntos finales necesarios.

En la ilustración siguiente se muestra la salida de línea creada mediante una llamada a las funciones [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)y [**PolyPolyline.**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)

![ilustración que muestra una línea recta, un cuadro en forma de "l" y dos formas que aparecen tridimensionales](images/cslcv-02.png)

 

 



