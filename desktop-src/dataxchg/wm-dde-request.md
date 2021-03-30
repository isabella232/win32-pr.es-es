---
title: Mensaje de WM_DDE_REQUEST (DDE. h)
description: Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un \_ \_ mensaje de solicitud de WM DDE a una aplicación de servidor DDE para solicitar el valor de un elemento de datos. Para enviar este mensaje, llame a la función PostMessage con los parámetros siguientes.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- Intercambio de datos de mensajes de WM_DDE_REQUEST
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801964"
---
# <a name="wm_dde_request-message"></a><span data-ttu-id="dd2bd-105">Mensaje de solicitud de \_ DDE de WM \_</span><span class="sxs-lookup"><span data-stu-id="dd2bd-105">WM\_DDE\_REQUEST message</span></span>

<span data-ttu-id="dd2bd-106">Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un mensaje de **\_ \_ solicitud de WM DDE** a una aplicación de servidor DDE para solicitar el valor de un elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="dd2bd-106">A Dynamic Data Exchange (DDE) client application posts a **WM\_DDE\_REQUEST** message to a DDE server application to request the value of a data item.</span></span>

<span data-ttu-id="dd2bd-107">Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="dd2bd-107">To post this message, call the [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) function with the following parameters.</span></span>


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a><span data-ttu-id="dd2bd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd2bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd2bd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dd2bd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd2bd-110">Identificador de la ventana de cliente que envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="dd2bd-110">A handle to the client window sending the message.</span></span>

</dd> <dt>

<span data-ttu-id="dd2bd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dd2bd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dd2bd-112">La palabra de orden inferior especifica un formato de Portapapeles estándar o registrado.</span><span class="sxs-lookup"><span data-stu-id="dd2bd-112">The low-order word specifies a standard or registered clipboard format.</span></span>

<span data-ttu-id="dd2bd-113">La palabra de orden superior contiene un átomo que identifica el elemento de datos solicitado desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="dd2bd-113">The high-order word contains an atom that identifies the data item requested from the server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd2bd-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dd2bd-114">Remarks</span></span>

### <a name="posting"></a><span data-ttu-id="dd2bd-115">Config</span><span class="sxs-lookup"><span data-stu-id="dd2bd-115">Posting</span></span>

<span data-ttu-id="dd2bd-116">La aplicación cliente asigna el átomo llamando a la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .</span><span class="sxs-lookup"><span data-stu-id="dd2bd-116">The client application allocates the atom by calling the [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) function.</span></span>

### <a name="receiving"></a><span data-ttu-id="dd2bd-117">Recepción</span><span class="sxs-lookup"><span data-stu-id="dd2bd-117">Receiving</span></span>

<span data-ttu-id="dd2bd-118">Si la aplicación receptora (servidor) puede satisfacer la solicitud, responde con un mensaje [**de \_ \_ datos de WM DDE**](wm-dde-data.md) que contiene los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="dd2bd-118">If the receiving (server) application can satisfy the request, it responds with a [**WM\_DDE\_DATA**](wm-dde-data.md) message containing the requested data.</span></span> <span data-ttu-id="dd2bd-119">De lo contrario, responde con un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo.</span><span class="sxs-lookup"><span data-stu-id="dd2bd-119">Otherwise, it responds with a negative [**WM\_DDE\_ACK**](wm-dde-ack.md) message.</span></span>

<span data-ttu-id="dd2bd-120">Cuando responde con un mensaje [**de \_ \_ datos DDE de WM**](wm-dde-data.md) o de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) , la aplicación de servidor puede reutilizar el átomo o eliminar el átomo y crear uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="dd2bd-120">When responding with either a [**WM\_DDE\_DATA**](wm-dde-data.md) or [**WM\_DDE\_ACK**](wm-dde-ack.md) message, the server application can either reuse the atom or it can delete the atom and create a new one.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd2bd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd2bd-121">Requirements</span></span>



| <span data-ttu-id="dd2bd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd2bd-122">Requirement</span></span> | <span data-ttu-id="dd2bd-123">Value</span><span class="sxs-lookup"><span data-stu-id="dd2bd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2bd-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd2bd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dd2bd-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dd2bd-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dd2bd-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd2bd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dd2bd-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dd2bd-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="dd2bd-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd2bd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd2bd-129"><dt>DDE. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd2bd-129"><dt>Dde.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd2bd-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd2bd-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="dd2bd-131">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="dd2bd-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dd2bd-132">**GlobalAddAtom**</span><span class="sxs-lookup"><span data-stu-id="dd2bd-132">**GlobalAddAtom**</span></span>](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[<span data-ttu-id="dd2bd-133">**PackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="dd2bd-133">**PackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[<span data-ttu-id="dd2bd-134">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="dd2bd-134">**PostMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="dd2bd-135">**ReuseDDElParam**</span><span class="sxs-lookup"><span data-stu-id="dd2bd-135">**ReuseDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[<span data-ttu-id="dd2bd-136">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="dd2bd-136">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[<span data-ttu-id="dd2bd-137">**UnpackDDElParam**</span><span class="sxs-lookup"><span data-stu-id="dd2bd-137">**UnpackDDElParam**</span></span>](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[<span data-ttu-id="dd2bd-138">**\_confirmación de DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="dd2bd-138">**WM\_DDE\_ACK**</span></span>](wm-dde-ack.md)
</dt> <dt>

[<span data-ttu-id="dd2bd-139">**\_datos DDE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="dd2bd-139">**WM\_DDE\_DATA**</span></span>](wm-dde-data.md)
</dt> <dt>

<span data-ttu-id="dd2bd-140">**Vista**</span><span class="sxs-lookup"><span data-stu-id="dd2bd-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dd2bd-141">Acerca de Intercambio dinámico de datos</span><span class="sxs-lookup"><span data-stu-id="dd2bd-141">About Dynamic Data Exchange</span></span>](about-dynamic-data-exchange.md)
</dt> </dl>

 

