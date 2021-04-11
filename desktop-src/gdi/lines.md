---
description: 'Una línea es un conjunto de píxeles resaltados en una pantalla de trama (o un conjunto de puntos de una página impresa) identificados por dos puntos: un punto inicial y un punto final.'
ms.assetid: 538aa3c3-e13a-40dc-b977-3e353a7e9893
title: Líneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cd678f782567e98d32ab7f8786d5b87aab1918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275999"
---
# <a name="lines"></a>Líneas

Una línea es un conjunto de píxeles resaltados en una pantalla de trama (o un conjunto de puntos de una página impresa) identificados por dos puntos: un punto inicial y un punto final. El píxel situado en el punto inicial siempre se incluye en la línea y siempre se excluye el píxel situado en el punto final. (Este tipo de línea a veces se denomina inclusivo-exclusivo).

Cuando una aplicación llama a una de las funciones de dibujo de líneas, la interfaz de dispositivo gráfico (GDI) o, en algunos casos, un controlador de dispositivo, determina qué píxeles deben resaltarse. GDI es una biblioteca de vínculos dinámicos (DLL) que procesa las llamadas de función de gráficos de una aplicación y pasa esas llamadas a un controlador de dispositivo. Un controlador de dispositivo es un archivo DLL que recibe la entrada de GDI, convierte la entrada en comandos de dispositivo y pasa los comandos al dispositivo adecuado. GDI usa un analizador diferencial digital (DDA) para determinar el conjunto de píxeles que definen una línea. DDA determina el conjunto de píxeles mediante el examen de cada punto de la línea y la identificación de esos píxeles en la superficie de la pantalla (o puntos de una página impresa) que corresponden a los puntos. En la ilustración siguiente se muestra una línea, su punto de partida, su punto final y los píxeles resaltados con un DDA simple.

![Ilustración en la que se muestra una cuadrícula de píxeles, puntos inicial y final, una línea y sombreado en los píxeles situados a lo largo de la línea](images/cslcv-01.png)

El DDA más sencillo y más común es Bresenham, o incremental, DDA. Una versión modificada de este algoritmo dibuja líneas en Windows. El DDA incremental se indica por su simplicidad, pero también se indica por su inexactitud. Dado que se redondea al valor entero más cercano, a veces no representa la línea original solicitada por la aplicación. La DDA usada por GDI no se redondea al entero más próximo. Como resultado, este nuevo DDA genera una salida que a veces está mucho más cercana a la línea original solicitada por la aplicación.

> [!Note]  
> Si una aplicación requiere una salida de línea que no se puede lograr con el nuevo DDA, puede dibujar sus propias líneas mediante una llamada a la función [**LineDDA**](/windows/desktop/api/Wingdi/nf-wingdi-linedda) y proporcionar un DDA privado ([**LineDDAProc**](/windows/desktop/api/Wingdi/nc-wingdi-lineddaproc)). Sin embargo, la función **LineDDA** dibuja líneas mucho más lentas que las funciones de dibujo de líneas. No utilice esta función dentro de una aplicación si la velocidad es una preocupación principal.

 

Una aplicación puede usar el nuevo DDA para dibujar líneas individuales y varios segmentos de línea conectados. Una aplicación puede dibujar una sola línea llamando a la función [**lineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) . Esta función dibuja una línea desde la posición actual hasta un punto final especificado, pero sin incluirlo. Una aplicación puede dibujar una serie de segmentos de línea conectados llamando a la función [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) , proporcionando una matriz de puntos que especifican el punto final de cada segmento de línea. Una aplicación puede dibujar varias series separadas de segmentos de línea conectados mediante una llamada a la función de [**polipolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) , proporcionando los puntos finales necesarios.

En la ilustración siguiente se muestra la salida de línea creada mediante una llamada a las funciones [**lineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto), [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)y [**polipolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline) .

![Ilustración en la que se muestra una línea recta, un cuadro con forma de "l" y dos formas que aparecen en tres dimensiones](images/cslcv-02.png)

 

 



