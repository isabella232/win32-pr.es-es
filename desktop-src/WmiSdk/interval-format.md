---
description: Define los intervalos de fecha y hora con un formato similar a la sintaxis de fecha y hora dividiendo la cadena en los campos de días, horas, minutos, segundos y microsegundos.
ms.assetid: 13a3ca74-e3e9-44d7-9254-e288eb70ae4c
ms.tgt_platform: multiple
title: Formato de intervalo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10e13d5febbce22648ec76961269ab18b1c028a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649275"
---
# <a name="interval-format"></a><span data-ttu-id="ef671-103">Formato de intervalo</span><span class="sxs-lookup"><span data-stu-id="ef671-103">Interval Format</span></span>

<span data-ttu-id="ef671-104">WMI define los intervalos de fecha y hora con un formato similar a la sintaxis de fecha y hora dividiendo la cadena en los campos de días, horas, minutos, segundos y microsegundos.</span><span class="sxs-lookup"><span data-stu-id="ef671-104">WMI defines date-time intervals with a format similar to the date and time syntax by breaking the string into the fields for days, hours, minutes, seconds, and microseconds.</span></span>

<span data-ttu-id="ef671-105">En el ejemplo siguiente se muestra el formato de un intervalo de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="ef671-105">The following example shows the format of a date-time interval.</span></span>

``` syntax
ddddddddHHMMSS.mmmmmm:000
```

<span data-ttu-id="ef671-106">En la tabla siguiente se muestran los campos del intervalo de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="ef671-106">The following table lists the fields of the date-time interval.</span></span>



| <span data-ttu-id="ef671-107">Campo</span><span class="sxs-lookup"><span data-stu-id="ef671-107">Field</span></span>    | <span data-ttu-id="ef671-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef671-108">Description</span></span>                                                                                                                                                                                                                                  |
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef671-109">dddddddd</span><span class="sxs-lookup"><span data-stu-id="ef671-109">dddddddd</span></span> | <span data-ttu-id="ef671-110">Ocho dígitos que representan un número de días (00000000 a 99999999).</span><span class="sxs-lookup"><span data-stu-id="ef671-110">Eight digits that represent a number of days (00000000 through 99999999).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="ef671-111">HH</span><span class="sxs-lookup"><span data-stu-id="ef671-111">HH</span></span>       | <span data-ttu-id="ef671-112">Hora de dos dígitos del día que usa el reloj de 24 horas (de 00 a 23).</span><span class="sxs-lookup"><span data-stu-id="ef671-112">Two-digit hour of the day that uses the 24-hour clock (00 through 23).</span></span>                                                                                                                                                                       |
| <span data-ttu-id="ef671-113">MM</span><span class="sxs-lookup"><span data-stu-id="ef671-113">MM</span></span>       | <span data-ttu-id="ef671-114">Minuto de dos dígitos en la hora (de 00 a 59).</span><span class="sxs-lookup"><span data-stu-id="ef671-114">Two-digit minute in the hour (00 through 59).</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="ef671-115">SS</span><span class="sxs-lookup"><span data-stu-id="ef671-115">SS</span></span>       | <span data-ttu-id="ef671-116">Número de segundos de dos dígitos en el minuto (de 00 a 59).</span><span class="sxs-lookup"><span data-stu-id="ef671-116">Two-digit number of seconds in the minute (00 through 59).</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="ef671-117">MMMMMM</span><span class="sxs-lookup"><span data-stu-id="ef671-117">mmmmmm</span></span>   | <span data-ttu-id="ef671-118">Número de seis dígitos de microsegundos en el segundo (000000 a 999999).</span><span class="sxs-lookup"><span data-stu-id="ef671-118">Six-digit number of microseconds in the second (000000 through 999999).</span></span> <span data-ttu-id="ef671-119">No es necesario que la implementación admita la evaluación mediante este campo, pero este campo siempre debe estar presente para conservar la naturaleza de longitud fija de la cadena.</span><span class="sxs-lookup"><span data-stu-id="ef671-119">Your implementation is not required to support evaluation using this field, but this field must always be present to preserve the fixed-length nature of the string.</span></span> |



 

<span data-ttu-id="ef671-120">Los intervalos siempre tienen un ": 000" final como los cuatro últimos caracteres.</span><span class="sxs-lookup"><span data-stu-id="ef671-120">Intervals always have a trailing ":000" as the last four characters.</span></span> <span data-ttu-id="ef671-121">Además, a diferencia de la fecha y la hora, no puede usar asteriscos para indicar campos no usados.</span><span class="sxs-lookup"><span data-stu-id="ef671-121">Further, unlike the date and time, you cannot use asterisks to indicate unused fields.</span></span> <span data-ttu-id="ef671-122">Además, todas las propiedades de tipo [ \_ DateTime de CIM](cim-datetime.md) que representan intervalos deben marcarse con el calificador estándar de [subtipo](standard-wmi-qualifiers.md) , con el calificador establecido en "Interval".</span><span class="sxs-lookup"><span data-stu-id="ef671-122">In addition, all properties of type [CIM\_DATETIME](cim-datetime.md) that represent intervals must be marked with the [SubType](standard-wmi-qualifiers.md) standard qualifier, with the qualifier set to "interval".</span></span>

<span data-ttu-id="ef671-123">La siguiente cadena representa un intervalo de 1 día, 12 horas, 0 minutos y 32 segundos.</span><span class="sxs-lookup"><span data-stu-id="ef671-123">The following string represents an interval of 1 day, 12 hours, 0 minutes, and 32 seconds.</span></span>

``` syntax
00000001120032.000000:000
```

## <a name="related-topics"></a><span data-ttu-id="ef671-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef671-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef671-125">Formato de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="ef671-125">Date and Time Format</span></span>](date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="ef671-126">Acerca de WMI</span><span class="sxs-lookup"><span data-stu-id="ef671-126">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="ef671-127">\_fecha y hora de CIM</span><span class="sxs-lookup"><span data-stu-id="ef671-127">CIM\_DATETIME</span></span>](cim-datetime.md)
</dt> </dl>

 

 



