---
description: Si el origen de datos es un archivo de registro, puede especificar un intervalo de tiempo para la consulta.
ms.assetid: 8d9c3e96-3645-4875-9b5f-a6c9ddf23ec3
title: Establecer un intervalo de tiempo para una consulta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55baf642a4a12a86476e2d6feada6b79f1fda72c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062880"
---
# <a name="setting-a-time-range-for-a-query"></a>Establecer un intervalo de tiempo para una consulta

Si el origen de datos es un archivo de registro, puede especificar un intervalo de tiempo para la consulta. La consulta recupera los datos del contador del archivo de registro que se recopiló durante el intervalo de tiempo especificado. Para establecer el intervalo de tiempo, llame a la [**función PdhSetQueryTimeRange.**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) **PdhSetQueryTimeRange** no se usa para consultar datos de rendimiento de orígenes de datos en tiempo real.

Para crear el valor de tiempo, siga estos pasos.

1.  Asigne una [**estructura SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) e inicialice los campos con el valor de hora deseado.
2.  Llame [**a SystemTimeToFileTime para**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) convertir el valor de tiempo de la estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en una [**hora de estructura FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)
3.  Convertir la [**estructura FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) como una variable LONGLONG, teniendo en cuenta las convenciones de relleno de miembros de estructura de la plataforma y el compilador.
4.  Copie el valor LONGLONG en el campo adecuado de la [**estructura PDH \_ TIME \_ INFO.**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

Para recuperar el intervalo de tiempo de todos los datos de rendimiento contenidos en un archivo de registro, llame a la [**función PdhGetDataSourceTimeRange.**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea)

 

 
