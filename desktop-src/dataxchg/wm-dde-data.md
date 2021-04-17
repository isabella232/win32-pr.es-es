---
title: Mensaje de WM_DDE_DATA (DDE. h)
description: Una aplicación de servidor Intercambio dinámico de datos (DDE) envía un \_ mensaje de datos de WM DDE \_ a una aplicación cliente DDE para pasar un elemento de datos al cliente o para notificar al cliente la disponibilidad de un elemento de datos.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- Intercambio de datos de mensajes de WM_DDE_DATA
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714580"
---
# <a name="wm_dde_data-message"></a><span data-ttu-id="1f519-104">\_Mensaje de datos DDE de WM \_</span><span class="sxs-lookup"><span data-stu-id="1f519-104">WM\_DDE\_DATA message</span></span>

<span data-ttu-id="1f519-105">Una aplicación de servidor Intercambio dinámico de datos (DDE) envía un mensaje de **\_ \_ datos de WM DDE** a una aplicación cliente DDE para pasar un elemento de datos al cliente o para notificar al cliente la disponibilidad de un elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="1f519-105">A Dynamic Data Exchange (DDE) server application posts a **WM\_DDE\_DATA** message to a DDE client application to pass a data item to the client or to notify the client of the availability of a data item.</span></span>

<span data-ttu-id="1f519-106">Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="1f519-106">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a><span data-ttu-id="1f519-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f519-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f519-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f519-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f519-109">Identificador de la ventana del servidor que publica el mensaje.</span><span class="sxs-lookup"><span data-stu-id="1f519-109">A handle to the server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="1f519-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f519-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f519-111">La palabra de orden inferior es un identificador de un objeto de memoria global que contiene una estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) con los datos e información adicional.</span><span class="sxs-lookup"><span data-stu-id="1f519-111">The low-order word is a handle to a global memory object containing a [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure with the data and additional information.</span></span> <span data-ttu-id="1f519-112">El identificador se debe establecer en **null** si el servidor notifica al cliente que el valor del elemento de datos ha cambiado durante un vínculo de datos semiactivos.</span><span class="sxs-lookup"><span data-stu-id="1f519-112">The handle should be set to **NULL** if the server is notifying the client that the data-item value has changed during a warm data link.</span></span> <span data-ttu-id="1f519-113">El cliente establece un vínculo en caliente mediante el envío de un mensaje de [**\_ \_ notificación de WM DDE**](wm-dde-advise.md) con el conjunto de bits **fDeferUpd** .</span><span class="sxs-lookup"><span data-stu-id="1f519-113">A warm link is established by the client sending a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message with the **fDeferUpd** bit set.</span></span>

<span data-ttu-id="1f519-114">La palabra de orden superior contiene un átomo que identifica el elemento de datos para el que se envían los datos o la notificación.</span><span class="sxs-lookup"><span data-stu-id="1f519-114">The high-order word contains an atom that identifies the data item for which the data or notification is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f519-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f519-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="1f519-116">Config</span><span class="sxs-lookup"><span data-stu-id="1f519-116">Posting</span></span>

<span data-ttu-id="1f519-117">La aplicación de servidor asigna el objeto de memoria global mediante la función [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="1f519-117">The server application allocates the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="1f519-118">Asigna el átomo mediante la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="1f519-118">It allocates the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="1f519-119">El servidor debe crear o reutilizar el parámetro *lParam* de **\_ \_ datos DDE de WM** llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="1f519-119">The server must create or reuse the **WM\_DDE\_DATA** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="1f519-120">Si la aplicación receptora (cliente) responde con un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo, la aplicación de posting (servidor) debe eliminar el objeto de memoria global; de lo contrario, el cliente debe eliminar el objeto después de extraer su contenido mediante una llamada a la función [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) .</span><span class="sxs-lookup"><span data-stu-id="1f519-120">If the receiving (client) application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the posting (server) application must delete the global memory object; otherwise, the client must delete the object after extracting its contents by calling the [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) function.</span></span>

<span data-ttu-id="1f519-121">Si la aplicación de servidor establece el miembro **fRelease** de la estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) en **false**, el servidor es responsable de eliminar el objeto al recibir una confirmación positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="1f519-121">If the server application sets the **fRelease** member of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**, the server is responsible for deleting the object upon receiving either a positive or negative acknowledgment.</span></span>

<span data-ttu-id="1f519-122">La aplicación de servidor no debe establecer los miembros **fAckReq** y **fRelease** de la estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) en **false**.</span><span class="sxs-lookup"><span data-stu-id="1f519-122">The server application should not set both the **fAckReq** and **fRelease** members of the [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) structure to **FALSE**.</span></span> <span data-ttu-id="1f519-123">Si ambos miembros están establecidos en **false**, no es posible que el servidor determine Cuándo se debe eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="1f519-123">If both members are set to **FALSE**, it is impossible for the server to determine when to delete the object.</span></span>

