---
description: La fecha y la hora de ms-dos son valores de 16 bits empaquetados que especifican el mes, el día, el año y la hora del día en que se escribió por última vez en un archivo de MS-DOS.
ms.assetid: 948e6d77-dd01-4c90-9ef0-af143972c3fa
title: Fecha y hora de MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d401c731c9a3f5127511e28adf846c929a89a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666638"
---
# <a name="ms-dos-date-and-time"></a><span data-ttu-id="294d5-103">Fecha y hora de MS-DOS</span><span class="sxs-lookup"><span data-stu-id="294d5-103">MS-DOS Date and Time</span></span>

<span data-ttu-id="294d5-104">La **fecha** y la **hora** de ms-dos son valores de 16 bits empaquetados que especifican el mes, el día, el año y la hora del día en que se escribió por última vez en un archivo de ms-dos.</span><span class="sxs-lookup"><span data-stu-id="294d5-104">**MS-DOS date** and **MS-DOS time** are packed 16-bit values that specify the month, day, year, and time of day an MS-DOS file was last written to.</span></span> <span data-ttu-id="294d5-105">MS-DOS registra la fecha y la hora en que una aplicación MS-DOS crea o escribe en un archivo.</span><span class="sxs-lookup"><span data-stu-id="294d5-105">MS-DOS records the date and time whenever an MS-DOS application creates or writes to a file.</span></span> <span data-ttu-id="294d5-106">Las aplicaciones MS-DOS recuperan esta fecha y hora mediante funciones de MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="294d5-106">MS-DOS applications retrieve this date and time using MS-DOS functions.</span></span> <span data-ttu-id="294d5-107">Cuando se usa la función [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) para recuperar las horas de archivo de los archivos creados por ms-dos, **GetFileTime** convierte automáticamente las fechas y horas de ms-dos en horas basadas en UTC.</span><span class="sxs-lookup"><span data-stu-id="294d5-107">When you use the [**GetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) function to retrieve the file times for files that were created by MS-DOS, **GetFileTime** automatically converts MS-DOS dates and times to UTC-based times.</span></span>

<span data-ttu-id="294d5-108">Si encuentra una fecha y una hora de MS-DOS que no se han convertido, puede convertirla a una hora basada en UTC mediante la función [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) .</span><span class="sxs-lookup"><span data-stu-id="294d5-108">If you encounter an MS-DOS date and time that has not been converted, you can convert it to a UTC-based time by using the [**DosDateTimeToFileTime**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) function.</span></span> <span data-ttu-id="294d5-109">Esta función copia la fecha y hora convertidas en una estructura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="294d5-109">This function copies the converted date and time to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="294d5-110">Puede volver a convertir el valor en una fecha y hora de MS-DOS mediante la función [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) .</span><span class="sxs-lookup"><span data-stu-id="294d5-110">You can convert the value back to an MS-DOS date and time by using the [**FileTimeToDosDateTime**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) function.</span></span>

 

 
