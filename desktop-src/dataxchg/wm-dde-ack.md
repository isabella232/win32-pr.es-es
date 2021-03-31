---
title: Mensaje de WM_DDE_ACK (DDE. h)
description: El \_ mensaje de \_ confirmación de DDE de WM notifica a una aplicación intercambio dinámico de datos (DDE) de la recepción y el procesamiento de los siguientes mensajes WM DDE, de WM, de ejecución, de WM DDE o de la \_ \_ \_ \_ solicitud de \_ \_ \_ \_ \_ \_ \_ \_ \_ DDE de WM \_ (en algunos casos). Para enviar este mensaje, llame a la función PostMessage con los parámetros siguientes.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- Intercambio de datos de mensajes de WM_DDE_ACK
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079292"
---
# <a name="wm_dde_ack-message"></a><span data-ttu-id="8f690-105">Mensaje de confirmación de \_ DDE de WM \_</span><span class="sxs-lookup"><span data-stu-id="8f690-105">WM\_DDE\_ACK message</span></span>

<span data-ttu-id="8f690-106">El mensaje de **\_ \_ confirmación de DDE de WM** notifica a una aplicación intercambio dinámico de datos (DDE) de la recepción y el procesamiento de los mensajes siguientes: [**WM \_ DDE \_**](wm-dde-poke.md), error de WM, [**\_ \_ ejecución**](wm-dde-execute.md)de WM DDE, [**datos de WM \_ DDE \_**](wm-dde-data.md), [**\_ \_ aviso de DDE**](wm-dde-advise.md)de WM, [**\_ \_ desaconsejar**](wm-dde-unadvise.md)DDE de WM, [**\_ \_ Inicio de WM DDE**](wm-dde-initiate.md)o [**\_ \_ solicitud de DDE de WM**](wm-dde-request.md) (en algunos casos).</span><span class="sxs-lookup"><span data-stu-id="8f690-106">The **WM\_DDE\_ACK** message notifies a Dynamic Data Exchange (DDE) application of the receipt and processing of the following messages: [**WM\_DDE\_POKE**](wm-dde-poke.md), [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_ADVISE**](wm-dde-advise.md), [**WM\_DDE\_UNADVISE**](wm-dde-unadvise.md), [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), or [**WM\_DDE\_REQUEST**](wm-dde-request.md) (in some cases).</span></span>

<span data-ttu-id="8f690-107">Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="8f690-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a><span data-ttu-id="8f690-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f690-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f690-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f690-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f690-110">Cuando se responde a [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md), este parámetro es un identificador de la ventana del servidor que envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8f690-110">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), this parameter is a handle to the server window sending the message.</span></span>

<span data-ttu-id="8f690-111">Cuando se responde a [**WM \_ DDE \_ Execute**](wm-dde-execute.md), este parámetro es un identificador de la ventana del servidor que publica el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8f690-111">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), this parameter is a handle to the server window posting the message.</span></span>

<span data-ttu-id="8f690-112">Al responder a todos los demás mensajes, este parámetro es un identificador de la ventana de cliente o de servidor que publica el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8f690-112">When replying to all other messages, this parameter is a handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="8f690-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f690-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f690-114">Cuando se responde a [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md), la palabra de orden inferior contiene un átomo que identifica la aplicación de respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f690-114">When responding to [**WM\_DDE\_INITIATE**](wm-dde-initiate.md), the low-order word contains an atom that identifies the replying application.</span></span> <span data-ttu-id="8f690-115">La palabra de orden superior contiene un átomo que identifica el tema para el que se está estableciendo una conversación.</span><span class="sxs-lookup"><span data-stu-id="8f690-115">The high-order word contains an atom that identifies the topic for which a conversation is being established.</span></span>

<span data-ttu-id="8f690-116">Cuando se responde a [**WM \_ DDE \_ Execute**](wm-dde-execute.md), la palabra de orden inferior especifica una estructura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contiene una serie de marcas que indican el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f690-116">When responding to [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="8f690-117">La palabra de orden superior es un identificador de un objeto de memoria global que contiene la cadena de comandos que se recibió en el mensaje de **\_ \_ ejecución de WM DDE** .</span><span class="sxs-lookup"><span data-stu-id="8f690-117">The high-order word is a handle to a global memory object that contains the command string that was received in the **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="8f690-118">Al responder a todos los demás mensajes, la palabra de orden inferior especifica una estructura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contiene una serie de marcas que indican el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f690-118">When replying to all other messages, the low-order word specifies a [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) structure containing a series of flags that indicate the status of the response.</span></span> <span data-ttu-id="8f690-119">La palabra de orden superior contiene un átomo global que identifica el nombre del elemento de datos para el que se envía la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f690-119">The high-order word contains a global atom that identifies the name of the data item for which the response is sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f690-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f690-120">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="8f690-121">Config</span><span class="sxs-lookup"><span data-stu-id="8f690-121">Posting</span></span>

