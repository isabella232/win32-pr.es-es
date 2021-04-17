---
description: La mayoría de los contadores requieren dos valores de ejemplo para calcular un valor que se pueda mostrar.
ms.assetid: 75e45baf-51c5-400c-a31f-92bdab4ee492
title: Mostrar datos de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d913474b794585dd557fae2b1fc232336b637d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677905"
---
# <a name="displaying-performance-data"></a>Mostrar datos de rendimiento

La mayoría de los contadores requieren dos valores de ejemplo para calcular un valor que se pueda mostrar. La fórmula de cada contador determina si el contador requiere dos ejemplos. Para obtener una lista de contadores y sus fórmulas, vea la sección tipos de contador del [Kit de implementación de Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).

[Recopilación de datos de rendimiento](collecting-performance-data.md) muestra cómo recuperar datos de ejemplo. Una vez que tenga los ejemplos, normalmente llama a [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue) para calcular un valor que se puede mostrar.

Si necesita escalar o reducir verticalmente el valor del contador para mostrar el valor, llame a la función [**PdhSetCounterScaleFactor**](/windows/desktop/api/Pdh/nf-pdh-pdhsetcounterscalefactor) antes de llamar a [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue). Los valores de contador se pueden escalar con una potencia de diez desde un factor de-7 a 7.

Si la ruta de acceso del contador contiene un carácter comodín para el nombre de instancia, llame a [**PdhGetFormattedCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcounterarraya) para recuperar una matriz de valores de contador con formato para cada instancia recopilada.

También puede usar las funciones [**PdhCalculateCounterFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhcalculatecounterfromrawvalue) y [**PdhFormatFromRawValue**](/windows/desktop/api/Pdh/nf-pdh-pdhformatfromrawvalue) para calcular un valor que se pueda mostrar. Para usar estas funciones, debe recuperar el ejemplo recopilado después de cada llamada a [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) y almacenar el ejemplo usted mismo. Para recuperar el ejemplo, llame a la función [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue) o [**PdhGetRawCounterArray**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcounterarraya) . Para los valores de contadores basados en el tiempo, llame a [**PdhGetCounterTimeBase**](/windows/desktop/api/Pdh/nf-pdh-pdhgetcountertimebase) antes de **PdhFormatFromRawValue** para recuperar la base de tiempo del contador.

Si realiza cálculos con los datos sin procesar, compruebe siempre el miembro **CStatus** de la estructura del [**\_ \_ contador sin formato PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) antes de usar el ejemplo. El ejemplo no es válido si el valor de **CStatus** no es PDH \_ CStatus \_ nuevos \_ datos o los \_ \_ datos válidos de PDH CStatus \_ .

## <a name="displaying-statistics-for-a-counter"></a>Mostrar estadísticas de un contador

Si desea calcular los valores mínimo, máximo y promedio de un contador, llame a la función [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) . Al recopilar ejemplos, almacene las estructuras de [**\_ \_ contador sin formato PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) en una matriz que se pasa a **PdhComputeCounterStatistics**. La función devuelve los valores estadísticos en una estructura de [**\_ estadísticas de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics) .

También puede usar esta función para comprimir un archivo de registro. Por ejemplo, lea diez registros de un archivo de registro, llame a [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) para calcular el valor medio y, a continuación, escriba el valor medio en un archivo de registro de salida.

 

 
