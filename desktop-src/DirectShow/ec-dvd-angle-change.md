---
description: Indica que se ha cambiado el número de ángulos disponibles o que ha cambiado el número de ángulo actual.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 08914e3fcb93d38ccad25053f7c33480e900ad93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680808"
---
# <a name="ec_dvd_angle_change"></a><span data-ttu-id="1add1-103">\_cambio de \_ ángulo de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="1add1-103">EC\_DVD\_ANGLE\_CHANGE</span></span>

<span data-ttu-id="1add1-104">Indica que se ha cambiado el número de ángulos disponibles o que ha cambiado el número de ángulo actual.</span><span class="sxs-lookup"><span data-stu-id="1add1-104">Signals that either the number of available angles changed or that the current angle number changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="1add1-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1add1-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1add1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="1add1-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="1add1-107">Valor **DWORD** que indica el número de ángulos disponibles.</span><span class="sxs-lookup"><span data-stu-id="1add1-107">**DWORD** value indicating the number of available angles.</span></span> <span data-ttu-id="1add1-108">Cuando el número de ángulos disponibles es 1, el vídeo actual no es multiángulo.</span><span class="sxs-lookup"><span data-stu-id="1add1-108">When the number of available angles is 1, the current video is not multiangle.</span></span>

</dd> <dt>

<span data-ttu-id="1add1-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="1add1-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="1add1-110">Valor **DWORD** que indica el número de ángulo actual.</span><span class="sxs-lookup"><span data-stu-id="1add1-110">**DWORD** value indicating the current angle number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1add1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1add1-111">Remarks</span></span>

<span data-ttu-id="1add1-112">Los números de ángulo oscilan entre 1 y 9.</span><span class="sxs-lookup"><span data-stu-id="1add1-112">Angle numbers range from 1 to 9.</span></span>

<span data-ttu-id="1add1-113">El número de ángulo actual puede cambiar automáticamente con un comando de navegación creado en el disco, así como a través del control de la aplicación mediante la interfaz [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .</span><span class="sxs-lookup"><span data-stu-id="1add1-113">The current angle number can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="1add1-114">Este evento se desencadena en todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="1add1-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="1add1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1add1-115">Requirements</span></span>



| <span data-ttu-id="1add1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1add1-116">Requirement</span></span> | <span data-ttu-id="1add1-117">Value</span><span class="sxs-lookup"><span data-stu-id="1add1-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1add1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1add1-118">Header</span></span><br/> | <dl> <span data-ttu-id="1add1-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1add1-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1add1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="1add1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1add1-121">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="1add1-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="1add1-122">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="1add1-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="1add1-123">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="1add1-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




