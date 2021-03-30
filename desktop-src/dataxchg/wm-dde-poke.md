---
title: Mensaje de WM_DDE_POKE (DDE. h)
description: Una aplicación cliente Intercambio dinámico de datos (DDE) envía un mensaje de mensajes de envío de WM \_ DDE \_ a una aplicación de servidor DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- Intercambio de datos de mensajes de WM_DDE_POKE
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803920"
---
# <a name="wm_dde_poke-message"></a><span data-ttu-id="12b28-104">\_Mensaje de mensaje de error de WM DDE \_</span><span class="sxs-lookup"><span data-stu-id="12b28-104">WM\_DDE\_POKE message</span></span>

<span data-ttu-id="12b28-105">Una aplicación cliente Intercambio dinámico de datos (DDE) envía un mensaje de mensajes de envío de **WM \_ DDE \_** a una aplicación de servidor DDE.</span><span class="sxs-lookup"><span data-stu-id="12b28-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_POKE** message to a DDE server application.</span></span> <span data-ttu-id="12b28-106">Un cliente usa este mensaje para solicitar al servidor que acepte un elemento de datos no solicitado.</span><span class="sxs-lookup"><span data-stu-id="12b28-106">A client uses this message to request the server to accept an unsolicited data item.</span></span> <span data-ttu-id="12b28-107">Se espera que el servidor responda con un mensaje de [**\_ \_ confirmación de DDE de WM**](wm-dde-ack.md) que indica si aceptó el elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="12b28-107">The server is expected to reply with a [**WM\_DDE\_ACK**](wm-dde-ack.md) message indicating whether it accepted the data item.</span></span>

<span data-ttu-id="12b28-108">Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="12b28-108">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a><span data-ttu-id="12b28-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="12b28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12b28-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12b28-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12b28-111">Identificador de la ventana de cliente que publica el mensaje.</span><span class="sxs-lookup"><span data-stu-id="12b28-111">A handle to the client window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="12b28-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12b28-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12b28-113">La palabra de orden inferior es un identificador de un objeto de memoria global que contiene una estructura [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) con los datos e información adicional.</span><span class="sxs-lookup"><span data-stu-id="12b28-113">The low-order word is a handle to a global memory object containing a [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) structure with the data and additional information.</span></span>

<span data-ttu-id="12b28-114">La palabra de orden superior contiene un átomo global que identifica el elemento de datos para el que se envían los datos o la notificación.</span><span class="sxs-lookup"><span data-stu-id="12b28-114">The high-order word contains a global atom that identifies the data item for which the data or notification is being sent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12b28-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12b28-115">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="12b28-116">Config</span><span class="sxs-lookup"><span data-stu-id="12b28-116">Posting</span></span>

<span data-ttu-id="12b28-117">La aplicación cliente debe asignar memoria para el objeto de memoria global mediante la función [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) .</span><span class="sxs-lookup"><span data-stu-id="12b28-117">The client application must allocate memory for the global memory object using the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function.</span></span> <span data-ttu-id="12b28-118">La aplicación cliente debe eliminar el objeto si se cumple alguna de las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="12b28-118">The client application must delete the object if either of the following conditions is true:</span></span>

-   <span data-ttu-id="12b28-119">La aplicación de servidor responde con un mensaje [**de \_ \_ confirmación de DDE de WM**](wm-dde-ack.md) negativo.</span><span class="sxs-lookup"><span data-stu-id="12b28-119">The server application responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>
-   <span data-ttu-id="12b28-120">El miembro **fRelease** es **false**, pero la aplicación de servidor responde con una [**confirmación de WM \_ DDE \_**](wm-dde-ack.md)positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="12b28-120">The **fRelease** member is **FALSE**, but the server application responds with either a positive or negative [**WM\_DDE\_ACK**](wm-dde-ack.md).</span></span>

<span data-ttu-id="12b28-121">La aplicación cliente debe crear el átomo mediante la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="12b28-121">The client application must create the atom using the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="12b28-122">La aplicación cliente debe crear o reutilizar el parámetro *lParam* de **WM \_ DDE \_** , llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="12b28-122">The client application must create or reuse the **WM\_DDE\_POKE** *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="12b28-123">Recepción</span><span class="sxs-lookup"><span data-stu-id="12b28-123">Receiving</span></span>

