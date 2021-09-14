---
description: Los tipos de contadores no condicionales no tienen una fórmula asociada. El valor sin formato es directamente significativo.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Tipos de contadores no condicionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172557"
---
# <a name="noncomputational-counter-types"></a>Tipos de contadores no condicionales

Los tipos de contadores no condicionales no tienen una fórmula asociada. El valor sin formato es directamente significativo.

La **propiedad FilesToBeIndexed** de la clase [**\_ \_ ContentIndex \_ IndexingService de PerfRawData de Win32**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) es un ejemplo del tipo de contador **\_ PERF COUNTER \_ RAWCOUNT.** Contiene un recuento de archivos que no se han indexado.

Los tipos de contador se designan mediante la constante definida en Winperf.h, que se encuentra en el Kit de desarrollo de software (SDK) de Microsoft Windows. En la tabla siguiente se enumeran los tipos de contadores no condicionales que se proporcionan.



| CounterType                                                                                                 | Descripción                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [PERF \_ COUNTER \_ TEXT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 2816<br/>                | Este tipo de contador muestra una cadena de texto de longitud variable en Unicode. No muestra valores calculados.               |
| [PERF \_ COUNTER \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65536<br/>           | Valor de contador sin formato que no requiere cálculos y representa una muestra que es solo el último valor observado. |
| [PERF \_ COUNTER \_ LARGE \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 65792<br/>    | Igual que **PERF \_ COUNTER \_ RAWCOUNT,** pero una representación de 64 bits para valores mayores.                                    |
| [PERF \_ COUNTER \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0<br/>                  | Valor observado más recientemente en formato hexadecimal. No muestra promedios.                                    |
| [PERF \_ COUNTER \_ LARGE \_ RAWCOUNT \_ HEX](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 256<br/> | Igual que **PERF \_ COUNTER \_ RAWCOUNT \_ HEX,** pero una representación de 64 bits en hexadecimal para su uso con valores grandes.        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contadores de rendimiento wmi](wmi-performance-counter-types.md)
</dt> </dl>

 

