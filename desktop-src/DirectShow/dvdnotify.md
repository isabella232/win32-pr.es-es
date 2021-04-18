---
description: El evento DVDNotify notifica a una aplicación de muchos eventos de DVD e instrucciones de disco diferentes.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: DVDNotify (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b31a2974bec428cb8ffe290edc9a384445e42070
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680443"
---
# <a name="dvdnotify"></a><span data-ttu-id="e58e9-103">DVDNotify</span><span class="sxs-lookup"><span data-stu-id="e58e9-103">DVDNotify</span></span>

> [!Note]  
> <span data-ttu-id="e58e9-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e58e9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e58e9-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="e58e9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e58e9-106">El `DVDNotify` evento notifica a una aplicación de muchos eventos de DVD e instrucciones de disco diferentes.</span><span class="sxs-lookup"><span data-stu-id="e58e9-106">The `DVDNotify` event notifies an application of many different DVD events and disc instructions.</span></span>

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a><span data-ttu-id="e58e9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e58e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e58e9-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span><span class="sxs-lookup"><span data-stu-id="e58e9-108"><span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*</span></span>
</dt> <dd>

<span data-ttu-id="e58e9-109">Especifica el código de notificación de eventos de DVD.</span><span class="sxs-lookup"><span data-stu-id="e58e9-109">Specifies the DVD event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e58e9-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="e58e9-110"><span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*</span></span>
</dt> <dd>

<span data-ttu-id="e58e9-111">Puede contener información adicional relacionada con el evento.</span><span class="sxs-lookup"><span data-stu-id="e58e9-111">Can contain additional information related to the event.</span></span>

</dd> <dt>

<span data-ttu-id="e58e9-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span><span class="sxs-lookup"><span data-stu-id="e58e9-112"><span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*</span></span>
</dt> <dd>

<span data-ttu-id="e58e9-113">Puede contener información adicional relacionada con el evento.</span><span class="sxs-lookup"><span data-stu-id="e58e9-113">Can contain additional information related to the event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e58e9-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e58e9-114">Remarks</span></span>

<span data-ttu-id="e58e9-115">Los [códigos de notificación de eventos de DVD](dvd-notification-codes.md) proporcionan una explicación completa de todos los códigos de notificación de eventos de DVD y sus parámetros.</span><span class="sxs-lookup"><span data-stu-id="e58e9-115">[DVD Event Notification Codes](dvd-notification-codes.md) gives a full explanation of all DVD event notification codes and their parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e58e9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e58e9-116">Requirements</span></span>



| <span data-ttu-id="e58e9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e58e9-117">Requirement</span></span> | <span data-ttu-id="e58e9-118">Value</span><span class="sxs-lookup"><span data-stu-id="e58e9-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e58e9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e58e9-119">Header</span></span><br/> | <dl> <span data-ttu-id="e58e9-120"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="e58e9-120"><dt>Segment.h</dt></span></span> </dl> |



 

 




