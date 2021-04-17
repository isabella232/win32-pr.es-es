---
description: Describe los formatos de hora admitidos para su uso en la cláusula WQL WHERE.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: Formatos de hora de WQL-Supported
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715817"
---
# <a name="wql-supported-time-formats"></a><span data-ttu-id="a427c-103">Formatos de hora de WQL-Supported</span><span class="sxs-lookup"><span data-stu-id="a427c-103">WQL-Supported Time Formats</span></span>

<span data-ttu-id="a427c-104">Además del formato DATETIME de WMI, se admiten los siguientes formatos de fecha para su uso en la cláusula WHERE de WQL.</span><span class="sxs-lookup"><span data-stu-id="a427c-104">In addition to the WMI DATETIME format, the following date formats are supported for use in the WQL WHERE clause.</span></span>



| <span data-ttu-id="a427c-105">Formato</span><span class="sxs-lookup"><span data-stu-id="a427c-105">Format</span></span>                                    | <span data-ttu-id="a427c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a427c-106">Description</span></span>                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a427c-107">HH \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="a427c-107">hh\[ \]{AP}M</span></span><br/>                   | <span data-ttu-id="a427c-108">Hora, tal como se muestra en un reloj de 12 horas, y la designación AM o PM.</span><span class="sxs-lookup"><span data-stu-id="a427c-108">Hour as shown on a twelve-hour clock, and AM or PM designation.</span></span><br/> <span data-ttu-id="a427c-109">4 PM</span><span class="sxs-lookup"><span data-stu-id="a427c-109">4 PM</span></span><br/>                                                                                                             |
| <span data-ttu-id="a427c-110">hh:mm</span><span class="sxs-lookup"><span data-stu-id="a427c-110">hh:mm</span></span><br/>                          | <span data-ttu-id="a427c-111">Hora y minutos delimitados por signos de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="a427c-111">Colon-delimited hour and minutes.</span></span> <span data-ttu-id="a427c-112">Sin designación AM o PM.</span><span class="sxs-lookup"><span data-stu-id="a427c-112">No AM or PM designation.</span></span><br/> <span data-ttu-id="a427c-113">3:23</span><span class="sxs-lookup"><span data-stu-id="a427c-113">3:23</span></span><br/>                                                                                                                  |
| <span data-ttu-id="a427c-114">HH: mm \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="a427c-114">hh:mm\[ \]{AP}M</span></span><br/>                | <span data-ttu-id="a427c-115">Horas y minutos delimitados por signos de dos puntos, espacio opcional y designación AM o PM.</span><span class="sxs-lookup"><span data-stu-id="a427c-115">Colon-delimited hour and minutes, optional space, and AM or PM designation.</span></span><br/> <span data-ttu-id="a427c-116">3:23 AM</span><span class="sxs-lookup"><span data-stu-id="a427c-116">3:23 AM</span></span><br/>                                                                                              |
| <span data-ttu-id="a427c-117">hh:mm:ss</span><span class="sxs-lookup"><span data-stu-id="a427c-117">hh:mm:ss</span></span><br/>                       | <span data-ttu-id="a427c-118">Hora, minutos y segundos delimitados por signos de dos puntos.</span><span class="sxs-lookup"><span data-stu-id="a427c-118">Colon-delimited hour, minutes and seconds.</span></span> <span data-ttu-id="a427c-119">Ninguna designación AM/PM.</span><span class="sxs-lookup"><span data-stu-id="a427c-119">No AM/PM designation.</span></span><br/> <span data-ttu-id="a427c-120">3:23:00</span><span class="sxs-lookup"><span data-stu-id="a427c-120">3:23:00</span></span><br/>                                                                                                         |
| <span data-ttu-id="a427c-121">HH: mm: SS \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="a427c-121">hh:mm:ss\[ \]{AP}M</span></span><br/>             | <span data-ttu-id="a427c-122">Hora, minutos y segundos delimitados por signos de dos puntos, espacio opcional y designación AM/PM.</span><span class="sxs-lookup"><span data-stu-id="a427c-122">Colon-delimited hour, minutes and seconds, optional space, and AM/PM designation.</span></span><br/> <span data-ttu-id="a427c-123">3:23: P.M.</span><span class="sxs-lookup"><span data-stu-id="a427c-123">3:23:00PM</span></span><br/>                                                                                      |
| <span data-ttu-id="a427c-124">HH: mm: SS: UUU</span><span class="sxs-lookup"><span data-stu-id="a427c-124">hh:mm:ss:uuu</span></span><br/>                   | <span data-ttu-id="a427c-125">Hora, minutos y segundos delimitados por signos de dos puntos, y desplazamiento de tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="a427c-125">Colon-delimited hour, minutes and seconds, and three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                                    |
| <span data-ttu-id="a427c-126">HH: mm: SS: \[ \[ u \] u \] u</span><span class="sxs-lookup"><span data-stu-id="a427c-126">hh:mm:ss:\[\[u\]u\]u</span></span><br/>           | <span data-ttu-id="a427c-127">Hora, minutos y segundos delimitados por signos de dos puntos; y un desplazamiento de uno, dos o tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="a427c-127">Colon-delimited hour, minutes and seconds; and one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC.</span></span><br/>                       |
| <span data-ttu-id="a427c-128">HH: mm: SS: UUU \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="a427c-128">hh:mm:ss:uuu\[ \]{AP}M</span></span><br/>         | <span data-ttu-id="a427c-129">Hora, minutos y segundos delimitados por signos de dos puntos, desplazamiento de tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de la hora UTC y la designación AM o PM.</span><span class="sxs-lookup"><span data-stu-id="a427c-129">Colon-delimited hour, minutes and seconds, three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC, and AM or PM designation.</span></span><br/>              |
| <span data-ttu-id="a427c-130">HH: mm: SS: \[ \[ u \] u \] u \[ \] {AP} M</span><span class="sxs-lookup"><span data-stu-id="a427c-130">hh:mm:ss:\[\[u\]u\]u\[ \]{AP}M</span></span><br/> | <span data-ttu-id="a427c-131">Hora, minutos y segundos delimitados por signos de dos puntos; desplazamiento de uno, dos o tres dígitos que indica el número de minutos que la zona horaria de origen se desvía de la hora UTC. y la designación AM o PM.</span><span class="sxs-lookup"><span data-stu-id="a427c-131">Colon-delimited hour, minutes and seconds; one, two, or three-digit offset that indicates the number of minutes that the originating time zone deviates from UTC; and AM or PM designation.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a427c-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a427c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a427c-133">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="a427c-133">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




