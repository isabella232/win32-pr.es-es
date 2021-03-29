---
description: Indica si se está reproduciendo un bloque de ángulo y se pueden realizar cambios en el ángulo.
ms.assetid: 15593841-3162-4598-86bc-1debca22b284
title: EC_DVD_ANGLES_AVAILABLE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLES_AVAILABLE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e4d2abb17b329323cf4a21128da5dba927b48d4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680807"
---
# <a name="ec_dvd_angles_available"></a><span data-ttu-id="2dc35-103">ángulos de DVD de EC \_ \_ \_ disponibles</span><span class="sxs-lookup"><span data-stu-id="2dc35-103">EC\_DVD\_ANGLES\_AVAILABLE</span></span>

<span data-ttu-id="2dc35-104">Indica si se está reproduciendo un bloque de ángulo y se pueden realizar cambios en el ángulo.</span><span class="sxs-lookup"><span data-stu-id="2dc35-104">Indicates whether an angle block is being played and angle changes can be performed.</span></span>

## <a name="parameters"></a><span data-ttu-id="2dc35-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2dc35-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dc35-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="2dc35-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="2dc35-107">Valor booleano (**bool**) que indica si se está reproduciendo un bloque de ángulo.</span><span class="sxs-lookup"><span data-stu-id="2dc35-107">Boolean (**BOOL**) value that indicates if an angle block is being played back.</span></span> <span data-ttu-id="2dc35-108">Cero (0) indica que la reproducción no está en un bloque de ángulo y los ángulos no están disponibles, uno (1) indica que se está reproduciendo un bloque de ángulo y se pueden realizar cambios de ángulo.</span><span class="sxs-lookup"><span data-stu-id="2dc35-108">Zero (0) indicates that playback is not in an angle block and angles are not available, One (1) indicates that an angle block is being played back and angle changes can be performed.</span></span>

</dd> <dt>

<span data-ttu-id="2dc35-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="2dc35-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="2dc35-110">Cero.</span><span class="sxs-lookup"><span data-stu-id="2dc35-110">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2dc35-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2dc35-111">Remarks</span></span>

<span data-ttu-id="2dc35-112">Los cambios de ángulo no se restringen a los bloques de ángulo y la manifestación del cambio de ángulo solo puede verse en un bloque de ángulo.</span><span class="sxs-lookup"><span data-stu-id="2dc35-112">Angle changes are not restricted to angle blocks and the manifestation of the angle change can be seen only in an angle block.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dc35-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dc35-113">Requirements</span></span>



| <span data-ttu-id="2dc35-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dc35-114">Requirement</span></span> | <span data-ttu-id="2dc35-115">Value</span><span class="sxs-lookup"><span data-stu-id="2dc35-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dc35-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2dc35-116">Header</span></span><br/> | <dl> <span data-ttu-id="2dc35-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2dc35-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dc35-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2dc35-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc35-119">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="2dc35-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="2dc35-120">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="2dc35-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="2dc35-121">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="2dc35-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




