---
title: Mensaje de WM_DDE_ADVISE (DDE. h)
description: Una aplicación cliente de Intercambio dinámico de datos (DDE) envía el \_ mensaje de notificación de DDE de WM \_ a una aplicación de servidor DDE para solicitar al servidor que proporcione una actualización para un elemento de datos cada vez que cambie el elemento.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- Intercambio de datos de mensajes de WM_DDE_ADVISE
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150212"
---
# <a name="wm_dde_advise-message"></a><span data-ttu-id="dfaaa-104">Mensaje de aviso de \_ DDE de WM \_</span><span class="sxs-lookup"><span data-stu-id="dfaaa-104">WM\_DDE\_ADVISE message</span></span>

<span data-ttu-id="dfaaa-105">Una aplicación cliente de Intercambio dinámico de datos (DDE) envía el mensaje de **\_ \_ notificación de DDE de WM** a una aplicación de servidor DDE para solicitar al servidor que proporcione una actualización para un elemento de datos cada vez que cambie el elemento.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-105">A Dynamic Data Exchange (DDE) client application posts the **WM\_DDE\_ADVISE** message to a DDE server application to request the server to supply an update for a data item whenever the item changes.</span></span>

<span data-ttu-id="dfaaa-106">Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a><span data-ttu-id="dfaaa-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dfaaa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfaaa-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dfaaa-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfaaa-109">Identificador de la ventana de cliente que publica el mensaje.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-109">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="dfaaa-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dfaaa-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dfaaa-111">La palabra de orden inferior es un identificador de un objeto de memoria global que contiene una estructura [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) que especifica cómo se van a enviar los datos.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-111">The low-order word is a handle to a global memory object containing a [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) structure that specifies how the data is to be sent.</span></span>

<span data-ttu-id="dfaaa-112">La palabra de orden superior contiene un átomo que identifica el elemento de datos solicitado.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-112">The high-order word contains an atom that identifies the requested data item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfaaa-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfaaa-113">Remarks</span></span>

<span data-ttu-id="dfaaa-114">Si una aplicación cliente admite más de un formato de Portapapeles para un solo tema y elemento, puede enviar varios mensajes de **\_ \_ notificación de DDE de WM** para el tema y el elemento, especificando un formato de Portapapeles diferente con cada mensaje.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-114">If a client application supports more than one clipboard format for a single topic and item, it can post multiple **WM\_DDE\_ADVISE** messages for the topic and item, specifying a different clipboard format with each message.</span></span> <span data-ttu-id="dfaaa-115">Tenga en cuenta que un servidor solo puede admitir varios formatos para vínculos de datos activos, no vínculos de datos semiactivos.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-115">Note that a server can support multiple formats only for hot data links, not warm data links.</span></span>

### <a name="posting"></a><span data-ttu-id="dfaaa-116">Config</span><span class="sxs-lookup"><span data-stu-id="dfaaa-116">Posting</span></span>

<span data-ttu-id="dfaaa-117">La aplicación cliente envía el mensaje de **\_ \_ aviso de DDE de WM** mediante una llamada a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , no a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="dfaaa-117">The client application posts the **WM\_DDE\_ADVISE** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span>

<span data-ttu-id="dfaaa-118">La aplicación cliente asigna el objeto de memoria global mediante la función [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="dfaaa-118">The client application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="dfaaa-119">Asigna el átomo mediante la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="dfaaa-119">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="dfaaa-120">La aplicación cliente debe crear o volver a usar el parámetro del método *lParam* de **WM \_ DDE \_** para llamar a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="dfaaa-120">The client application must create or reuse the **WM\_DDE\_ADVISE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="dfaaa-121">Si la aplicación receptora (servidor) responde con un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo, la aplicación de publicación debe eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-121">If the receiving (server) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting application must delete the object.</span></span>

<span data-ttu-id="dfaaa-122">La **marca fRelease** no se utiliza en los mensajes de **\_ \_ notificación de DDE de WM** , pero su comportamiento de liberación de datos es similar al de los mensajes de WM y de [**\_ \_ datos DDE**](wm-dde-data.md) [**de WM donde \_ \_**](wm-dde-poke.md) **fRelease** es **true**.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-122">The **fRelease** flag is not used in **WM\_DDE\_ADVISE** messages, but their data-freeing behavior is similar to that of [**WM\_DDE\_DATA**](wm-dde-data.md) and [**WM\_DDE\_POKE**](wm-dde-poke.md) messages where **fRelease** is **TRUE**.</span></span>

### <a name="receiving"></a><span data-ttu-id="dfaaa-123">Recepción</span><span class="sxs-lookup"><span data-stu-id="dfaaa-123">Receiving</span></span>

<span data-ttu-id="dfaaa-124">La aplicación de servidor envía el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para responder de forma positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-124">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="dfaaa-125">Al publicar **la \_ \_ confirmación de WM DDE**, la aplicación puede reutilizar el átomo o eliminarlo y crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-125">When posting **WM\_DDE\_ACK**, the application can reuse the atom or delete it and create a new one.</span></span> <span data-ttu-id="dfaaa-126">Si el mensaje de **\_ \_ confirmación de DDE de WM** es positivo, la aplicación debe eliminar el objeto de memoria global; de lo contrario, la aplicación no debe eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="dfaaa-126">If the **WM\_DDE\_ACK** message is positive, the application should delete the global memory object; otherwise, the application should not delete the object.</span></span>

<span data-ttu-id="dfaaa-127">El servidor debe crear o volver a usar el parámetro *lParam* de la [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) mediante una llamada a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="dfaaa-127">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfaaa-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfaaa-128">Requirements</span></span>



| <span data-ttu-id="dfaaa-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfaaa-129">Requirement</span></span> | <span data-ttu-id="dfaaa-130">Value</span><span class="sxs-lookup"><span data-stu-id="dfaaa-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfaaa-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfaaa-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dfaaa-132">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dfaaa-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dfaaa-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dfaaa-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dfaaa-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dfaaa-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dfaaa-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dfaaa-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfaaa-136"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfaaa-136"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfaaa-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfaaa-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="dfaaa-138">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dfaaa-139">**DDEADVISE**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-139">**DDEADVISE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeadvise)
</dt> <dt>

[<span data-ttu-id="dfaaa-140">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-140">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="dfaaa-141">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-141">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="dfaaa-142">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-142">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="dfaaa-143">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-143">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="dfaaa-144">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-144">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="dfaaa-145">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-145">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="dfaaa-146">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-146">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="dfaaa-147">**\_confirmación de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-147">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="dfaaa-148">**\_datos DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-148">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="dfaaa-149">**hiperdinámico de WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-149">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="dfaaa-150">**\_solicitud de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-150">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="dfaaa-151">**Vista**</span><span class="sxs-lookup"><span data-stu-id="dfaaa-151">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dfaaa-152">Acerca de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="dfaaa-152">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

