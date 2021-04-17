---
description: Indica que se ha activado automáticamente un botón de menú de DVD según las instrucciones del disco. Esto se produce cuando se agota el tiempo de espera de un menú y el disco ha especificado un botón para que se active automáticamente.
ms.assetid: ecd79c2a-1717-473d-b111-2b1db2ca4cc1
title: EC_DVD_BUTTON_AUTO_ACTIVATED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_AUTO_ACTIVATED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6a30ddcff32140165d5cb6cb648df84b3360a1b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680853"
---
# <a name="ec_dvd_button_auto_activated"></a><span data-ttu-id="b6ce8-103">botón de DVD de EC \_ \_ \_ \_ activado automáticamente</span><span class="sxs-lookup"><span data-stu-id="b6ce8-103">EC\_DVD\_BUTTON\_AUTO\_ACTIVATED</span></span>

<span data-ttu-id="b6ce8-104">Indica que se ha activado automáticamente un botón de menú de DVD según las instrucciones del disco. Esto se produce cuando se agota el tiempo de espera de un menú y el disco ha especificado un botón para que se active automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b6ce8-104">Signals that a DVD menu button has been automatically activated per instructions on the disc. This occurs when a menu times out and the disc has specified a button to be automatically activated.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6ce8-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6ce8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6ce8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b6ce8-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b6ce8-107">Valor **DWORD** que indica el botón que se activó.</span><span class="sxs-lookup"><span data-stu-id="b6ce8-107">**DWORD** value indicating the button that was activated.</span></span>

</dd> <dt>

<span data-ttu-id="b6ce8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b6ce8-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b6ce8-109">Cero.</span><span class="sxs-lookup"><span data-stu-id="b6ce8-109">Zero.</span></span>

</dd> </dl>

<span data-ttu-id="b6ce8-110">Este evento se desencadena en todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="b6ce8-110">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ce8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6ce8-111">Requirements</span></span>



| <span data-ttu-id="b6ce8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6ce8-112">Requirement</span></span> | <span data-ttu-id="b6ce8-113">Value</span><span class="sxs-lookup"><span data-stu-id="b6ce8-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6ce8-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6ce8-114">Header</span></span><br/> | <dl> <span data-ttu-id="b6ce8-115"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6ce8-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6ce8-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6ce8-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ce8-117">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="b6ce8-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="b6ce8-118">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="b6ce8-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b6ce8-119">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="b6ce8-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




