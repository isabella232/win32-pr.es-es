---
description: Recopilar información Fine-Tuning datos
ms.assetid: 0d9ea896-e0a9-411b-9a10-e366e3686a34
title: Recopilar información Fine-Tuning datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7148724473504631431780f320b1c1852f6de9fe5f8d29b38dca94882f37f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084445"
---
# <a name="collecting-fine-tuning-information"></a>Recopilar información Fine-Tuning datos

Aunque normalmente se espera que las frecuencias de cable sean exactas, la estación de difusión puede ajustar o reducir varias kHz las frecuencias de difusión para reducir las posibles interferencias con los canales vecinos.

Cuando el filtro tv Tuner se ajuste a un canal, busca la señal más precisa. Para guardar esta información en el Registro para las operaciones de optimización posteriores, haga lo siguiente:

1.  Llame [**a IAMTuner::ChannelMinMax para**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) determinar el intervalo de entradas de frecuencia en la tabla de frecuencia actual.
2.  Llame al [**método IAMTuner::p ut \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) una vez para cada índice de frecuencia del intervalo.
3.  Llame [**a IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) para guardar la información de ajuste en el Registro. La información se almacena en la clave del Registro para el espacio de optimización actual.

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



Con versiones anteriores del filtro tv Tuner, se recomienda el método [**IAMTVTuner::AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) para ajustar. Sin embargo, este método omite las invalidaciones de frecuencia, por lo que ya no se recomienda su uso. El código siguiente es equivalente al **método AutoTune,** pero funciona correctamente con invalidaciones de frecuencia:


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



Con la recepción de difusión, no siempre es posible obtener un bloqueo horizontal, aunque la imagen se puede ver. En estos casos, el hardware del afinador tendrá un bloqueo de frecuencia, pero el descodificador no tendrá bloqueo horizontal. Esta condición se puede detectar al usar [**put \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) o [**AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) examinando el código de retorno.



| Valor    | Descripción                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK    | La operación de ajuste se ha correcto y el ajuste tiene un bloqueo de frecuencia.                                                                                                                          |
| S \_ FALSE | No hubo errores durante la operación de ajuste, pero el afinador no pudo obtener un bloqueo de frecuencia. Es muy poco probable que haya un canal visualizable resultante de esta operación. |



 

Cualquier otro código de retorno indica que se ha producido algún error.

Un valor devuelto de S \_ OK no garantiza que el descodificador tenga un bloqueo horizontal. El [**método AutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) actualiza el *parámetro FoundSignal* para indicar si se ha logrado o no el bloqueo horizontal. El [**método IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) devuelve la misma información.

Sin embargo, cuando el valor devuelto es S OK, la aplicación tiene la opción de omitir el parámetro \_ *FoundSignal,* ya que el tuner informa de un bloqueo de frecuencia. Existe la posibilidad de un bloqueo de frecuencia en el ruido, pero esta posibilidad debe sopesar la posibilidad de omitir los canales que se pueden ver.

## <a name="registry-conversion"></a>Conversión del Registro

Para admitir invalidaciones de frecuencia, ha cambiado el formato interno de la clave del Registro que contiene información de ajuste preciso. El formato original sigue siendo compatible con versiones anteriores, pero no admite invalidaciones de frecuencia.

El formato del Registro anterior se convierte al nuevo formato cada vez que se llama al método [**IAMTVTuner::StoreAutoTune.**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) Si la aplicación agrega invalidaciones de frecuencia, debe llamar al método **StoreAutoTune** para convertir al nuevo formato del Registro. No es necesario recopilar información de ajuste antes de llamar **a StoreAutoTune**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ajuste de televisión análoga internacional](international-analog-tv-tuning.md)
</dt> </dl>

 

 