<span data-ttu-id="12b28-124">La aplicación de servidor debe publicar el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para responder de forma positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="12b28-124">The server application should post the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="12b28-125">Al publicar **la \_ \_ confirmación de WM DDE**, el servidor puede volver a usar el átomo, o bien puede eliminarlo y crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="12b28-125">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete it and create a new one.</span></span>

<span data-ttu-id="12b28-126">El servidor debe crear o volver a usar el parámetro *lParam* de la [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) mediante una llamada a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .</span><span class="sxs-lookup"><span data-stu-id="12b28-126">The server must create or reuse the [**WM\_DDE\_ACK**](wm-dde-ack.md) *lParam* parameter by calling the [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) function or the [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) function.</span></span>

<span data-ttu-id="12b28-127">Para liberar el objeto de memoria global, el servidor debe llamar a la función [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) .</span><span class="sxs-lookup"><span data-stu-id="12b28-127">To free the global memory object, the server should call the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function.</span></span> <span data-ttu-id="12b28-128">Además, si el formato de los datos es [**CF \_ DSPMETAFILEPICT**](clipboard-formats.md) o **CF \_ METAFILEPICT**, el servidor también debe llamar a [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) con el identificador de metarchivo incrustado.</span><span class="sxs-lookup"><span data-stu-id="12b28-128">Also, if the data format is either [**CF\_DSPMETAFILEPICT**](clipboard-formats.md) or **CF\_METAFILEPICT**, the server must also call [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) with the embedded metafile handle.</span></span> <span data-ttu-id="12b28-129">Estos dos formatos tienen un nivel de direccionamiento indirecto adicional. es decir, una aplicación debe bloquear el objeto para obtener un puntero a un identificador y, a continuación, bloquear ese identificador para obtener un puntero a una estructura [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) y, por último, llamar a **DeleteMetaFile** con el identificador del miembro **hMF** de la estructura **METAFILEPICT** .</span><span class="sxs-lookup"><span data-stu-id="12b28-129">These two formats have an extra level of indirection; that is, an application must lock the object to get a pointer to a handle, then lock that handle to get a pointer to a [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) structure, and finally call **DeleteMetaFile** with the handle from the **hMF** member of the **METAFILEPICT** structure.</span></span>

<span data-ttu-id="12b28-130">Para liberar el objeto, el servidor debe llamar a la función [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .</span><span class="sxs-lookup"><span data-stu-id="12b28-130">To free the object, the server should call the [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="12b28-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12b28-131">Requirements</span></span>



| <span data-ttu-id="12b28-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="12b28-132">Requirement</span></span> | <span data-ttu-id="12b28-133">Value</span><span class="sxs-lookup"><span data-stu-id="12b28-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12b28-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12b28-134">Minimum supported client</span></span><br/> | <span data-ttu-id="12b28-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="12b28-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="12b28-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12b28-136">Minimum supported server</span></span><br/> | <span data-ttu-id="12b28-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="12b28-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="12b28-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="12b28-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="12b28-139"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12b28-139"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12b28-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="12b28-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="12b28-141">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="12b28-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="12b28-142">**DDEPOKE**</span><span class="sxs-lookup"><span data-stu-id="12b28-142">**DDEPOKE**</span></span>](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[<span data-ttu-id="12b28-143">**FreeDDElParam**</span><span class="sxs-lookup"><span data-stu-id="12b28-143">**FreeDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[<span data-ttu-id="12b28-144">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="12b28-144">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="12b28-145">**METAFILEPICT**</span><span class="sxs-lookup"><span data-stu-id="12b28-145">**METAFILEPICT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
</dt> <dt>

[<span data-ttu-id="12b28-146">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="12b28-146">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="12b28-147">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="12b28-147">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="12b28-148">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="12b28-148">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="12b28-149">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="12b28-149">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="12b28-150">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="12b28-150">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="12b28-151">**\_confirmación de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="12b28-151">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

<span data-ttu-id="12b28-152">**Vista**</span><span class="sxs-lookup"><span data-stu-id="12b28-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="12b28-153">Acerca de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="12b28-153">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

