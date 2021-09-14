---
title: Agregar la propiedad Mezcla mezclada
description: Agregar la propiedad Mezcla mezclada
ms.assetid: 4605d893-8ac0-42fd-a1ac-51430561f174
keywords:
- Reproductor de Windows Media complementos, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, propiedades de ejemplo de eco
- Complementos DE DSP, propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, propiedades
- Ejemplo de complemento DSP de eco, propiedad de combinación con efectos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6af8e7b4857ccbf6b725044575d1b8524aaf50
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890209"
---
# <a name="adding-the-wet-mix-property"></a>Agregar la propiedad Mezcla mezclada

Debe agregar el código para proporcionar la propiedad adicional para el nivel de efecto.

En la sección [Adding Properties to the Sample Audio DSP Plug-in](adding-properties-to-the-sample-audio-dsp-plug-in.md) (Agregar propiedades al complemento DSP de audio de ejemplo) se proporcionan detalles sobre cómo agregar una nueva propiedad mediante Visual C++. En esta sección se muestra cómo agregar el código manualmente. Esto implica agregar código en los mismos tres lugares donde se modificó el código para la propiedad delay time.

Agregue los prototipos para get wetmix y coloque los métodos demezclado inmediatamente después de los otros prototipos de métodos de propiedad \_ \_ en Echo.h. Use la sintaxis siguiente:


```C++
STDMETHOD(get_wetmix)(double *pVal);
STDMETHOD(put_wetmix)(double newVal);

```



Ahora, agregue la implementación para cada método inmediatamente después de las otras implementaciones de propiedad en Echo.cpp. En el ejemplo siguiente se muestra el código para ambos métodos:


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



Observe que la implementación de put \_ wetmix incluye el código para calcular el valor correcto para m \_ fDryMix. Cada vez que se especifica un nuevo valor para m \_ fWetMix, se requiere este cálculo.

Agregue el código siguiente en la definición de interfaz justo después del código para los métodos de retraso en Echo.idl:


```C++
HRESULT get_wetmix([out] double *pVal);
HRESULT put_wetmix([in] double newVal);

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedades de ejemplo de eco**](echo-sample-properties.md)
</dt> </dl>

 

 




