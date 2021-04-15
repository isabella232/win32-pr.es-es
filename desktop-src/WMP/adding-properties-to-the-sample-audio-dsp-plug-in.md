---
title: Agregar propiedades al complemento DSP de audio de ejemplo
description: Agregar propiedades al complemento DSP de audio de ejemplo
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- Complementos de Windows Media Player, audio DSP
- complementos, DSP de audio
- Complementos de procesamiento de señal digital, propiedades de audio
- Complementos DSP, propiedades de audio
- Complementos DSP de audio, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ab1054631b09997ac986529a641e6ff05ec3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695313"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a>Agregar propiedades al complemento DSP de audio de ejemplo

El código de ejemplo de DSP de audio que genera el Asistente para complementos de Windows Media Player usa una única propiedad que representa el factor de escala para el volumen de audio. El complemento puede requerir más de una propiedad. Puede agregar fácilmente propiedades al complemento DSP en Visual Studio siguiendo estos pasos:

-   Defina los métodos en el código de definición de interfaz en el archivo IDL que forma parte del proyecto proxy-stub.
    -   Agregue las implementaciones de método al archivo CPP principal del proyecto:

    ```C++
    STDMETHODIMP CYourProject::get_color(COLORREF *pColor)
    {
        if ( NULL == pColor )
        {
            return E_POINTER;
        }

        *pColor = m_Color;

        return S_OK;
    }

    STDMETHODIMP CYourProject::put_color(COLORREF newColor)
    {
        m_Color = newColor;
        
        return S_OK;
    }
    
    ```

    

Por último, para que el usuario pueda tener acceso a las propiedades, querrá realizar cambios en la implementación de la página de propiedades.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementar un complemento de DSP de audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




