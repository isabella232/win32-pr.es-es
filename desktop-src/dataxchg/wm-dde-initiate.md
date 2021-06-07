---
title: WM_DDE_INITIATE mensaje (Dde.h)
description: Una Intercambio dinámico de datos cliente de Intercambio dinámico de datos (DDE) envía un mensaje WM DDE INITIATE para iniciar una conversación con una aplicación de servidor que responde a los nombres de aplicación y \_ \_ tema especificados.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE intercambio de datos de mensajes
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf65e222c7711d429db44e391d4f03c35997e219
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386734"
---
# <a name="wm_dde_initiate-message"></a><span data-ttu-id="68958-104">Mensaje \_ WM DDE \_ INITIATE</span><span class="sxs-lookup"><span data-stu-id="68958-104">WM\_DDE\_INITIATE message</span></span>

<span data-ttu-id="68958-105">Una Intercambio dinámico de datos cliente de Intercambio dinámico de datos (DDE) envía un mensaje **WM \_ DDE \_ INITIATE** para iniciar una conversación con una aplicación de servidor que responde a los nombres de aplicación y tema especificados.</span><span class="sxs-lookup"><span data-stu-id="68958-105">A Dynamic Data Exchange (DDE) client application sends a **WM\_DDE\_INITIATE** message to initiate a conversation with a server application responding to the specified application and topic names.</span></span> <span data-ttu-id="68958-106">Tras recibir este mensaje, se espera que todas las aplicaciones de servidor con nombres que coincidan con la aplicación especificada y que admitan el tema especificado la confirmen.</span><span class="sxs-lookup"><span data-stu-id="68958-106">Upon receiving this message, all server applications with names that match the specified application and that support the specified topic are expected to acknowledge it.</span></span> <span data-ttu-id="68958-107">(Para obtener más información, vea el mensaje [**\_ WM DDE \_ ACK).**](wm-dde-ack.md)</span><span class="sxs-lookup"><span data-stu-id="68958-107">(For more information, see the [**WM\_DDE\_ACK**](wm-dde-ack.md) message.)</span></span>


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a><span data-ttu-id="68958-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68958-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68958-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68958-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68958-110">Identificador a la ventana de cliente que envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="68958-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="68958-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68958-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68958-112">La palabra de orden bajo contiene un atom que identifica la aplicación con la que se solicita una conversación.</span><span class="sxs-lookup"><span data-stu-id="68958-112">The low-order word contains an atom that identifies the application with which a conversation is requested.</span></span> <span data-ttu-id="68958-113">El nombre de la aplicación no puede contener barras diagonales inversas (/) ni barras diagonales inversas ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="68958-113">The application name cannot contain slashes (/) or backslashes (\\).</span></span> <span data-ttu-id="68958-114">Estos caracteres están reservados para implementaciones de red.</span><span class="sxs-lookup"><span data-stu-id="68958-114">These characters are reserved for network implementations.</span></span> <span data-ttu-id="68958-115">Si este parámetro es **NULL,** se solicita una conversación con todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="68958-115">If this parameter is **NULL**, a conversation with all applications is requested.</span></span>

<span data-ttu-id="68958-116">La palabra de orden superior contiene un atom que identifica el tema para el que se solicita una conversación.</span><span class="sxs-lookup"><span data-stu-id="68958-116">The high-order word contains an atom that identifies the topic for which a conversation is requested.</span></span> <span data-ttu-id="68958-117">Si el tema es **NULL,** se solicitan conversaciones para todos los temas disponibles.</span><span class="sxs-lookup"><span data-stu-id="68958-117">If the topic is **NULL**, conversations for all available topics are requested.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68958-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="68958-118">Remarks</span></span>

