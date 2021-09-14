---
description: Invalidaciones de frecuencia
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Invalidaciones de frecuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061164"
---
# <a name="frequency-overrides"></a>Invalidaciones de frecuencia

Se ha invertido una cantidad considerable de esfuerzo para garantizar que las frecuencias de difusión y las asignaciones estándar de color son correctas para cada país o región. Aun así, habrá situaciones en las que las tablas de frecuencia no son suficientes, contienen errores o se vuelven obsoletas. Para solucionar este problema, las frecuencias enumeradas en las tablas de frecuencias del filtro de ajuste de TV se pueden invalidar de forma selectiva, mediante la siguiente clave del Registro:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

> [!Note]  
> A partir Windows 7, se usa la siguiente clave del Registro redirigida para aplicaciones x86 que se ejecutan en versiones x64 de Windows:

 

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Wow6432Node** \\ **Microsoft** \\ **TV System Services** \\ **TVAutoTune** \\ **TS0-1**

Las invalidaciones de frecuencia se agrupan en "espacios de optimización" definidos por la aplicación, que se identifican por número. En el ejemplo siguiente se muestra una invalidación de ejemplo:

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

En este caso, "TS0-1" indica espacio de optimización 0 para frecuencias de cable. El primer número identifica el espacio de optimización. El segundo número es 0 para las frecuencias de difusión o 1 para las frecuencias de cable.

La subclave denominada "12" invalida el valor de frecuencia de la frecuencia en el índice 12 de la tabla de frecuencia actual. El valor de la subclave es **un DWORD** que especifica la frecuencia en Hertz (Hz). En este ejemplo, la frecuencia se establece en 67,25 MHz. Las invalidaciones se pueden definir para cualquier número de canal en el intervalo de 1 a 999, ambos incluidos. Si el hardware de optimización no admite una frecuencia determinada, se producirá un error en la solicitud de optimización.

Este mecanismo también se puede usar para crear nuevos números de canal fuera del intervalo existente en la tabla frequency. El [**método IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) devolverá el intervalo de canales extendido. Por ejemplo, si el intervalo de canales original era de 1 a 158 y se agrega una invalidación de canal de "200" al registro, el método **ChannelMinMax** devolverá 200 como canal máximo. En este caso, los números de canal del intervalo de 159 a 199 no tendrán ninguna frecuencia asignada, por lo que las solicitudes de optimización de ese intervalo producirán un error automáticamente.

El [**método IAMTuner::p ut \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) permite a la aplicación elegir el conjunto de invalidaciones y la información de ajuste que se va a usar. El ajuste de los números de espacio es arbitrario. Es responsabilidad de la aplicación mantener la relación entre el espacio de optimización y la tabla frequency. El enfoque más sencillo es usar el código de país o región como número de espacio de optimización. A continuación, cada vez que la aplicación cambia a un nuevo código de país o región, también cambia al mismo espacio de optimización (en ese orden).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ajuste internacional de televisión análoga](international-analog-tv-tuning.md)
</dt> </dl>

 

 



