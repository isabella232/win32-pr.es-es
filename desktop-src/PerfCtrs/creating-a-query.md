---
description: Para crear una nueva consulta que recopile datos de rendimiento de un archivo de registro o origen en tiempo real, llame a la función PdhOpenQuery. La función devuelve un identificador a la consulta que se usa en llamadas a funciones PDH posteriores.
ms.assetid: 6fd4716e-b163-47a3-b0cb-5f9599f8681f
title: Crear una consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1175c491ac1336458ed73d375d963f8a68b874bf3fecbb32000730a475d52714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775665"
---
# <a name="creating-a-query"></a>Crear una consulta

Para crear una nueva consulta que recopile datos de rendimiento de un archivo de registro o origen en tiempo real, llame a la [**función PdhOpenQuery.**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) La función devuelve un identificador a la consulta que se usa en llamadas a funciones PDH posteriores.

Después de crear la consulta, llame a [**la función PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) para cada contador que desee agregar a la consulta. Puede usar uno de los métodos siguientes para proporcionar la ruta de acceso completa del contador.

-   Defina la ruta de acceso del contador como una cadena estática. Use este método si siempre supervisa el mismo contador y si está familiarizado con la sintaxis correcta de una ruta de acceso de contador. Para obtener información sobre la sintaxis correcta utilizada para especificar un contador, vea [Especificar una ruta de acceso de contador.](specifying-a-counter-path.md)
-   Inicialice una [**estructura \_ PDH COUNTER \_ PATH \_ ELEMENTS**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) con los nombres del equipo, el objeto, el contador y la instancia. Pase esta estructura a [**PdhMakeCounterPath,**](/windows/desktop/api/Pdh/nf-pdh-pdhmakecounterpatha) que devolverá una ruta de acceso de contador para los elementos especificados.
-   Especifique una ruta de acceso de contador que contenga caracteres comodín y llame a [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) para obtener una lista de nombres de contador que coincidan con los caracteres comodín de la ruta de acceso. Analice la lista de nombres de contadores y agregue a la consulta los contadores que desee de esta lista.
-   Llame a [**la función PdhBrowseCounters**](/windows/desktop/api/Pdh/nf-pdh-pdhbrowsecountersa) para mostrar un cuadro de diálogo que permita al usuario examinar y seleccionar contadores de rendimiento. Para obtener más información, vea [Examinar contadores](browsing-counters.md).

Tenga en cuenta que si se especifica una instancia de contador que no existe, [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) no informa de una condición de error. En su lugar, devuelve ERROR \_ SUCCESS. El motivo de este comportamiento es que no se sabe si se ha especificado una instancia de contador inexistente o una que existirá pero que aún no se ha creado.

[**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata), [**PdhGetRawCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetrawcountervalue)o [**PdhGetFormattedCounterValue**](/windows/desktop/api/Pdh/nf-pdh-pdhgetformattedcountervalue)notifican la instancia de contador que falta. Al llamar a **PdhCollectQueryData** solo para una instancia de contador y la instancia del contador sigue sin existir, se supone que la instancia del contador no existirá y la función devuelve PDH \_ NO \_ DATA. Sin embargo, si se consulta más de un contador, **PdhCollectQueryData** puede seguir devolviendo ERROR SUCCESS incluso si una de las instancias del contador aún \_ no existe. En este caso, llame a **PdhGetRawCounterValue** o **PdhGetFormattedCounterValue** para cada una de las instancias de contador de interés. Si la instancia no existe al llamar a **PdhGetRawCounterValue,** la función devuelve ERROR SUCCESS y establece el miembro \_ **CStatus** de [**PDH \_ RAW \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter) en PDH \_ STATUS NO \_ \_ INSTANCE. Si la instancia no existe al llamar a **PdhGetFormattedCounterValue,** la función devuelve datos no válidos de PDH y establece el miembro CStatus de \_ \_ [**PDH \_ FMT \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue) en PDH  \_ CSTATUS NO \_ \_ INSTANCE.

Tenga en cuenta que la ruta de acceso del contador especificada en [**la función PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) debe estar localizada. La [**función PdhAddEnglishCounter proporciona**](/windows/desktop/api/Pdh/nf-pdh-pdhaddenglishcountera) una manera neutra de la configuración regional para agregar contadores de rendimiento a la consulta. Esta función es la manera recomendada de agregar contadores neutros de configuración regional a una consulta.

Para quitar un contador de una consulta, llame a la [**función PdhRemoveCounter.**](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)

Cuando termine de recopilar datos para una consulta, llame a la función [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) para cerrar la consulta y liberar todos los recursos del sistema asignados. **PdhCloseQuery cierra** todos los identificadores de contador asociados a la consulta.

 

 