### <a name="receiving"></a><span data-ttu-id="1f519-124">Recepción</span><span class="sxs-lookup"><span data-stu-id="1f519-124">Receiving</span></span>

<span data-ttu-id="1f519-125">Si **fAckReq** es **true**, la aplicación cliente debe exponer el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para responder positiva o negativamente.</span><span class="sxs-lookup"><span data-stu-id="1f519-125">If **fAckReq** is **TRUE**, the client application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="1f519-126">Al publicar **la \_ \_ confirmación de WM DDE**, el cliente puede volver a usar el átomo, o bien puede eliminarlo y crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="1f519-126">When posting **WM\_DDE\_ACK**, the client can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="1f519-127">El cliente debe crear o volver a usar el parámetro *lParam* de la [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) mediante una llamada a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="1f519-127">The client must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="1f519-128">Si **fAckReq** es **false**, la aplicación cliente debe eliminar el átomo.</span><span class="sxs-lookup"><span data-stu-id="1f519-128">If **fAckReq** is **FALSE**, the client application should delete the atom.</span></span>

<span data-ttu-id="1f519-129">Si la aplicación de publicación especifica el objeto de memoria global como **null**, la aplicación receptora puede solicitar al servidor que envíe los datos mediante la publicación de un mensaje de [**solicitud de \_ DDE \_ de WM**](wm-dde-request.md) .</span><span class="sxs-lookup"><span data-stu-id="1f519-129">If the posting application specified global memory object as **NULL**, the receiving application can request the server to send the data by posting a [**WM\_DDE\_REQUEST**](wm-dde-request.md) message.</span></span>

<span data-ttu-id="1f519-130">Después de procesar un mensaje de **\_ \_ datos de DDE de WM** en el que el objeto de memoria global no es **null**, el cliente debe liberar el objeto, a menos que se cumpla una de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="1f519-130">After processing a **WM\_DDE\_DATA** message in which the global memory object is not **NULL**, the client should free the object, unless one of the following conditions is true:</span></span>

-   <span data-ttu-id="1f519-131">El miembro **fRelease** es **false**.</span><span class="sxs-lookup"><span data-stu-id="1f519-131">The **fRelease** member is **FALSE**.</span></span>
-   <span data-ttu-id="1f519-132">El miembro **fRelease** es **true**, pero la aplicación cliente responde con un mensaje de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo.</span><span class="sxs-lookup"><span data-stu-id="1f519-132">The **fRelease** member is **TRUE**, but the client application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f519-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f519-133">Requirements</span></span>



| <span data-ttu-id="1f519-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f519-134">Requirement</span></span> | <span data-ttu-id="1f519-135">Value</span><span class="sxs-lookup"><span data-stu-id="1f519-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f519-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f519-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1f519-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1f519-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1f519-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f519-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1f519-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1f519-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1f519-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f519-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f519-141"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f519-141"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f519-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f519-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f519-143">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1f519-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1f519-144">**DDEDATA**</span><span class="sxs-lookup"><span data-stu-id="1f519-144">**DDEDATA**</span></span>](/windows/desktop/api/Dde/ns-dde-ddedata)
</dt> <dt>

[<span data-ttu-id="1f519-145">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="1f519-145">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="1f519-146">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="1f519-146">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="1f519-147">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="1f519-147">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="1f519-148">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="1f519-148">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="1f519-149">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="1f519-149">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="1f519-150">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="1f519-150">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="1f519-151">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="1f519-151">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="1f519-152">**\_confirmación de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1f519-152">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="1f519-153">**\_aviso de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1f519-153">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="1f519-154">**hiperdinámico de WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f519-154">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="1f519-155">**\_solicitud de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1f519-155">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

<span data-ttu-id="1f519-156">**Vista**</span><span class="sxs-lookup"><span data-stu-id="1f519-156">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1f519-157">Acerca de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="1f519-157">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

