---
title: Mensaje de WM_DDE_TERMINATE (DDE. h)
description: Una aplicación Intercambio dinámico de datos (DDE) (cliente o servidor) envía un \_ mensaje de finalización de WM DDE \_ para finalizar una conversación. Para enviar este mensaje, llame a la función PostMessage con los parámetros siguientes.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- Intercambio de datos de mensajes de WM_DDE_TERMINATE
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150160"
---
# <a name="wm_dde_terminate-message"></a><span data-ttu-id="f6892-105">Mensaje de terminación de WM \_ DDE \_</span><span class="sxs-lookup"><span data-stu-id="f6892-105">WM\_DDE\_TERMINATE message</span></span>

<span data-ttu-id="f6892-106">Una aplicación Intercambio dinámico de datos (DDE) (cliente o servidor) envía un mensaje de **\_ \_ finalización de WM DDE** para finalizar una conversación.</span><span class="sxs-lookup"><span data-stu-id="f6892-106">A Dynamic Data Exchange (DDE) application (client or server) posts a **WM\_DDE\_TERMINATE** message to terminate a conversation.</span></span>

<span data-ttu-id="f6892-107">Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="f6892-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a><span data-ttu-id="f6892-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6892-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6892-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6892-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6892-110">Identificador de la ventana de cliente o de servidor que publica el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f6892-110">A handle to the client or server window posting the message.</span></span>

</dd> <dt>

<span data-ttu-id="f6892-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6892-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6892-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="f6892-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6892-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6892-113">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="f6892-114">Config</span><span class="sxs-lookup"><span data-stu-id="f6892-114">Posting</span></span>

<span data-ttu-id="f6892-115">Mientras se espera la confirmación de la finalización, la aplicación de publicación no debe publicar ningún otro mensaje en la aplicación receptora.</span><span class="sxs-lookup"><span data-stu-id="f6892-115">While waiting for confirmation of the termination, the posting application should not post any other messages to the receiving application.</span></span> <span data-ttu-id="f6892-116">Si la aplicación emisora recibe mensajes (distintos de la **\_ \_ terminación de WM DDE**) de la aplicación receptora, debe eliminar todos los subconjuntos o objetos de memoria compartida que acompañan a los mensajes, excepto los objetos de memoria global asociados a los mensajes de [**\_ \_ datos dinámicos**](wm-dde-data.md) de WM o WM que no tienen el conjunto de miembros **fRelease** . [**\_ \_**](wm-dde-poke.md)</span><span class="sxs-lookup"><span data-stu-id="f6892-116">If the sending application receives messages (other than **WM\_DDE\_TERMINATE**) from the receiving application, it should delete any atoms or shared memory objects accompanying the messages, except global memory objects associated with [**WM\_DDE\_POKE**](wm-dde-poke.md) or [**WM\_DDE\_DATA**](wm-dde-data.md) messages that do not have the **fRelease** member set.</span></span>

### <a name="receiving"></a><span data-ttu-id="f6892-117">Recepción</span><span class="sxs-lookup"><span data-stu-id="f6892-117">Receiving</span></span>

<span data-ttu-id="f6892-118">La aplicación de cliente o de servidor debe responder mediante la publicación de un mensaje de **\_ \_ finalización de WM DDE** .</span><span class="sxs-lookup"><span data-stu-id="f6892-118">The client or server application should respond by posting a **WM\_DDE\_TERMINATE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6892-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6892-119">Requirements</span></span>



| <span data-ttu-id="f6892-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6892-120">Requirement</span></span> | <span data-ttu-id="f6892-121">Value</span><span class="sxs-lookup"><span data-stu-id="f6892-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6892-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6892-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f6892-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f6892-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f6892-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6892-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f6892-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f6892-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f6892-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6892-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6892-127"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6892-127"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6892-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6892-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="f6892-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f6892-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f6892-130">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="f6892-130">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="f6892-131">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="f6892-131">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="f6892-132">**\_datos DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f6892-132">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

[<span data-ttu-id="f6892-133">**hiperdinámico de WM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f6892-133">**WM\_DDE\_POKE**</span></span>](wm-dde-poke.md)
</dt> <dt>

<span data-ttu-id="f6892-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f6892-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f6892-135">Acerca de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="f6892-135">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

