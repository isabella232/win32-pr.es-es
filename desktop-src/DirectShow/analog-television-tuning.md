---
description: Ajuste de televisión análoga
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: Ajuste de televisión análoga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b85d0826340b913df88cb20dc538bc85943949b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162289"
---
# <a name="analog-television-tuning"></a>Ajuste de televisión análoga

La optimización se controla mediante el filtro tv Tuner , a través de [**la interfaz IAMTVTuner.**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) La interfaz IAMTVTuner hereda IAMTuner. Para obtener un puntero a la interfaz, llame al [**método ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) como se muestra a continuación:


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



El primer parámetro indica que se debe buscar ascendente desde el filtro de captura.

Tablas de frecuencia

Internamente, el filtro tv Tuner mantiene una lista de tablas de frecuencia. Cada tabla de frecuencias corresponde a las frecuencias de difusión o cable de un país o región determinados. También hay una tabla genérica de frecuencia "unicable", que se usa cuando un país o región no tiene un conjunto estándar de asignaciones de frecuencia.

Cada tabla de frecuencias contiene una lista de frecuencias de optimización. En algunos países o regiones, los índices de la tabla se corresponden directamente con los números de canal; es decir, la frecuencia del canal n es la nª entrada de la tabla. Sin embargo, en algunos países o regiones no hay ninguna correspondencia directa entre los números de canal y las frecuencias. En ese caso, la aplicación debe mantener una lista que asigna los números de canal (normalmente elegidos por el usuario) a las entradas de tabla de frecuencia. Por ejemplo, lo que el usuario ve como "canal 5" podría ser el número de entrada 12 en la tabla de frecuencias.

Para obtener más información, consulte [Ajuste de TELEVISIÓN análogo internacional.](international-analog-tv-tuning.md)

Operaciones básicas de optimización

Si el afinador admite varios modos de recepción, como televisión y radio FM, llame al modo [**IAMTuner::p ut \_ para**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) seleccionar el modo. El [**método IAMTuner::GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) devuelve todos los modos que admite el afinador. Por ejemplo, el código siguiente comprueba si el afinador admite radio FM y, si es así, cambia a ese modo.


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



Para establecer el país o región, llame al [**método IAMTuner::p ut \_ CountryCode.**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) El afinador usa este valor para seleccionar la tabla de frecuencia adecuada. Consulte [Asignaciones de país o región](country-region-assignments.md) para obtener más información.

Para establecer el canal, llame al [**método IAMTuner::p ut \_ Channel.**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) El argumento de este método no es realmente un número de canal, sino un índice en la tabla de frecuencia actual. Como se ha descrito anteriormente, el número de índice puede o no corresponder a un número de canal. El [**método IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) devuelve los valores de índice mínimo y máximo para la tabla de frecuencia actual.

Invalidar entradas de frecuencia

Es posible que algunas entradas de las tablas de frecuencia sean incorrectas o que estén obsoletas. Por lo tanto, se proporciona un mecanismo para invalidar entradas individuales mediante claves del Registro.

Los detalles se explican en el tema [International Analog TV Tuning](international-analog-tv-tuning.md). Cada clave del Registro define un "espacio de optimización" que contiene una o varias subclaves. Cada subclave invalida una entrada de frecuencia. Para establecer el espacio de optimización actual, use el [**método IAMTuner::p ut \_ TuningSpace.**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) Al activar el espacio de optimización se invalidan las entradas de frecuencia de la tabla de frecuencia actual. Por lo tanto, es la aplicación la que debe mantener una correspondencia entre los espacios de optimización y los países o regiones. El mejor enfoque es usar simplemente el identificador de país o región como nombre del espacio de optimización.

Ajustar las entradas de frecuencia

La estación de difusión puede ajustar las frecuencias de difusión hacia arriba o hacia abajo varios kHz para reducir las posibles interferencias con los canales vecinos. Dada la frecuencia nominal, la tarjeta de tuner puede buscar la frecuencia exacta. El filtro de tv tuner tiene un mecanismo para guardar las frecuencias ajustadas en el registro.

Para cada entrada de la tabla frequency, llame al método put \_ Channel para ajustarse a esa frecuencia. El afinador buscará la frecuencia más precisa. Puede comprobar si el afinador ha logrado un bloqueo horizontal llamando a [**IAMTuner::SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent). El filtro tv tuner también almacena el resultado internamente.

Después de examinar todas las frecuencias, llame al método [**IAMTVTuner::StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) para escribir los valores actualizados en el registro. Los valores actualizados se almacenan en la entrada del Registro para el espacio de optimización actual.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Televisión análoga](analog-television.md)
</dt> </dl>

 

 



