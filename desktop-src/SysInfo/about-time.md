---
description: Las funciones relacionadas con el tiempo devuelven el tiempo en uno de varios formatos. Puede usar las funciones de tiempo para realizar la conversión entre algunos formatos de hora para facilitar la comparación y la visualización. En la tabla siguiente se resumen los formatos de hora.
ms.assetid: 74feb158-ba45-4660-970b-3eb577b1ebf8
title: Acerca del tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a95571637bb480920f82e90011a72f6eba9e8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082768"
---
# <a name="about-time"></a><span data-ttu-id="948b4-105">Acerca del tiempo</span><span class="sxs-lookup"><span data-stu-id="948b4-105">About Time</span></span>

<span data-ttu-id="948b4-106">Las funciones relacionadas con el tiempo devuelven el tiempo en uno de varios formatos.</span><span class="sxs-lookup"><span data-stu-id="948b4-106">Time-related functions return time in one of several formats.</span></span> <span data-ttu-id="948b4-107">Puede usar las funciones de tiempo para realizar la conversión entre algunos formatos de hora para facilitar la comparación y la visualización.</span><span class="sxs-lookup"><span data-stu-id="948b4-107">You can use the time functions to convert between some time formats for ease of comparison and display.</span></span> <span data-ttu-id="948b4-108">En la tabla siguiente se resumen los formatos de hora.</span><span class="sxs-lookup"><span data-stu-id="948b4-108">The following table summarizes the time formats.</span></span>



| <span data-ttu-id="948b4-109">Formato</span><span class="sxs-lookup"><span data-stu-id="948b4-109">Format</span></span>          | <span data-ttu-id="948b4-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="948b4-110">Type</span></span>                                                                     | <span data-ttu-id="948b4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="948b4-111">Description</span></span>                                                                                                                         |
|-----------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="948b4-112">Sistema</span><span class="sxs-lookup"><span data-stu-id="948b4-112">System</span></span>          | [<span data-ttu-id="948b4-113">**SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="948b4-113">**SYSTEMTIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-systemtime)                                     | <span data-ttu-id="948b4-114">Año, mes, día, hora, segundo y milisegundo, tomado del reloj de hardware interno.</span><span class="sxs-lookup"><span data-stu-id="948b4-114">Year, month, day, hour, second, and millisecond, taken from the internal hardware clock.</span></span>                                            |
| <span data-ttu-id="948b4-115">Local</span><span class="sxs-lookup"><span data-stu-id="948b4-115">Local</span></span>           | <span data-ttu-id="948b4-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) o [ **FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span><span class="sxs-lookup"><span data-stu-id="948b4-116">[**SYSTEMTIME**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) or [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)</span></span> | <span data-ttu-id="948b4-117">Hora del sistema o hora de archivo convertida en la zona horaria local del sistema.</span><span class="sxs-lookup"><span data-stu-id="948b4-117">A system time or file time converted to the system's local time zone.</span></span>                                                               |
| <span data-ttu-id="948b4-118">Archivo</span><span class="sxs-lookup"><span data-stu-id="948b4-118">File</span></span>            | [<span data-ttu-id="948b4-119">**FILETIME**</span><span class="sxs-lookup"><span data-stu-id="948b4-119">**FILETIME**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)                                         | <span data-ttu-id="948b4-120">El número de intervalos de 100 a nanosegundos desde el 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="948b4-120">The number of 100-nanosecond intervals since January 1, 1601.</span></span>                                                                       |
| <span data-ttu-id="948b4-121">MS-DOS</span><span class="sxs-lookup"><span data-stu-id="948b4-121">MS-DOS</span></span>          | <span data-ttu-id="948b4-122">**WORD**</span><span class="sxs-lookup"><span data-stu-id="948b4-122">**WORD**</span></span>                                                                 | <span data-ttu-id="948b4-123">Una palabra empaquetada para la fecha, otra para el tiempo.</span><span class="sxs-lookup"><span data-stu-id="948b4-123">A packed word for the date, another for the time.</span></span>                                                                                   |
| <span data-ttu-id="948b4-124">Windows</span><span class="sxs-lookup"><span data-stu-id="948b4-124">Windows</span></span>         | <span data-ttu-id="948b4-125">**DWORD** o **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="948b4-125">**DWORD** or **ULONGLONG**</span></span>                                               | <span data-ttu-id="948b4-126">Número de milisegundos desde la última vez que se inició el sistema.</span><span class="sxs-lookup"><span data-stu-id="948b4-126">The number of milliseconds since the system was last started.</span></span> <span data-ttu-id="948b4-127">Cuando se recupera como un valor DWORD, la hora de Windows se recorre cada 49,7 días.</span><span class="sxs-lookup"><span data-stu-id="948b4-127">When retrieved as a DWORD value, Windows time cycles every 49.7 days.</span></span> |
| <span data-ttu-id="948b4-128">Recuento de interrupciones</span><span class="sxs-lookup"><span data-stu-id="948b4-128">Interrupt Count</span></span> | <span data-ttu-id="948b4-129">**ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="948b4-129">**ULONGLONG**</span></span>                                                            | <span data-ttu-id="948b4-130">El número de intervalos de 100 segundos desde la última vez que se inició el sistema.</span><span class="sxs-lookup"><span data-stu-id="948b4-130">The number of 100-nanosecond intervals since the system was last started.</span></span>                                                           |



 

<span data-ttu-id="948b4-131">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="948b4-131">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="948b4-132">Hora del sistema</span><span class="sxs-lookup"><span data-stu-id="948b4-132">System Time</span></span>](system-time.md)
-   [<span data-ttu-id="948b4-133">Hora local</span><span class="sxs-lookup"><span data-stu-id="948b4-133">Local Time</span></span>](local-time.md)
-   [<span data-ttu-id="948b4-134">Horas de archivo</span><span class="sxs-lookup"><span data-stu-id="948b4-134">File Times</span></span>](file-times.md)
-   [<span data-ttu-id="948b4-135">Fecha y hora de MS-DOS</span><span class="sxs-lookup"><span data-stu-id="948b4-135">MS-DOS Date and Time</span></span>](ms-dos-date-and-time.md)
-   [<span data-ttu-id="948b4-136">Hora de Windows</span><span class="sxs-lookup"><span data-stu-id="948b4-136">Windows Time</span></span>](windows-time.md)
-   [<span data-ttu-id="948b4-137">Tiempo de interrupción</span><span class="sxs-lookup"><span data-stu-id="948b4-137">Interrupt Time</span></span>](interrupt-time.md)

 

 
