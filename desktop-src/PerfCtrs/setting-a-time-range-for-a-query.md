---
description: Si el origen de datos es un archivo de registro, puede especificar un intervalo de tiempo para la consulta.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Establecer un intervalo de tiempo para una consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667249"
---
# <a name="setting-a-time-range-for-a-query"></a>Establecer un intervalo de tiempo para una consulta

Si el origen de datos es un archivo de registro, puede especificar un intervalo de tiempo para la consulta. La consulta recupera los datos del contador del archivo de registro que se recopiló durante el intervalo de tiempo especificado. Para establecer el intervalo de tiempo, llame a la función [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) . **PdhSetQueryTimeRange** no se utiliza para consultar los datos de rendimiento de los orígenes de datos en tiempo real.

Para crear el valor de hora, siga estos pasos.

1.  Asigne una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) e inicialice los campos con el valor de tiempo deseado.
2.  Llame a [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) para convertir el valor de hora de la estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en una hora de estructura de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .
3.  Convierta la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) en una variable LONGLONG, teniendo en cuenta las convenciones de relleno de miembros de la estructura de la plataforma y el compilador.
4.  Copie el valor LONGLONG en el campo correspondiente de la estructura de [**\_ \_ información de hora de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) .

Para recuperar el intervalo de tiempo de todos los datos de rendimiento contenidos en un archivo de registro, llame a la función [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) .

 

 
