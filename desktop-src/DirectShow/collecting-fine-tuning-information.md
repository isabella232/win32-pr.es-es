---
description: Recopilar información de Fine-Tuning
ms.assetid: 0d9ea896-e0a9-411b-9a10-e366e3686a34
title: Recopilar información de Fine-Tuning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27d191f677acc9306202bce141ef8f6683b43c61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105666109"
---
# <a name="collecting-fine-tuning-information"></a>Recopilar información de Fine-Tuning

Aunque generalmente se espera que las frecuencias de cable sean exactas, las frecuencias de difusión se pueden ajustar o reducir verticalmente varios kHz en la estación de difusión para reducir las posibles interferencias con los canales vecinos.

Cuando el filtro de sintonizador de TV se sintoniza en un canal, busca la señal más precisa. Para guardar esta información en el registro para las operaciones de optimización posteriores, haga lo siguiente:

1.  Llame a [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) para determinar el intervalo de entradas de frecuencia en la tabla de frecuencia actual.
2.  Llame al método de [**\_ canal IAMTuner::p UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) una vez para cada índice de frecuencia del intervalo.
3.  Llame a [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) para guardar la información de ajuste en el registro. La información se almacena en la clave del registro para el espacio de optimización actual.

El siguiente código muestra estos pasos:


```C++
long lMin = 0, lMax = 0;
hr = pTuner->ChannelMinMax(&lMin, &lMax);
if (SUCCEEDED(hr))
{
    for (long i = lMin; i <= lMax; i++)
    {
        pTuner->put_Channel(i, AMTUNER_SUBCHAN_DEFAULT,
            AMTUNER_SUBCHAN_DEFAULT)
    }
    pTuner->StoreAutoTune();
}
```



Con las versiones anteriores del filtro de sintonizador de TV, se recomendó el método [**IAMTVTuner:: AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) para ajustarse. Sin embargo, este método omite cualquier invalidación de frecuencia, por lo que ya no se recomienda su uso. El código siguiente es equivalente al método **AutoTune** , pero funciona correctamente con invalidaciones de frecuencia:


```C++
HRESULT MyAutoTune(IAMTVTuner *pTuner, long lIndex, long *plFoundSignal)
{
    long SignalStrength = AMTUNER_NOSIGNAL;
    HRESULT hr;
    hr = pTuner->put_Channel(lIndex, AMTUNER_SUBCHAN_DEFAULT, AMTUNER_SUBCHAN_DEFAULT);
    if (NOERROR == hr)
        pTuner->SignalPresent(&SignalStrength);
    *plFoundSignal = (SignalStrength != AMTUNER_NOSIGNAL);
        return hr;
}
```



Con la recepción de difusión, no siempre es posible obtener un bloqueo horizontal, aunque se puede ver la imagen. En estos casos, el hardware del sintonizador tendrá un bloqueo de frecuencia, pero el descodificador no tendrá un bloqueo horizontal. Esta condición se puede detectar al usar [**Put \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) o [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) examinando el código de retorno.



| Value    | Descripción                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ correcto    | La operación de optimización se realizó correctamente y el sintonizador tenía un bloqueo de frecuencia.                                                                                                                          |
| S \_ false | No hubo errores durante la operación de optimización, pero el sintonizador no pudo obtener un bloqueo de frecuencia. Es muy improbable que haya un canal visible resultante de esta operación. |



 

Cualquier otro código de retorno indica que se produjo algún error.

Un valor devuelto de S \_ OK no garantiza que el descodificador tenga un bloqueo horizontal. El método [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) actualiza el parámetro *FoundSignal* para indicar si se ha conseguido un bloqueo horizontal. El método [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) devuelve la misma información.

Sin embargo, cuando el valor devuelto es \_ correcto, la aplicación tiene la opción de omitir el parámetro *FoundSignal* , porque el sintonizador informa de un bloqueo de frecuencia. Existe la posibilidad de un bloqueo de frecuencia en el ruido, pero esta posibilidad se debe sopesar contra la posibilidad de omitir canales visibles.

## <a name="registry-conversion"></a>Conversión del registro

Para admitir invalidaciones de frecuencia, ha cambiado el formato interno de la clave del registro que contiene la información de ajuste. El formato original todavía se admite por compatibilidad con versiones anteriores, pero no admite invalidaciones de frecuencia.

El formato del registro anterior se convierte al nuevo formato siempre que se llama al método [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) . Si la aplicación agrega invalidaciones de frecuencia, debe llamar al método **StoreAutoTune** para convertir al nuevo formato del registro. No es necesario recopilar información de ajuste preciso antes de llamar a **StoreAutoTune**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ajuste de TV analógica internacional](international-analog-tv-tuning.md)
</dt> </dl>

 

 