<span data-ttu-id="8f690-122">Excepto en respuesta al mensaje [**de \_ \_ Inicio de WM DDE**](wm-dde-initiate.md) , la aplicación envía el mensaje de **confirmación de WM \_ DDE \_** mediante una llamada a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , no mediante una llamada a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .</span><span class="sxs-lookup"><span data-stu-id="8f690-122">Except in response to the [**WM\_DDE\_INITIATE**](wm-dde-initiate.md) message, the application posts the **WM\_DDE\_ACK** message by calling the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function, not by calling the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function.</span></span> <span data-ttu-id="8f690-123">Al responder a **WM \_ DDE \_ iniciar**, la aplicación envía el mensaje de **\_ \_ confirmación de WM DDE** llamando a **SendMessage**.</span><span class="sxs-lookup"><span data-stu-id="8f690-123">When responding to **WM\_DDE\_INITIATE**, the application sends the **WM\_DDE\_ACK** message by calling **SendMessage**.</span></span> <span data-ttu-id="8f690-124">En este caso, ni el Atom del nombre de la aplicación ni el Atom del nombre del tema deben ser **null** (aunque el mensaje de **Inicio de WM \_ \_ DDE** especifique átomos **null** ).</span><span class="sxs-lookup"><span data-stu-id="8f690-124">In this case, neither the application-name atom nor the topic-name atom should be **NULL** (even if the **WM\_DDE\_INITIATE** message specified **NULL** atoms).</span></span>

<span data-ttu-id="8f690-125">Al confirmar cualquier mensaje con un átomo que lo acompañe, la confirmación de **la \_ \_ confirmación DDE de WM** de aplicación puede volver a usar el átomo que acompaña al mensaje original, o bien puede eliminarlo y crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="8f690-125">When acknowledging any message with an accompanying atom, the application posting **WM\_DDE\_ACK** can either reuse the atom that accompanied the original message, or it can delete it and create a new one.</span></span>

<span data-ttu-id="8f690-126">Cuando se confirma [**la \_ \_ ejecución de WM DDE**](wm-dde-execute.md), la aplicación que envía la **confirmación de WM \_ DDE \_** debe volver a usar el objeto de memoria global identificado en el mensaje de **ejecución de WM \_ \_ DDE** original.</span><span class="sxs-lookup"><span data-stu-id="8f690-126">When acknowledging [**WM\_DDE\_EXECUTE**](wm-dde-execute.md), the application that posts **WM\_DDE\_ACK** should reuse the global memory object identified in the original **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="8f690-127">Todos los mensajes de **\_ \_ confirmación DDE de WM** publicados deben crear o volver a usar el parámetro *lParam* llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="8f690-127">All posted **WM\_DDE\_ACK** messages must create or reuse the *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="8f690-128">Si una aplicación ha iniciado la finalización de una conversación mediante la publicación de la terminación de [**WM \_ DDE \_**](wm-dde-terminate.md) y está esperando la confirmación, la aplicación en espera no debe confirmar (positiva o negativamente) los mensajes posteriores enviados por la otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="8f690-128">If an application has initiated the termination of a conversation by posting [**WM\_DDE\_TERMINATE**](wm-dde-terminate.md) and is awaiting confirmation, the waiting application should not acknowledge (positively or negatively) any subsequent messages sent by the other application.</span></span> <span data-ttu-id="8f690-129">La aplicación en espera debe eliminar cualquier átomo o objeto de memoria compartida recibido en estos mensajes que intervienen.</span><span class="sxs-lookup"><span data-stu-id="8f690-129">The waiting application should delete any atoms or shared memory objects received in these intervening messages.</span></span> <span data-ttu-id="8f690-130">Los objetos de memoria no deben liberarse si la marca **fRelease** está establecida en **false** en los mensajes de [**\_ \_ datos DDE**](wm-dde-data.md) de WM y WM [**\_ DDE \_**](wm-dde-poke.md) .</span><span class="sxs-lookup"><span data-stu-id="8f690-130">Memory objects should not be freed if the **fRelease** flag is set to **FALSE** in [**WM\_DDE\_POKE**](wm-dde-poke.md) and [**WM\_DDE\_DATA**](wm-dde-data.md) messages.</span></span>

### <a name="receiving"></a><span data-ttu-id="8f690-131">Recepción</span><span class="sxs-lookup"><span data-stu-id="8f690-131">Receiving</span></span>

