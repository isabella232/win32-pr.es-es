---
description: Los tipos de contador no computacional no tienen una fórmula asociada. El valor sin formato es directamente significativo.
ms.assetid: 2a6bb3a3-0aec-437a-881a-c4e14fcff6da
ms.tgt_platform: multiple
title: Tipos de contador no computacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ba2757f08dcb2256236117daf2ef3343004425
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277703"
---
# <a name="noncomputational-counter-types"></a>Tipos de contador no computacional

Los tipos de contador no computacional no tienen una fórmula asociada. El valor sin formato es directamente significativo.

La propiedad **FilesToBeIndexed** de la [**clase \_ \_ \_ IndexingService ContentIndex de Win32 PerfRawData**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) es un ejemplo del tipo de contador **Perf \_ Counter \_ RAWCOUNT** . Contiene un recuento de archivos que no se han indexado.

Los tipos de contador se designan mediante la constante definida en WINPERF. h, que se encuentra en el kit de desarrollo de software (SDK) de Microsoft Windows. En la tabla siguiente se enumeran los tipos de contador no computacional que se proporcionan.



| Tipo                                                                                                 | Descripción                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Rendimiento \_ de \_Texto del contador](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 2816<br/>                | Este tipo de contador muestra una cadena de texto de longitud variable en Unicode. No muestra los valores calculados.               |
| [Rendimiento \_ de COUNTER \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 65536<br/>           | Valor del contador sin formato que no requiere cálculos y representa una muestra que es solo el último valor observado. |
| [Rendimiento \_ de COUNTER \_ Large \_ RAWCOUNT](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 65792<br/>    | Igual que **el \_ contador \_ de rendimiento RAWCOUNT**, pero una representación de 64 bits para valores mayores.                                    |
| [Rendimiento \_ de COUNTER \_ RAWCOUNT \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))0<br/>                  | Valor observado más recientemente en formato hexadecimal. No muestra promedios.                                    |
| [Rendimiento \_ de COUNTER \_ Large \_ RAWCOUNT \_ Hex](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))decimal 256<br/> | Igual que **el \_ contador de rendimiento \_ RAWCOUNT \_ Hex**, pero una representación de 64 bits en formato hexadecimal para su uso con valores grandes.        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de contador de rendimiento de WMI](wmi-performance-counter-types.md)
</dt> </dl>

 

