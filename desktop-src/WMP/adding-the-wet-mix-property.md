---
title: Agregar la propiedad de combinación húmeda
description: Agregar la propiedad de combinación húmeda
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Complementos de Media Player de Windows, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- Complementos de procesamiento de señal digital, eco de propiedades de ejemplo
- Complementos DSP, propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, propiedades
- Ejemplo de complemento de DSP de eco, propiedad de combinación húmeda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357127"
---
# <a name="adding-the-wet-mix-property"></a>Agregar la propiedad de combinación húmeda

Debe agregar el código para proporcionar la propiedad adicional para el nivel de efecto.

En la sección [Agregar propiedades al complemento DSP de audio de ejemplo se](adding-properties-to-the-sample-audio-dsp-plug-in.md) proporcionan detalles sobre cómo agregar una nueva propiedad mediante Visual C++. En esta sección se muestra cómo agregar el código manualmente. Esto implica agregar código en los mismos tres lugares en los que se modificó el código para la propiedad tiempo de retraso.

Agregue los prototipos para los \_ métodos Get WETMIX y put \_ WETMIX inmediatamente después de los otros prototipos de método de propiedad en echo. h. Use la sintaxis siguiente:


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



Ahora, agregue la implementación de cada método inmediatamente después de las otras implementaciones de propiedades en echo. cpp. En el ejemplo siguiente se muestra el código de ambos métodos:


```C++
// Property get to retrieve the wet mix value by using the public interface.
STDMETHODIMP CEcho::get_wetmix(double *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_fWetMix;

    return S_OK;
}

// Property put to store the wet mix value by using the public interface.
STDMETHODIMP CEcho::put_wetmix(double newVal)
{
    m_fWetMix = newVal;

    // Calculate m_fDryMix
    m_fDryMix = 1.0 - m_fWetMix;
    
    return S_OK;
}

```



Observe que la implementación de put \_ WETMIX incluye el código para calcular el valor correcto para m \_ fDryMix. Cada vez que se especifica un nuevo valor para m \_ fWetMix, se requiere este cálculo.

Agregue el código siguiente en la definición de interfaz justo después del código para los métodos de retraso en echo. idl:


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Eco de propiedades de ejemplo**](echo-sample-properties.md)
</dt> </dl>

 

 