<span data-ttu-id="68958-119">Si la palabra de orden bajo *de lParam* **es NULL,** cualquier aplicación de servidor puede responder.</span><span class="sxs-lookup"><span data-stu-id="68958-119">If the low-order word of *lParam* is **NULL**, any server application can respond.</span></span> <span data-ttu-id="68958-120">Si la palabra de orden superior de *lParam* **es NULL,** cualquier tema es válido.</span><span class="sxs-lookup"><span data-stu-id="68958-120">If the high-order word of *lParam* is **NULL**, any topic is valid.</span></span> <span data-ttu-id="68958-121">Al recibir una solicitud **WM \_ DDE \_ INITIATE** con la palabra de orden superior del parámetro *lParam* establecida en **NULL,** un servidor debe enviar un mensaje [**\_ \_ ACK**](wm-dde-ack.md) de DDE de WM para cada uno de los temas que admite.</span><span class="sxs-lookup"><span data-stu-id="68958-121">Upon receiving a **WM\_DDE\_INITIATE** request with the high-order word of the *lParam* parameter set to **NULL**, a server must send a [**WM\_DDE\_ACK**](wm-dde-ack.md) message for each of the topics it supports.</span></span>

### <a name="sending"></a><span data-ttu-id="68958-122">Envío</span><span class="sxs-lookup"><span data-stu-id="68958-122">Sending</span></span>

<span data-ttu-id="68958-123">El cliente difunde el mensaje a todas las ventanas de nivel superior estableciendo el primer parámetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) en **HWND \_ BROADCAST.**</span><span class="sxs-lookup"><span data-stu-id="68958-123">The client broadcasts the message to all top-level windows by setting the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="68958-124">Si la aplicación cliente ya ha obtenido el identificador de ventana del servidor deseado, puede enviar **WM \_ DDE \_ INITIATE** directamente a la ventana del servidor pasando el identificador de ventana del servidor como primer parámetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="68958-124">If the client application has already obtained the window handle of the desired server, it can send **WM\_DDE\_INITIATE** directly to the server window by passing the server's window handle as the first parameter of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span>

<span data-ttu-id="68958-125">La aplicación cliente asigna atoms mediante una llamada a la [**función GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)</span><span class="sxs-lookup"><span data-stu-id="68958-125">The client application allocates atoms by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="68958-126">Cuando [**sendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) devuelve un valor, la aplicación cliente debe eliminar los atoms.</span><span class="sxs-lookup"><span data-stu-id="68958-126">When [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) returns, the client application must delete the atoms.</span></span>

### <a name="receiving"></a><span data-ttu-id="68958-127">Recepción</span><span class="sxs-lookup"><span data-stu-id="68958-127">Receiving</span></span>

<span data-ttu-id="68958-128">Para completar el inicio de una conversación, la aplicación de servidor debe responder con uno o varios mensajes [**\_ DDE \_ ACK**](wm-dde-ack.md) de WM, donde cada mensaje es para un tema independiente.</span><span class="sxs-lookup"><span data-stu-id="68958-128">To complete the initiation of a conversation, the server application must respond with one or more [**WM\_DDE\_ACK**](wm-dde-ack.md) messages, where each message is for a separate topic.</span></span> <span data-ttu-id="68958-129">Al enviar **el \_ mensaje DDE \_ ACK** de WM, el servidor debe crear nuevos átomos; no debe reutilizar los átomos enviados con **WM \_ DDE \_ INITIATE**.</span><span class="sxs-lookup"><span data-stu-id="68958-129">When sending **WM\_DDE\_ACK** message, the server should create new atoms; it should not reuse the atoms sent with **WM\_DDE\_INITIATE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="68958-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68958-130">Requirements</span></span>



| <span data-ttu-id="68958-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="68958-131">Requirement</span></span> | <span data-ttu-id="68958-132">Valor</span><span class="sxs-lookup"><span data-stu-id="68958-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68958-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68958-133">Minimum supported client</span></span><br/> | <span data-ttu-id="68958-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="68958-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="68958-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68958-135">Minimum supported server</span></span><br/> | <span data-ttu-id="68958-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="68958-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="68958-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68958-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="68958-138"><dt>Dde.h (incluir Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="68958-138"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68958-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="68958-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="68958-140">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="68958-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="68958-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="68958-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="68958-142">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="68958-142">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="68958-143">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="68958-143">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="68958-144">**WM \_ DDE \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="68958-144">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="68958-145">**Conceptual**</span><span class="sxs-lookup"><span data-stu-id="68958-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="68958-146">Acerca de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="68958-146">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

