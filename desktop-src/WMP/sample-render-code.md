---
title: Código de representación de ejemplo
description: Código de representación de ejemplo
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- visualizaciones, código de ejemplo
- visualizaciones personalizadas, código de ejemplo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función render, código de ejemplo
- ejemplos, función Render para visualizaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075964"
---
# <a name="sample-render-code"></a>Código de representación de ejemplo

Este es un código de ejemplo que usa la función **Render** para dibujar una línea a través de la pantalla. El alto de la línea se define mediante el valor de la forma de onda.


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



La función de **representación** es donde tiene lugar el trabajo principal del código. Cada vez que Windows Media Player toma una instantánea del audio, llamará a esta función y el código se ejecutará.

Este código realiza las siguientes tareas. Consulte el SDK de la plataforma Microsoft Windows para Windows de 32 bits para obtener más detalles sobre funciones específicas.

## <a name="creating-objects"></a>Crear objetos

Normalmente, se usarán las funciones de dibujo que se incorporan a la interfaz gráfica de visualización de Microsoft Windows (GDI). Debe crear lápices para dibujar líneas y pinceles para rellenar áreas.

Se crea un pincel negro sólido para rellenar el fondo.

Se crea un lápiz sólido para dibujar una línea. El color será el color de primer plano tal como lo define la máscara que va a mostrar la visualización.

## <a name="adding-the-object-to-the-dc"></a>Agregar el objeto al controlador de dominio

Debe agregar el lápiz al contexto de dispositivo (DC). El controlador de dominio es la parte de la memoria en la que se almacenan todos los datos y objetos de dibujo. Esencialmente, el controlador de dominio es el administrador de tráfico de Windows que realiza un seguimiento de todo el gráfico.

Debe *convertir* el objeto Pen que creó y almacenarlo como un lápiz antiguo. Use esta técnica de codificación para todos los lápices nuevos. Esta técnica es necesaria para la programación de 32 bits.

## <a name="filling-in-the-background"></a>Rellenar el fondo

Ahora está listo para dibujar. La función **FillRect** llenará el rectángulo de la ventana, tal como se define en los parámetros de la función de **representación** . El rectángulo se rellena con un pincel negro.

## <a name="getting-audio-data"></a>Obtención de datos de audio

A continuación, el código obtiene algunos datos de audio de Windows Media Player. Mediante el uso de la matriz de forma de onda, puede obtener el valor actual de la energía de audio en el momento en que se tomó la instantánea. En este caso, va a tomar los datos de audio del canal izquierdo. El primer valor de la matriz es el primer 1024th de la instantánea de la alimentación de audio.

Esta información se usará para mostrar una línea cuyo alto coincida con la instantánea de la alimentación de audio.

## <a name="draw-the-line"></a>Dibujar la línea

La línea se dibuja de izquierda a derecha mediante las funciones GDI **MoveToEx** y **lineTo** .

En primer lugar, mueva el lápiz al punto inicial. En este caso, x e y se usan para definir los valores de izquierda a derecha y de arriba a abajo que el usuario verá en la pantalla. X se define mediante el rectángulo PRC y, en concreto, por el valor de PRC->izquierda. Y se define como el valor de los datos de la forma de onda en ese momento.

A continuación, dibuje una línea en el otro lado de la ventana. El punto al que se dibuja la línea es de nuevo un valor x, y. X se define mediante el rectángulo PRC, pero esta vez por PRC->a la derecha. Y sigue estando definido por los datos de la forma de onda y es el mismo que el punto desde el que se inició, porque está dibujando una línea recta de izquierda a derecha.

## <a name="clean-up-everything"></a>Limpie todo

Debe eliminar los objetos que cree. En concreto, debe eliminar todos los pinceles y lápices que cree. Es recomendable eliminar lápices y pinceles cuando termine de utilizarlos.

Si no Los elimina antes de finalizar la implementación de la función de **representación** , la visualización se bloqueará en un minuto o menos. Debe mantener un recuento de los lápices y pinceles y destruir cada uno de ellos. Tenga especial cuidado de no crear lápices dentro de un bucle de código.

Use la técnica de codificación que se proporciona en el ejemplo para destruir los lápices y los pinceles.

-   **Importante** Destruya sus lápices y pinceles.

Cuando haya terminado de limpiar, asegúrese de volver a ser \_ correcto para que Windows Media Player sepa que ha terminado de dibujar. Una vez que termine, el dibujo se transferirá a la ventana, se tomará otra instantánea, la **representación** le pedirá que vuelva a dibujar el código, etc.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de render**](implementing-render.md)
</dt> </dl>

 

 




