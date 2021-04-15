---
title: Método IVMVirtualPCEvents OnEventLogged (VPCCOMInterfaces. h)
description: Recibe la notificación de que Windows Virtual PC registra un evento.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Método OnEventLogged Virtual PC
- Método OnEventLogged Virtual PC, interfaz IVMVirtualPCEvents
- Interfaz IVMVirtualPCEvents Virtual PC, método OnEventLogged
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534390"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a><span data-ttu-id="c0a2f-106">IVMVirtualPCEvents:: OnEventLogged (método)</span><span class="sxs-lookup"><span data-stu-id="c0a2f-106">IVMVirtualPCEvents::OnEventLogged method</span></span>

<span data-ttu-id="c0a2f-107">\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c0a2f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c0a2f-108">En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c0a2f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c0a2f-109">Recibe la notificación de que Windows Virtual PC registra un evento.</span><span class="sxs-lookup"><span data-stu-id="c0a2f-109">Receives notification that Windows Virtual PC logs an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0a2f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0a2f-110">Syntax</span></span>


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a><span data-ttu-id="c0a2f-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0a2f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0a2f-112">*logMessageID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c0a2f-112">*logMessageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0a2f-113">Identificador de mensaje del mensaje de registro de eventos que se registró.</span><span class="sxs-lookup"><span data-stu-id="c0a2f-113">The message identifier of the event log message that was logged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0a2f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0a2f-114">Return value</span></span>

<span data-ttu-id="c0a2f-115">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c0a2f-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c0a2f-116">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c0a2f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0a2f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0a2f-117">Remarks</span></span>

<span data-ttu-id="c0a2f-118">Se llama a este método cuando Windows Virtual PC registra un mensaje en el registro de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="c0a2f-118">This method is called when Windows Virtual PC logs a message to the Windows event log.</span></span> <span data-ttu-id="c0a2f-119">El programa cliente debe implementar este método de interfaz para recibir la notificación del evento **vmVirtualPCEvent \_ EventLogged** que se origina desde [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="c0a2f-119">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_EventLogged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0a2f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0a2f-120">Requirements</span></span>



| <span data-ttu-id="c0a2f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0a2f-121">Requirement</span></span> | <span data-ttu-id="c0a2f-122">Value</span><span class="sxs-lookup"><span data-stu-id="c0a2f-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a2f-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0a2f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a2f-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0a2f-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0a2f-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0a2f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a2f-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c0a2f-126">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c0a2f-127">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c0a2f-127">End of client support</span></span><br/>    | <span data-ttu-id="c0a2f-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0a2f-128">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c0a2f-129">Producto</span><span class="sxs-lookup"><span data-stu-id="c0a2f-129">Product</span></span><br/>                  | <span data-ttu-id="c0a2f-130">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c0a2f-130">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c0a2f-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0a2f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0a2f-132"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0a2f-132"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c0a2f-133">IID</span><span class="sxs-lookup"><span data-stu-id="c0a2f-133">IID</span></span><br/>                      | <span data-ttu-id="c0a2f-134">DIID \_ IVMVirtualPCEvents se define como efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="c0a2f-134">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="c0a2f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0a2f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0a2f-136">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="c0a2f-136">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

