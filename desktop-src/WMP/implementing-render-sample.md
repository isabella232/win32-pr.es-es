---
title: Implementación del ejemplo de representación
description: Implementación del ejemplo de representación
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- visualizaciones, ejemplo de glow
- visualizaciones personalizadas, ejemplo de glow
- guía de programación, visualizaciones
- samples,Glow visualization
- Ejemplo de visualización de efecto de brillo
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Render function,Glow sample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c00b57f15655468e5bd0000ccc3b5120e19c2af58d5a1ad6b5493b535c7253f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135578"
---
# <a name="implementing-render-sample"></a>Implementación del ejemplo de representación

El código siguiente se usa para implementar la **función Render:**


```C++
STDMETHODIMP CGlow::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    COLORREF mycolor;
    int mylevel = pLevels->waveform[0][0];
    
    switch (m_nPreset)
    {
    case PRESET_RED:
        {
        mycolor = RGB( mylevel, 0, 0);    
        }
        break;
    case PRESET_GREEN:
        {
        mycolor = RGB( 0, mylevel, 0);        
        }
        break;
    case PRESET_BLUE:
        {
        mycolor = RGB( 0, 0, mylevel);        
        }
        break;
    }

     HBRUSH hNewBrush = ::CreateSolidBrush( mycolor );
    ::FillRect( hdc, prc, hNewBrush );

    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }

    return S_OK;
}

```



Esta es una explicación del código:

Una variable denominada *mycolor* se usa para el color del brillo y se declara con **COLORREF**. Todos los colores deben usar el **tipo de datos COLORREF.**

Se usa una variable denominada *mylevel* para la instantánea de nivel de forma de onda de audio. Este valor dependerá del nivel de energía real en el momento de la instantánea.

La **instrucción switch** se establece mediante el valor preestablecido que el usuario ha elegido en Reproductor de Windows Media. La opción establecerá *mycolor* en el color deseado (rojo, verde o azul). Sin embargo, el color exacto lo determinará el nivel de potencia de audio. Por ejemplo, si se elige el valor preestablecido rojo, el color será un rojo sólido, pero será más claro u oscuro en función de la forma de onda del audio en el momento de la instantánea. Asegúrese de usar la **macro RBG** para crear el color.

Se crea un pincel denominado *hNewBrush* y se usa para rellenar el *rectángulo prc* proporcionado por Reproductor de Windows Media. La superficie de dibujo es el *contexto del dispositivo hdc* proporcionado por Reproductor de Windows Media.

DeleteObject elimina el pincel. Asegúrese siempre de eliminar los lápices o pinceles que cree.

Una vez **finalizado el** código de representación, Reproductor de Windows Media mostrará los gráficos *hdc* en una ventana determinada por la máscara que se usa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**El ejemplo de efecto de brillo**](the-glow-sample.md)
</dt> </dl>

 

 




