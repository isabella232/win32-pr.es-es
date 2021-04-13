---
title: Mensaje de WM_DDE_UNADVISE (DDE. h)
description: Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un \_ \_ mensaje de desaconsejar DDE de WM para informar a una aplicación de servidor DDE de que el elemento especificado o un formato de Portapapeles determinado para el elemento ya no debe actualizarse.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- Intercambio de datos de mensajes de WM_DDE_UNADVISE
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492197"
---
# <a name="wm_dde_unadvise-message"></a><span data-ttu-id="f5033-104">Mensaje de no notificación de DDE de WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="f5033-104">WM\_DDE\_UNADVISE message</span></span>

<span data-ttu-id="f5033-105">Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un mensaje de **\_ \_ desaconsejar DDE de WM** para informar a una aplicación de servidor DDE de que el elemento especificado o un formato de Portapapeles determinado para el elemento ya no debe actualizarse.</span><span class="sxs-lookup"><span data-stu-id="f5033-105">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_UNADVISE** message to inform a DDE server application that the specified item or a particular clipboard format for the item should no longer be updated.</span></span> <span data-ttu-id="f5033-106">Esto finaliza el vínculo de datos activo o activo para el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="f5033-106">This terminates the warm or hot data link for the specified item.</span></span>

<span data-ttu-id="f5033-107">Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="f5033-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a><span data-ttu-id="f5033-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5033-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5033-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5033-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5033-110">Identificador de la ventana de cliente que envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5033-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="f5033-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5033-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5033-112">La palabra de orden inferior especifica el formato del Portapapeles del elemento para el que se retira la solicitud de actualización.</span><span class="sxs-lookup"><span data-stu-id="f5033-112">The low-order word specifies the clipboard format of the item for which the update request is being retracted.</span></span> <span data-ttu-id="f5033-113">Si es **null**, todas las conversaciones [**de \_ \_ notificaciones de DDE de WM**](wm-dde-advise.md) activa para el elemento se terminarán.</span><span class="sxs-lookup"><span data-stu-id="f5033-113">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) conversations for the item are to be terminated.</span></span>

<span data-ttu-id="f5033-114">La palabra de orden superior contiene un átomo global que identifica el elemento para el que se retira la solicitud de actualización.</span><span class="sxs-lookup"><span data-stu-id="f5033-114">The high-order word contains a global atom that identifies the item for which the update request is being retracted.</span></span> <span data-ttu-id="f5033-115">Si es **null**, se terminarán todos los vínculos de [**aviso de WM \_ DDE \_**](wm-dde-advise.md) activos asociados a la conversación.</span><span class="sxs-lookup"><span data-stu-id="f5033-115">If this is **NULL**, all active [**WM\_DDE\_ADVISE**](wm-dde-advise.md) links associated with the conversation are to be terminated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5033-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5033-116">Remarks</span></span>

<span data-ttu-id="f5033-117">La aplicación cliente asigna la palabra de orden superior de *lParam* mediante una llamada a la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="f5033-117">The client application allocates the high-order word of *lParam* by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

<span data-ttu-id="f5033-118">La aplicación de servidor envía el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para responder de forma positiva o negativa.</span><span class="sxs-lookup"><span data-stu-id="f5033-118">The server application posts the [**WM\_DDE\_ACK**](wm-dde-ack.md) message to respond positively or negatively.</span></span> <span data-ttu-id="f5033-119">Al publicar **la \_ \_ confirmación de WM DDE**, el servidor puede volver a usar el átomo, o bien puede eliminar el átomo y crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="f5033-119">When posting **WM\_DDE\_ACK**, the server can either reuse the atom, or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5033-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5033-120">Requirements</span></span>



| <span data-ttu-id="f5033-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5033-121">Requirement</span></span> | <span data-ttu-id="f5033-122">Value</span><span class="sxs-lookup"><span data-stu-id="f5033-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5033-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5033-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f5033-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f5033-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f5033-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5033-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f5033-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f5033-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f5033-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5033-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5033-128"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5033-128"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5033-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5033-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="f5033-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f5033-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f5033-131">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="f5033-131">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="f5033-132">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f5033-132">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="f5033-133">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="f5033-133">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="f5033-134">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f5033-134">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="f5033-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="f5033-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="f5033-136">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="f5033-136">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="f5033-137">**\_confirmación de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f5033-137">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="f5033-138">**\_aviso de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f5033-138">**WM\_DDE\_ADVISE**</span></span>](wm-dde-advise.md)
</dt> <dt>

<span data-ttu-id="f5033-139">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f5033-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f5033-140">Acerca de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="f5033-140">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

