---
description: Invalidaciones de frecuencia
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Invalidaciones de frecuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536646"
---
# <a name="frequency-overrides"></a>Invalidaciones de frecuencia

Se dedicó una cantidad significativa de esfuerzo para asegurarse de que las frecuencias de difusión y las asignaciones estándar de color son correctas para cada país o región. Incluso, habrá situaciones en las que las tablas de frecuencia no sean suficientes, contengan errores o queden obsoletas. Para solucionar este problema, las frecuencias enumeradas en las tablas de frecuencia del filtro de sintonizador de TV se pueden invalidar selectivamente, mediante el uso de la siguiente clave del registro:

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

> [!Note]  
> A partir de Windows 7, se usa la siguiente clave del registro redirigida para aplicaciones x86 que se ejecutan en versiones x64 de Windows:

 

**HKEY \_ Software de \_ equipo local** \\  \\ **Wow6432Node** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

Las invalidaciones de frecuencia se agrupan en "espacios de optimización" definidos por la aplicación, que se identifican por número. En el ejemplo siguiente se muestra una invalidación de ejemplo:

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

En este caso, "TS0-1" indica el espacio de optimización 0 para las frecuencias de cable. El primer número identifica el espacio de optimización. El segundo número es 0 para frecuencias de difusión o 1 para frecuencias de cable.

La subclave denominada "12" invalida el valor de frecuencia de la frecuencia en el índice 12 de la tabla de frecuencias actual. El valor de la subclave es un valor **DWORD** que especifica la frecuencia en hercios (Hz). En este ejemplo, la frecuencia se establece en 67,25 MHz. Se pueden definir invalidaciones para cualquier número de canal en el intervalo de 1 a 999, ambos inclusive. Si el hardware de ajuste no es compatible con una frecuencia determinada, se producirá un error en la solicitud de optimización.

Este mecanismo también puede usarse para crear nuevos números de canal fuera del intervalo existente en la tabla de frecuencia. El método [**IAMTuner:: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) devolverá el intervalo de canal extendido. Por ejemplo, si el intervalo de canales original era de 1 a 158 y se agrega una invalidación de canal de "200" al registro, el método **ChannelMinMax** devolverá 200 como el canal máximo. En este caso, los números de canal en el intervalo de 159 a 199 no tendrán ninguna frecuencia asignada, por lo que se producirá un error en cualquier solicitud de optimización de ese intervalo.

El método [**IAMTuner::p UT \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) permite a la aplicación elegir el conjunto de invalidaciones y la información de ajuste que se va a usar. Los números de espacio de optimización son arbitrarios. Es responsabilidad de la aplicación mantener la relación entre el espacio de optimización y la tabla de frecuencia. El enfoque más sencillo consiste en usar el código de país o región como el número de espacio de la optimización. Después, cada vez que la aplicación cambia a un nuevo código de país o región, también cambia al mismo espacio de optimización (en ese orden).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ajuste de TV analógica internacional](international-analog-tv-tuning.md)
</dt> </dl>

 

 



