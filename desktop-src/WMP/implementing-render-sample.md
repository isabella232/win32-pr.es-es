---
title: Implementación del ejemplo de representación
description: Implementación del ejemplo de representación
ms.assetid: 5791f6ea-ddad-49e6-8c6f-8093592895d4
keywords:
- visualizaciones, muestra brillante
- visualizaciones personalizadas, ejemplo de resplandor
- Guía de programación, visualizaciones
- ejemplos, visualización de resplandor
- Ejemplo de visualización brillante
- visualizaciones, función Render
- visualizaciones personalizadas, función Render
- Función render, ejemplo Glow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dabc816283113a82c1d5d677dfc0ca8e8887d344
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533717"
---
# <a name="implementing-render-sample"></a>Implementación del ejemplo de representación

El código siguiente se usa para implementar la función de **representación** :


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



A continuación se muestra una explicación del código:

Una variable denominada *ColorDelFondo* se usa para el color del resplandor y se declara con **COLORREF**. Todos los colores deben usar el tipo de datos **COLORREF** .

Se utiliza una variable denominada *allevel* para la instantánea de nivel de onda de audio. Este valor dependerá del nivel de energía real en el momento de la instantánea.

La instrucción **Switch** se establece mediante el valor preestablecido que el usuario ha elegido en Windows Media Player. La *opción establecerá el color deseado* (rojo, verde o azul). Sin embargo, el color exacto lo determinará el nivel de energía de audio. Por ejemplo, si se elige el valor preestablecido rojo, el color será un rojo sólido, pero será más claro o más oscuro en función de la forma de onda de audio en el momento de la instantánea. Asegúrese de usar la macro **RBG** para crear el color.

Se crea un pincel denominado *hNewBrush*, que se usa para rellenar el rectángulo *PRC* proporcionado por Windows Media Player. La superficie de dibujo es el contexto de dispositivo *HDC* proporcionado por Windows Media Player.

El pincel se elimina mediante **DeleteObject**. Asegúrese de eliminar siempre los lápices o pinceles que cree.

Una vez finalizado el código de **representación** , Windows Media Player mostrará los gráficos de *HDC* en una ventana determinada por la máscara que se está usando.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**El ejemplo de resplandor**](the-glow-sample.md)
</dt> </dl>

 

 




