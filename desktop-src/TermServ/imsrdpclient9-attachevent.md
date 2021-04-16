---
title: IMsRdpClient9 attachEvent, método
description: Adjunta un evento.
ms.assetid: 3a887aeb-a74f-4477-8cf3-8ac43a31fa26
ms.tgt_platform: multiple
keywords:
- Método attachEvent Servicios de Escritorio remoto
- Método attachEvent Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, Método attachEvent
- Método attachEvent Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, Método attachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.attachEvent
- IMsRdpClient10.attachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bd3fd518fba825c209a4170e6b314a7b774a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489136"
---
# <a name="imsrdpclient9attachevent-method"></a><span data-ttu-id="f4f92-108">IMsRdpClient9:: attachEvent (método)</span><span class="sxs-lookup"><span data-stu-id="f4f92-108">IMsRdpClient9::attachEvent method</span></span>

<span data-ttu-id="f4f92-109">Adjunta un evento.</span><span class="sxs-lookup"><span data-stu-id="f4f92-109">Attaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4f92-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4f92-110">Syntax</span></span>


```C++
HRESULT attachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="f4f92-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4f92-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4f92-112">*eventName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f4f92-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f92-113">Evento que se va a adjuntar.</span><span class="sxs-lookup"><span data-stu-id="f4f92-113">The event to attach.</span></span>

</dd> <dt>

<span data-ttu-id="f4f92-114">*devolución de llamada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f4f92-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4f92-115">La devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f4f92-115">The callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4f92-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4f92-116">Return value</span></span>

<span data-ttu-id="f4f92-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="f4f92-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f4f92-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4f92-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4f92-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4f92-119">Requirements</span></span>



| <span data-ttu-id="f4f92-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4f92-120">Requirement</span></span> | <span data-ttu-id="f4f92-121">Value</span><span class="sxs-lookup"><span data-stu-id="f4f92-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f92-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4f92-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f4f92-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f4f92-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="f4f92-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4f92-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f4f92-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f4f92-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="f4f92-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f4f92-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="f4f92-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4f92-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="f4f92-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f4f92-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4f92-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4f92-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="f4f92-130">IID</span><span class="sxs-lookup"><span data-stu-id="f4f92-130">IID</span></span><br/>                      | <span data-ttu-id="f4f92-131">CLSID \_ MsRdpClient9 se define como 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="f4f92-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="f4f92-132">CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="f4f92-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="f4f92-133">IID \_ IMsRdpClient9 se define como 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="f4f92-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4f92-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4f92-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f92-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="f4f92-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="f4f92-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f4f92-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 





