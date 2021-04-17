---
description: '\_ \_ Un codificador envía el evento de evento CODECAPI de EC para señalar un evento de codificación. El cliente se registra para el evento Encoder llamando al método ICodecAPI:: RegisterForEvent.'
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680258"
---
# <a name="ec_codecapi_event"></a><span data-ttu-id="6e08e-104">\_evento CODECAPI de EC \_</span><span class="sxs-lookup"><span data-stu-id="6e08e-104">EC\_CODECAPI\_EVENT</span></span>

<span data-ttu-id="6e08e-105">\_ \_ Un codificador envía el evento de evento CODECAPI de EC para señalar un evento de codificación.</span><span class="sxs-lookup"><span data-stu-id="6e08e-105">The EC\_CODECAPI\_EVENT event is sent by an encoder to signal an encoding event.</span></span> <span data-ttu-id="6e08e-106">El cliente se registra para el evento Encoder llamando al método [**ICodecAPI:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .</span><span class="sxs-lookup"><span data-stu-id="6e08e-106">The client registers for encoder event by calling the [**ICodecAPI::RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e08e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e08e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e08e-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6e08e-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6e08e-109">Datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="6e08e-109">User data.</span></span> <span data-ttu-id="6e08e-110">El valor de este parámetro es el puntero que el llamador especificó en el parámetro *UserData* del método [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .</span><span class="sxs-lookup"><span data-stu-id="6e08e-110">The value of this parameter is the pointer that the caller specified in the *userData* parameter of the [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) method.</span></span>

</dd> <dt>

<span data-ttu-id="6e08e-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6e08e-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6e08e-112">Puntero a los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="6e08e-112">Pointer to the event data.</span></span> <span data-ttu-id="6e08e-113">El codificador asigna estos datos y la aplicación debe liberarlos mediante la función **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="6e08e-113">This data is allocated by the encoder and must be freed by the application, using the **CoTaskMemFree** function.</span></span> <span data-ttu-id="6e08e-114">El bloque de datos se inicia con una estructura [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) . convierta el parámetro *lParam2* en un puntero a esta estructura.</span><span class="sxs-lookup"><span data-stu-id="6e08e-114">The data block starts with a [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) structure; cast the *lParam2* parameter to a pointer to this structure.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="6e08e-115">Acción predeterminada</span><span class="sxs-lookup"><span data-stu-id="6e08e-115">Default Action</span></span>

<span data-ttu-id="6e08e-116">Ninguna acción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6e08e-116">No default action.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e08e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e08e-117">Requirements</span></span>



| <span data-ttu-id="6e08e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e08e-118">Requirement</span></span> | <span data-ttu-id="6e08e-119">Value</span><span class="sxs-lookup"><span data-stu-id="6e08e-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6e08e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e08e-120">Header</span></span><br/> | <dl> <span data-ttu-id="6e08e-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e08e-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e08e-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e08e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e08e-123">Códigos de notificación de eventos</span><span class="sxs-lookup"><span data-stu-id="6e08e-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="6e08e-124">Notificación de eventos en DirectShow</span><span class="sxs-lookup"><span data-stu-id="6e08e-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




