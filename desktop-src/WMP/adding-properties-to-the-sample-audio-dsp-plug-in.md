---
title: Agregar propiedades al complemento DSP de audio de ejemplo
description: Agregar propiedades al complemento DSP de audio de ejemplo
ms.assetid: 9c6c2a34-4844-476b-8814-a95a236e75bb
keywords:
- Reproductor de Windows Media complementos,DSP de audio
- complementos, DSP de audio
- complementos de procesamiento de señal digital, propiedades de audio
- Complementos de DSP, propiedades de audio
- complementos de DSP de audio, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ab1054631b09997ac986529a641e6ff05ec3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374319"
---
# <a name="adding-properties-to-the-sample-audio-dsp-plug-in"></a>Agregar propiedades al complemento DSP de audio de ejemplo

El código de ejemplo de DSP de audio que genera Reproductor de Windows Media asistente para complementos usa una sola propiedad que representa el factor de escala para el volumen de audio. El complemento puede requerir más de una propiedad. Puede agregar fácilmente propiedades al complemento DSP Visual Studio los pasos siguientes:

-   Defina los métodos en el código de definición de interfaz en el archivo IDL que forma parte del proyecto de código auxiliar de proxy.
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

    

Por último, para que las propiedades puedan ser accesibles para el usuario, querrá realizar cambios en la implementación de la página de propiedades.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de un complemento dsp de audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




