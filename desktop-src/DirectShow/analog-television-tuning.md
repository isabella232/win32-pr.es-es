---
description: Optimización de televisión analógica
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: Optimización de televisión analógica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b85d0826340b913df88cb20dc538bc85943949b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659291"
---
# <a name="analog-television-tuning"></a>Optimización de televisión analógica

La optimización se controla mediante el filtro de sintonizador de TV, a través de la interfaz [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) . La interfaz IAMTVTuner hereda IAMTuner. Para obtener un puntero a la interfaz, llame al método [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) como se indica a continuación:


```C++
IAMTVTuner *pTuner = NULL;
hr = pBuild->FindInterface(
    &LOOK_UPSTREAM_ONLY,  // Look upstream from pCap.
    NULL,                 // No particular media type.
    pCap,                 // Pointer to the capture filter.
    IID_IAMTVTuner, (void**)&pTuner);
if (SUCCEEDED(hr))
{
    // Use pTuner ...
    pTuner->Release();
}
```



El primer parámetro indica que se busque en el flujo ascendente desde el filtro de captura.

Tablas de frecuencia

Internamente, el filtro de sintonizador de TV mantiene una lista de tablas de frecuencia. Cada tabla de frecuencia corresponde a las frecuencias de difusión o de cable para un país o región determinados. También hay una tabla de frecuencias genérica "Unicable", que se usa cuando un país o región no tiene un conjunto estándar de asignaciones de frecuencia.

Cada tabla de frecuencia contiene una lista de frecuencias de optimización. En algunos países o regiones, los índices de la tabla se corresponden directamente con los números de canal; es decir, la frecuencia de canal n es la entrada n de la tabla. Sin embargo, para algunos países o regiones, no hay ninguna correspondencia directa entre los números de canal y las frecuencias. En ese caso, la aplicación debe mantener una lista que asigne los números de canal (normalmente elegidos por el usuario) a las entradas de la tabla de frecuencias. Por ejemplo, lo que el usuario ve como "canal 5" podría ser el número de entrada 12 en la tabla de frecuencia.

Para obtener más información, consulte Ajuste de la [televisión analógica internacional](international-analog-tv-tuning.md).

Operaciones básicas de optimización

Si el sintonizador admite varios modos de recepción, como televisión y radio FM, llame a [**IAMTuner::p \_ modo UT**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) para seleccionar el modo. El método [**IAMTuner:: GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) devuelve todos los modos que admite el sintonizador. Por ejemplo, el código siguiente comprueba si el sintonizador admite radio FM y, en ese caso, cambia a ese modo.


```C++
// Check whether the mode is supported.
long lModes = 0;
hr = m_pTuner->GetAvailableModes(&lModes);
if (SUCCEEDED(hr) && (lModes & AMTUNER_MODE_FM_RADIO))
{
    // Set the mode.
    hr = pTuner->put_Mode(AMTUNER_MODE_FM_RADIO);
}
```



Para establecer el país o la región, llame al método [**IAMTuner: \_ :p**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) el método CountryCode. El sintonizador usa este valor para seleccionar la tabla de frecuencias adecuada. Para obtener más información [, consulte asignaciones de país o región](country-region-assignments.md) .

Para establecer el canal, llame al método [**IAMTuner::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) . El argumento para este método no es realmente un número de canal, sino un índice en la tabla de frecuencia actual. Tal y como se ha descrito anteriormente, el número de índice puede corresponderse o no a un número de canal. El método [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) devuelve los valores de índice mínimo y máximo de la tabla de frecuencias actual.

Invalidar entradas de frecuencia

Es posible que algunas entradas de las tablas de frecuencia sean incorrectas o estén obsoletas. Por lo tanto, se proporciona un mecanismo para invalidar entradas individuales mediante las claves del registro.

En el tema sobre el ajuste de la [televisión analógica internacional](international-analog-tv-tuning.md), se explican los detalles. Cada clave del registro define un "espacio de optimización" que contiene una o más subclaves. Cada subclave invalida una entrada de frecuencia. Para establecer el espacio de optimización actual, use el método [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) . Al activar el espacio de optimización, se invalidan las entradas de frecuencia en la tabla de frecuencia actual. Por lo tanto, depende de la aplicación mantener una correspondencia entre los espacios de optimización y los países o regiones. El mejor enfoque es simplemente usar el identificador de país o región como nombre del espacio de optimización.

Ajustar las entradas de frecuencia

La estación de difusión puede ajustar o reducir verticalmente varias frecuencias de difusión para reducir las posibles interferencias con canales vecinos. Dada la frecuencia nominal, la tarjeta sintonizadora puede buscar la frecuencia exacta. El filtro de sintonizador de TV tiene un mecanismo para guardar las frecuencias ajustadas en el registro.

Para cada entrada de la tabla Frequency, llame al \_ método put Channel para ajustarse a esa frecuencia. El sintonizador buscará la frecuencia más precisa. Puede comprobar si el sintonizador ha logrado un bloqueo horizontal mediante una llamada a [**IAMTuner:: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent). El filtro de sintonizador de TV también almacena el resultado internamente.

Después de examinar todas las frecuencias, llame al método [**IAMTVTuner:: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) para escribir los valores actualizados en el registro. Los valores actualizados se almacenan en la entrada del registro para el espacio de optimización actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Televisión analógica](analog-television.md)
</dt> </dl>

 

 



