---
description: Indica que el número de secuencia de la subimagen actual ha cambiado para el título principal.
ms.assetid: b6da3201-55df-47dc-ad4f-5cd2e78073ee
title: EC_DVD_SUBPICTURE_STREAM_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_SUBPICTURE_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c30ef0b27185b5300ac5cec877ed4e4b38685c12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679344"
---
# <a name="ec_dvd_subpicture_stream_change"></a><span data-ttu-id="a8efc-103">\_cambio de \_ secuencia de subimagen de DVD de \_ EC \_</span><span class="sxs-lookup"><span data-stu-id="a8efc-103">EC\_DVD\_SUBPICTURE\_STREAM\_CHANGE</span></span>

<span data-ttu-id="a8efc-104">Indica que el número de secuencia de la subimagen actual ha cambiado para el título principal.</span><span class="sxs-lookup"><span data-stu-id="a8efc-104">Signals that the current subpicture stream number changed for the main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8efc-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8efc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8efc-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a8efc-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a8efc-107">Valor **DWORD** que indica el nuevo número de secuencia de la subimagen del usuario.</span><span class="sxs-lookup"><span data-stu-id="a8efc-107">**DWORD** value indicating the new user subpicture stream number.</span></span> <span data-ttu-id="a8efc-108">Los números de secuencia de la subimagen oscilan entre 0 y 31.</span><span class="sxs-lookup"><span data-stu-id="a8efc-108">Subpicture stream numbers range from 0 to 31.</span></span> <span data-ttu-id="a8efc-109">El flujo 0xFFFFFFFF indica que no hay ninguna secuencia seleccionada.</span><span class="sxs-lookup"><span data-stu-id="a8efc-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="a8efc-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a8efc-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a8efc-111">Valor booleano que indica el estado de encendido o apagado de la subimagen.</span><span class="sxs-lookup"><span data-stu-id="a8efc-111">Boolean value that indicates the subpicture's on/off state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8efc-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8efc-112">Remarks</span></span>

<span data-ttu-id="a8efc-113">La subimagen puede cambiar automáticamente con un comando de navegación creado en el disco, así como a través del control de la aplicación mediante [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span><span class="sxs-lookup"><span data-stu-id="a8efc-113">The subpicture can change automatically with a navigation command authored on disc as well as through application control using [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2).</span></span>

<span data-ttu-id="a8efc-114">Este evento se desencadena en todos los dominios.</span><span class="sxs-lookup"><span data-stu-id="a8efc-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8efc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8efc-115">Requirements</span></span>



| <span data-ttu-id="a8efc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8efc-116">Requirement</span></span> | <span data-ttu-id="a8efc-117">Value</span><span class="sxs-lookup"><span data-stu-id="a8efc-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8efc-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8efc-118">Header</span></span><br/> | <dl> <span data-ttu-id="a8efc-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8efc-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8efc-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8efc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8efc-121">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="a8efc-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="a8efc-122">Códigos de notificación de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="a8efc-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a8efc-123">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="a8efc-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