<span data-ttu-id="8f690-132">La aplicación que recibe un mensaje de **\_ \_ confirmación de WM DDE** debe eliminar todos los átomos que acompañan al mensaje.</span><span class="sxs-lookup"><span data-stu-id="8f690-132">The application that receives a **WM\_DDE\_ACK** message should delete all atoms accompanying the message.</span></span> <span data-ttu-id="8f690-133">Si la aplicación recibe una **\_ \_ confirmación de WM DDE** en respuesta a un mensaje con un objeto de memoria global que lo acompaña, y el objeto se envió con las marcas **fRelease** establecidas en **false**, la aplicación es responsable de eliminar el objeto.</span><span class="sxs-lookup"><span data-stu-id="8f690-133">If the application receives a **WM\_DDE\_ACK** in response to a message with an accompanying global memory object, and the object was sent with the **fRelease** flags set to **FALSE**, the application is responsible for deleting the object.</span></span>

<span data-ttu-id="8f690-134">Si la aplicación recibe un mensaje **de \_ \_ confirmación DDE de WM** negativo publicado en respuesta a un mensaje de [**\_ \_ notificación de DDE de WM**](wm-dde-advise.md) , la aplicación debe eliminar el objeto de memoria global expuesto con el mensaje de **\_ \_ aviso de DDE de WM** original.</span><span class="sxs-lookup"><span data-stu-id="8f690-134">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_ADVISE**](wm-dde-advise.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_ADVISE** message.</span></span> <span data-ttu-id="8f690-135">Si la aplicación recibe un mensaje **de \_ \_ confirmación de DDE de WM** negativo expuesto en respuesta a un mensaje [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM \_ DDE \_**](wm-dde-poke.md), o de [**\_ \_ ejecución de WM DDE**](wm-dde-execute.md) , la aplicación debe eliminar el objeto de memoria global que se ha publicado con el mensaje de **\_ \_ ejecución** de **\_ \_ datos DDE** de WM original, de **WM \_ DDE \_** o de WM.</span><span class="sxs-lookup"><span data-stu-id="8f690-135">If the application receives a negative **WM\_DDE\_ACK** message posted in reply to a [**WM\_DDE\_DATA**](wm-dde-data.md), [**WM\_DDE\_POKE**](wm-dde-poke.md), or [**WM\_DDE\_EXECUTE**](wm-dde-execute.md) message, the application should delete the global memory object posted with the original **WM\_DDE\_DATA**, **WM\_DDE\_POKE**, or **WM\_DDE\_EXECUTE** message.</span></span>

<span data-ttu-id="8f690-136">La aplicación que recibe un mensaje **de \_ \_ confirmación de DDE de WM** publicado debe liberar el parámetro *lParam* mediante la función [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .</span><span class="sxs-lookup"><span data-stu-id="8f690-136">The application that receives a posted **WM\_DDE\_ACK** message must free the *lParam* parameter by using the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f690-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f690-137">Requirements</span></span>



| <span data-ttu-id="8f690-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f690-138">Requirement</span></span> | <span data-ttu-id="8f690-139">Value</span><span class="sxs-lookup"><span data-stu-id="8f690-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f690-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f690-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8f690-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8f690-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8f690-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8f690-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8f690-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8f690-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8f690-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f690-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f690-145"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f690-145"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f690-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f690-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f690-147">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8f690-147">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8f690-148">**DDEACK**</span><span class="sxs-lookup"><span data-stu-id="8f690-148">**DDEACK**</span></span>](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[<span data-ttu-id="8f690-149">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="8f690-149">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="8f690-150">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="8f690-150">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="8f690-151">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="8f690-151">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="8f690-152">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="8f690-152">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="8f690-153">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="8f690-153">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="8f690-154">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="8f690-154">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="8f690-155">**\_aviso de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="8f690-155">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

[<span data-ttu-id="8f690-156">**\_datos DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="8f690-156">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="8f690-157">**ejecución de WM \_ DDE \_**</span><span class="sxs-lookup"><span data-stu-id="8f690-157">**WM\_DDE\_EXECUTE**</span></span>](wm-dde-execute.md)
</dt> <dt>

[<span data-ttu-id="8f690-158">**Inicio de WM \_ DDE \_**</span><span class="sxs-lookup"><span data-stu-id="8f690-158">**WM\_DDE\_INITIATE**</span></span>](wm-dde-initiate.md)
</dt> <dt>

[<span data-ttu-id="8f690-159">**hiperdinámico de WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8f690-159">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

[<span data-ttu-id="8f690-160">**\_solicitud de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="8f690-160">**WM\_DDE\_REQUEST**</span></span>](wm-dde-request.md)
</dt> <dt>

[<span data-ttu-id="8f690-161">**\_finalización de WM DDE \_**</span><span class="sxs-lookup"><span data-stu-id="8f690-161">**WM\_DDE\_TERMINATE**</span></span>](wm-dde-terminate.md)
</dt> <dt>

[<span data-ttu-id="8f690-162">**\_DESaconsejar DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="8f690-162">**WM\_DDE\_UNADVISE**</span></span>](wm-dde-unadvise.md)
</dt> <dt>

<span data-ttu-id="8f690-163">**Vista**</span><span class="sxs-lookup"><span data-stu-id="8f690-163">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8f690-164">Acerca de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="8f690-164">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

