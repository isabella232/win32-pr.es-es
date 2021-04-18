---
description: Indica una condición de advertencia de DVD.
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: EC_DVD_WARNING (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7f25d4565c2afeb4619f7832f6d5742e07dcca0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679161"
---
# <a name="ec_dvd_warning"></a><span data-ttu-id="f084f-103">\_Advertencia de DVD de EC \_</span><span class="sxs-lookup"><span data-stu-id="f084f-103">EC\_DVD\_WARNING</span></span>

<span data-ttu-id="f084f-104">Indica una condición de advertencia de DVD.</span><span class="sxs-lookup"><span data-stu-id="f084f-104">Signals a DVD warning condition.</span></span>

## <a name="parameters"></a><span data-ttu-id="f084f-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f084f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f084f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="f084f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="f084f-107">Valor **DWORD** que indica la condición de advertencia.</span><span class="sxs-lookup"><span data-stu-id="f084f-107">**DWORD** value indicating the warning condition.</span></span> <span data-ttu-id="f084f-108">Miembro del tipo de datos de [**\_ Advertencia de DVD**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) enumerado.</span><span class="sxs-lookup"><span data-stu-id="f084f-108">Member of the [**DVD\_WARNING**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning) enumerated data type.</span></span>

</dd> <dt>

<span data-ttu-id="f084f-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="f084f-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="f084f-110">Si *pParam1* es igual a \_ Advertencia de DVD \_ Open, la advertencia de advertencia de DVD \_ o la \_ \_ Advertencia de DVD \_ leída, *lParam2* contiene el último código de error devuelto por **GetLastError**.</span><span class="sxs-lookup"><span data-stu-id="f084f-110">If *pParam1* equals DVD\_WARNING\_Open, DVD\_WARNING\_Seek, or DVD\_WARNING\_Read, then *lParam2* contains the last error code returned from **GetLastError**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f084f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f084f-111">Requirements</span></span>



| <span data-ttu-id="f084f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f084f-112">Requirement</span></span> | <span data-ttu-id="f084f-113">Value</span><span class="sxs-lookup"><span data-stu-id="f084f-113">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f084f-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f084f-114">Header</span></span><br/> | <dl> <span data-ttu-id="f084f-115"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f084f-115"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f084f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="f084f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f084f-117">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="f084f-117">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="f084f-118">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="f084f-118">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="f084f-119">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="f084f-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




