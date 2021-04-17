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
# <a name="setting-a-time-range-for-a-query"></a><span data-ttu-id="d0ec4-103">Establecer un intervalo de tiempo para una consulta</span><span class="sxs-lookup"><span data-stu-id="d0ec4-103">Setting a Time Range for a Query</span></span>

<span data-ttu-id="d0ec4-104">Si el origen de datos es un archivo de registro, puede especificar un intervalo de tiempo para la consulta.</span><span class="sxs-lookup"><span data-stu-id="d0ec4-104">If the data source is a log file, you can specify a time range for the query.</span></span> <span data-ttu-id="d0ec4-105">La consulta recupera los datos del contador del archivo de registro que se recopiló durante el intervalo de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="d0ec4-105">The query retrieves counter data from the log file that was collected during the specified time range.</span></span> <span data-ttu-id="d0ec4-106">Para establecer el intervalo de tiempo, llame a la función [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) .</span><span class="sxs-lookup"><span data-stu-id="d0ec4-106">To set the time range, call the [**PdhSetQueryTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhsetquerytimerange) function.</span></span> <span data-ttu-id="d0ec4-107">**PdhSetQueryTimeRange** no se utiliza para consultar los datos de rendimiento de los orígenes de datos en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="d0ec4-107">**PdhSetQueryTimeRange** is not used to query performance data from real time data sources.</span></span>

<span data-ttu-id="d0ec4-108">Para crear el valor de hora, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="d0ec4-108">To create time value, use the following steps.</span></span>

1.  <span data-ttu-id="d0ec4-109">Asigne una estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) e inicialice los campos con el valor de tiempo deseado.</span><span class="sxs-lookup"><span data-stu-id="d0ec4-109">Allocate a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure and initialize the fields with the desired time value.</span></span>
2.  <span data-ttu-id="d0ec4-110">Llame a [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) para convertir el valor de hora de la estructura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) en una hora de estructura de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="d0ec4-110">Call [**SystemTimeToFileTime**](/windows/desktop/api/timezoneapi/nf-timezoneapi-systemtimetofiletime) to convert the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure time value to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure time.</span></span>
3.  <span data-ttu-id="d0ec4-111">Convierta la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) en una variable LONGLONG, teniendo en cuenta las convenciones de relleno de miembros de la estructura de la plataforma y el compilador.</span><span class="sxs-lookup"><span data-stu-id="d0ec4-111">Cast the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure as a LONGLONG variable, keeping in mind the structure member padding conventions of your platform and compiler.</span></span>
4.  <span data-ttu-id="d0ec4-112">Copie el valor LONGLONG en el campo correspondiente de la estructura de [**\_ \_ información de hora de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) .</span><span class="sxs-lookup"><span data-stu-id="d0ec4-112">Copy the LONGLONG value to the appropriate field in the [**PDH\_TIME\_INFO**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info) structure.</span></span>

<span data-ttu-id="d0ec4-113">Para recuperar el intervalo de tiempo de todos los datos de rendimiento contenidos en un archivo de registro, llame a la función [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) .</span><span class="sxs-lookup"><span data-stu-id="d0ec4-113">To retrieve the time range of all of the performance data contained in a log file, call the [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) function.</span></span>

 

 
