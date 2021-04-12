---
description: Para crear una nueva consulta que recopile datos de rendimiento de un archivo de registro o de origen en tiempo real, llame a la función PdhOpenQuery. La función devuelve un identificador a la consulta que se utiliza en las siguientes llamadas de función de PDH.
ms.assetid: 6fd4716e-b163-47a3-b0cb-5f9599f8681f
title: Crear una consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9d50ec52966529a3476a6d375606ba3d0b538b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156528"
---
# <a name="creating-a-query"></a>Crear una consulta

Para crear una nueva consulta que recopile datos de rendimiento de un archivo de registro o de origen en tiempo real, llame a la función [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) . La función devuelve un identificador a la consulta que se utiliza en las siguientes llamadas de función de PDH.

Después de crear la consulta, llame a la función [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) para cada contador que desee agregar a la consulta. Puede usar uno de los métodos siguientes para proporcionar la ruta de acceso completa del contador.

-   Defina la ruta de acceso del contador como una cadena estática. Use este método si siempre supervisa el mismo contador y si está familiarizado con la sintaxis correcta de una ruta de acceso de contador. Para obtener información sobre la sintaxis correcta que se usa para especificar un contador, vea [especificar una ruta de acceso de contador](specifying-a-counter-path.md).
-   Inicialice una estructura de [**\_ elementos de ruta de \_ acceso \_ de contador PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) con los nombres del equipo, el objeto, el contador y la instancia. Pase esta estructura a [**PdhMakeCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha) , que devolverá una ruta de contador para los elementos especificados.
-   Especifique una ruta de acceso de contador que contenga caracteres comodín y llame a [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) para obtener una lista de nombres de contadores que coincidan con los caracteres comodín de la ruta de acceso. Examine la lista de nombres de contadores y agregue a la consulta los contadores que desee de esta lista.
-   Llame a la función [**PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) para mostrar un cuadro de diálogo que permita al usuario examinar y seleccionar los contadores de rendimiento. Para obtener más información, vea [examinar contadores](browsing-counters.md).

Tenga en cuenta que si se especifica una instancia de contador que no existe, [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) no notifica una condición de error. En su lugar, devuelve el ERROR \_ Success. La razón de este comportamiento es que no se conoce si se ha especificado una instancia de contador no existente o una que exista pero que todavía no se haya creado.

La instancia de contador que falta se informará de [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata), [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)o [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue). Cuando solo se llama a **PdhCollectQueryData** para una instancia de Counter y la instancia de Counter todavía no existe, se supone que la instancia de Counter no existirá y la función devolverá los datos de PDH \_ \_ . Sin embargo, si se consulta más de un contador, **PdhCollectQueryData** puede seguir devolviendo el error \_ si aún no existe una de las instancias de contador. En este caso, llame a **PdhGetRawCounterValue** o **PdhGetFormattedCounterValue** para cada una de las instancias de contador de interés. Si la instancia no existe al llamar a **PdhGetRawCounterValue**, la función devuelve el error \_ Success y establece el miembro **CStatus** del [**\_ \_ contador sin formato de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) en el estado de PDH \_ \_ sin \_ instancia. Si la instancia no existe cuando se llama a **PdhGetFormattedCounterValue**, la función devuelve los \_ datos no válidos de PDH \_ y establece el miembro **CSTATUS** del valor de un [**\_ \_ valor de PDH FMT**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue) en PDH \_ CStatus \_ sin \_ instancia.

Tenga en cuenta que la ruta de acceso del contador especificada en la función [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) debe estar localizada. La función [**PdhAddEnglishCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera) proporciona una manera independiente de la configuración regional de agregar contadores de rendimiento a la consulta. Esta función es la forma recomendada de agregar contadores de configuración regional neutro a una consulta.

Para quitar un contador de una consulta, llame a la función [**PdhRemoveCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter) .

Cuando termine de recopilar datos de una consulta, llame a la función [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) para cerrar la consulta y liberar todos los recursos del sistema asignados. **PdhCloseQuery** cierra todos los identificadores de contador asociados a la consulta.

 

 



