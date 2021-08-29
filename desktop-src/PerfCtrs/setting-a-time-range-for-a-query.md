---
description: Si el origen de datos es un archivo de registro, puede especificar un intervalo de tiempo para la consulta.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Establecer un intervalo de tiempo para una consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eaea9747a46d9ce1a6e7e7338801063e4cbd79a3f40bb8a097b3dd238914249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143788"
---
# <a name="setting-a-time-range-for-a-query"></a>Establecer un intervalo de tiempo para una consulta

Si el origen de datos es un archivo de registro, puede especificar un intervalo de tiempo para la consulta. La consulta recupera los datos del contador del archivo de registro que se recopiló durante el intervalo de tiempo especificado. Para establecer el intervalo de tiempo, llame a la [**función PdhSetQueryTimeRange.**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) **PdhSetQueryTimeRange** no se usa para consultar datos de rendimiento de orígenes de datos en tiempo real.

Para crear el valor de hora, siga estos pasos.

1.  Asigne una [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) e inicialice los campos con el valor de hora deseado.
2.  Llame [**a SystemTimeToFileTime para**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) convertir el valor de tiempo de la estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en un [**tiempo de estructura FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
3.  Convertir la [**estructura FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) como una variable LONGLONG, teniendo en cuenta las convenciones de relleno de miembros de estructura de la plataforma y el compilador.
4.  Copie el valor LONGLONG en el campo adecuado de la [**estructura PDH \_ TIME \_ INFO.**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

Para recuperar el intervalo de tiempo de todos los datos de rendimiento contenidos en un archivo de registro, llame a la [**función PdhGetDataSourceTimeRange.**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)

 

 
