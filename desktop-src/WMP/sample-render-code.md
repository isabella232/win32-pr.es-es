---
title: Ejemplo de código de representación
description: Ejemplo de código de representación
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- visualizaciones, código de ejemplo
- visualizaciones personalizadas, código de ejemplo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función de representación, código de ejemplo
- samples,Render function for visualizations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476170"
---
# <a name="sample-render-code"></a>Ejemplo de código de representación

Este es un código de ejemplo que usa la **función Render** para dibujar una línea en la pantalla. El alto de la línea se define mediante el valor de forma de onda.


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



La **función Render** es donde tiene lugar el trabajo principal del código. Cada vez Reproductor de Windows Media toma una instantánea del audio, llamará a esta función y se ejecutará el código.

Este código realiza las siguientes tareas. Consulte el SDK de microsoft Windows Platform para aplicaciones de 32 Windows para obtener más detalles sobre funciones específicas.

## <a name="creating-objects"></a>Crear objetos

Normalmente, se usarán las funciones de dibujo que se incluyen con la interfaz gráfica de pantalla (GDI) de Microsoft Windows. Debe crear lápices para dibujar líneas y pinceles para rellenar áreas.

Se crea un pincel negro sólido para rellenar el fondo.

Se crea un lápiz sólido para dibujar una línea. El color será el color de primer plano definido por la máscara que va a mostrar la visualización.

## <a name="adding-the-object-to-the-dc"></a>Agregar el objeto al controlador de dominio

Debe agregar el lápiz al contexto del dispositivo (DC). El controlador de dominio es la parte de memoria en la que se almacenan todos los datos y objetos de dibujo. Básicamente, el controlador de dominio es el administrador de tráfico de ventana que realiza un seguimiento gráfico de todo.

Debe convertir el *objeto* de lápiz que creó y almacenarlo como un lápiz antiguo. Use esta técnica de codificación para todos los lápices nuevos. Esta técnica es necesaria para la programación de 32 bits.

## <a name="filling-in-the-background"></a>Rellenar el fondo

Ya está listo para dibujar. La **función FillRect** rellenará el rectángulo de la ventana, tal como se define en los parámetros de la **función Render.** El rectángulo se rellena con un pincel negro.

## <a name="getting-audio-data"></a>Obtención de datos de audio

A continuación, el código obtiene algunos datos de audio Reproductor de Windows Media. Mediante el uso de la matriz de forma de onda, puede obtener el valor actual de la potencia de audio en el momento en que se tomó la instantánea. En este caso, está tomando los datos de audio del canal izquierdo. El primer valor de la matriz es el primer número 1024 de la instantánea de energía de audio.

Esta información se usará para mostrar una línea cuyo alto coincidirá con la instantánea de energía de audio.

## <a name="draw-the-line"></a>Un hasta aquí

La línea se dibuja de izquierda a derecha mediante las **funciones MoveToEx** y **LineTo** GDI.

En primer lugar, mueva el lápiz al punto inicial. En este caso, x e y se usan para definir los valores de izquierda a derecha y de arriba a abajo que el usuario verá en la pantalla. X se define mediante el rectángulo prc y específicamente por el valor de prc->izquierda. Y se define como el valor de los datos de forma de onda en ese momento.

A continuación, dibuje una línea al otro lado de la ventana. El punto en el que se dibuja la línea es de nuevo un valor x, y. X se define mediante el rectángulo prc, pero esta vez mediante prc->right. Y sigue definido por los datos de forma de onda y es el mismo que el punto desde el que empezó, porque está dibujando una línea recta de izquierda a derecha.

## <a name="clean-up-everything"></a>Limpiar todo

Debe eliminar los objetos que cree. En concreto, debe eliminar todos los pinceles y lápices que cree. Es una buena práctica eliminar lápices y pinceles cuando termine de usarlos.

Si no los elimina antes de finalizar la implementación de la función **Render,** la visualización se bloqueará en un minuto o menos. Debe mantener un recuento de los lápices y pinceles y destruir cada uno de ellos. Tenga especial cuidado de no crear lápices dentro de un bucle de código.

Use la técnica de codificación que se muestra en el ejemplo para destruir los lápices y pinceles.

-   **Importante** ¡Destruya los lápices y pinceles!

Cuando haya terminado de limpiar, asegúrese de devolver S \_ OK para que Reproductor de Windows Media sabe que ha terminado de dibujar. Una vez que haya terminado, el dibujo se transferirá a la ventana, se realizará otra instantánea, **Render** le pedirá al código que se dibuje de nuevo, y así sucesivamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de Render**](implementing-render.md)
</dt> </dl>

 

 




