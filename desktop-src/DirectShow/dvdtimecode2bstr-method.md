---
description: El método DVDTimeCode2bstr recupera una cadena que indica la hora actual del disco.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Método DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677127"
---
# <a name="dvdtimecode2bstr-method"></a><span data-ttu-id="de94c-103">Método DVDTimeCode2bstr</span><span class="sxs-lookup"><span data-stu-id="de94c-103">DVDTimeCode2bstr Method</span></span>

> [!Note]  
> <span data-ttu-id="de94c-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="de94c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="de94c-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="de94c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="de94c-106">El `DVDTimeCode2bstr` método recupera una cadena que indica la hora actual del disco.</span><span class="sxs-lookup"><span data-stu-id="de94c-106">The `DVDTimeCode2bstr` method retrieves a string indicating the current time on the disc.</span></span>

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a><span data-ttu-id="de94c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de94c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de94c-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span><span class="sxs-lookup"><span data-stu-id="de94c-108"><span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="de94c-109">Especifica la hora actual del disco con respecto al inicio del título como un número obtenido mediante el evento de [**\_ tiempo de \_ \_ HMSF actual \_ del DVD**](ec-dvd-current-hmsf-time.md) .</span><span class="sxs-lookup"><span data-stu-id="de94c-109">Specifies the current time on the disc relative to the start of the title as a Number obtained through the [**EC\_DVD\_CURRENT\_HMSF\_TIME**](ec-dvd-current-hmsf-time.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de94c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de94c-110">Return Value</span></span>

<span data-ttu-id="de94c-111">Devuelve una cadena de 11 caracteres en el formato "HH: mm: SS: FF" que representa las horas, los minutos, los segundos y las tramas que definen la hora actual.</span><span class="sxs-lookup"><span data-stu-id="de94c-111">Returns an 11-character String in the format "hh:mm:ss:ff" representing the hours, minutes, seconds and frames that define the current time.</span></span>

## <a name="remarks"></a><span data-ttu-id="de94c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de94c-112">Remarks</span></span>

<span data-ttu-id="de94c-113">Este método es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="de94c-113">This method is read only.</span></span>

## <a name="see-also"></a><span data-ttu-id="de94c-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="de94c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de94c-115">Control de las notificaciones de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="de94c-115">Handling DVD Event Notifications</span></span>](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



