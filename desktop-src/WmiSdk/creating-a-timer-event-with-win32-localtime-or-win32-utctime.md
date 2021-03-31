---
description: Puede usar el modelo estándar de eventos intrínsecos y filtros de eventos en combinación con las \_ clases Win32 localtime o Win32 \_ UTCTime para recibir una notificación con hora.
ms.assetid: 89ba41e2-c9b5-4914-b8cb-13d21ff03402
ms.tgt_platform: multiple
title: Crear un evento de temporizador con Win32_LocalTime o Win32_UTCTime
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 011b2270a80f6b632e832f77e8e7c528228801b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278769"
---
# <a name="creating-a-timer-event-with-win32_localtime-or-win32_utctime"></a><span data-ttu-id="59b57-103">Crear un evento de temporizador con Win32 \_ localtime o Win32 \_ UTCTime</span><span class="sxs-lookup"><span data-stu-id="59b57-103">Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime</span></span>

<span data-ttu-id="59b57-104">Puede usar el modelo estándar de eventos intrínsecos y filtros de eventos en combinación con las clases [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) para recibir una notificación con hora.</span><span class="sxs-lookup"><span data-stu-id="59b57-104">You can use the standard model of intrinsic events and event filters in combination with the [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes to receive a timed notification.</span></span> <span data-ttu-id="59b57-105">El método intrínseco es una manera recomendada de generar eventos con tiempo, ya que es coherente con el resto del modelo de eventos de Microsoft y admite condiciones de programación complejas.</span><span class="sxs-lookup"><span data-stu-id="59b57-105">The intrinsic method is a recommended way of generating timed events, as it is consistent with the rest of the Microsoft event model and supports complex scheduling conditions.</span></span>

<span data-ttu-id="59b57-106">Las clases de [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) y [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) son clases Singleton en el \\ espacio de nombres root cimv2 que representan el reloj del sistema.</span><span class="sxs-lookup"><span data-stu-id="59b57-106">The [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) and [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) classes are singleton classes in the root\\cimv2 namespace that represent the system clock.</span></span> <span data-ttu-id="59b57-107">Cuando se consulta, **Win32 \_ localtime** devuelve la hora actual en el momento de la recuperación de datos en un reloj de 24 horas con referencia local.</span><span class="sxs-lookup"><span data-stu-id="59b57-107">When queried, **Win32\_LocalTime** returns the current time at the moment of data retrieval in a 24-hour clock with local reference.</span></span> <span data-ttu-id="59b57-108">La **clase \_ UTCTime de Win32** devuelve la hora actual con la referencia UTC.</span><span class="sxs-lookup"><span data-stu-id="59b57-108">The **Win32\_UTCTime** class returns the current time with UTC reference.</span></span>

<span data-ttu-id="59b57-109">**Para generar eventos Timed o repeating con Win32 \_ localtime o Win32 \_ UTCTime**</span><span class="sxs-lookup"><span data-stu-id="59b57-109">**To generate timed or repeating events with Win32\_LocalTime or Win32\_UTCTime**</span></span>

-   <span data-ttu-id="59b57-110">Configure un filtro de eventos de notificación intrínseco para [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) que solicite la notificación de una fecha y hora específicas.</span><span class="sxs-lookup"><span data-stu-id="59b57-110">Set up an intrinsic notification event filter for [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) that requests notification for a specific date and time.</span></span>

<span data-ttu-id="59b57-111">Por ejemplo, si la hora local en horario de verano es 4 P.M.</span><span class="sxs-lookup"><span data-stu-id="59b57-111">For example, if the local time under Daylight Savings Time is 4 P.M.</span></span> <span data-ttu-id="59b57-112">y la ubicación es GMT-8 y, a continuación, [**Win32 \_ localtime. hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) devuelve 16 y [**Win32 \_ UTCTime. hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) devuelve 23.</span><span class="sxs-lookup"><span data-stu-id="59b57-112">and the location is GMT -8, then [**Win32\_LocalTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) returns 16 and [**Win32\_UTCTime.Hour**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) returns 23.</span></span>

<span data-ttu-id="59b57-113">En el ejemplo de código siguiente se describe cómo crear un filtro de eventos que señale un evento repetido cada día a medianoche.</span><span class="sxs-lookup"><span data-stu-id="59b57-113">The following code example describes how to create an event filter that signals a repeating event every day at midnight.</span></span>

``` syntax
// Win32_LocalTime and Win32_UTCTime reside in root\cimv2 namespace. 
// Defining the EventNamespace allows the filter
// to be compiled in any namespace.
instance of __EventFilter as $FILT1
{
 Name  = "wake-up call";
 Query = "SELECT * FROM __InstanceModificationEvent WHERE "    
 "TargetInstance ISA \"Win32_LocalTime\" AND "
 "TargetInstance.Hour = 0 AND TargetInstance.Minute = 0 AND "
 "TargetInstance.Second = 0";
 QueryLanguage = "WQL";
 EventNamespace = "root\\cimv2";
};
```

 

 
