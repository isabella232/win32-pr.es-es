---
title: IMsRdpClient9 detachEvent, método
description: Desasocia un evento.
ms.assetid: 6a3ca713-1d5c-4070-a527-ad4f532a4cbf
ms.tgt_platform: multiple
keywords:
- método detachEvent Servicios de Escritorio remoto
- método detachEvent Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método detachEvent
- método detachEvent Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método detachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.detachEvent
- IMsRdpClient10.detachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399611ea526338f4cfe40ef3a4d6543bf27f134a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149923"
---
# <a name="imsrdpclient9detachevent-method"></a><span data-ttu-id="95d30-108">IMsRdpClient9::d método etachEvent</span><span class="sxs-lookup"><span data-stu-id="95d30-108">IMsRdpClient9::detachEvent method</span></span>

<span data-ttu-id="95d30-109">Desasocia un evento.</span><span class="sxs-lookup"><span data-stu-id="95d30-109">Detaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d30-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95d30-110">Syntax</span></span>


```C++
HRESULT detachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="95d30-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95d30-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d30-112">*eventName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95d30-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d30-113">Nombre del evento.</span><span class="sxs-lookup"><span data-stu-id="95d30-113">Name of the event.</span></span>

</dd> <dt>

<span data-ttu-id="95d30-114">*devolución de llamada* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="95d30-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d30-115">Devolución de llamada asociada al evento.</span><span class="sxs-lookup"><span data-stu-id="95d30-115">The callback associated with the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d30-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95d30-116">Return value</span></span>

<span data-ttu-id="95d30-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="95d30-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="95d30-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="95d30-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="95d30-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95d30-119">Requirements</span></span>



| <span data-ttu-id="95d30-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d30-120">Requirement</span></span> | <span data-ttu-id="95d30-121">Value</span><span class="sxs-lookup"><span data-stu-id="95d30-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d30-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95d30-122">Minimum supported client</span></span><br/> | <span data-ttu-id="95d30-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="95d30-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="95d30-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95d30-124">Minimum supported server</span></span><br/> | <span data-ttu-id="95d30-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="95d30-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="95d30-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="95d30-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="95d30-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95d30-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="95d30-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95d30-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95d30-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95d30-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="95d30-130">IID</span><span class="sxs-lookup"><span data-stu-id="95d30-130">IID</span></span><br/>                      | <span data-ttu-id="95d30-131">CLSID \_ MsRdpClient9 se define como 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="95d30-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="95d30-132">CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="95d30-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="95d30-133">IID \_ IMsRdpClient9 se define como 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="95d30-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="95d30-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="95d30-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d30-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="95d30-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="95d30-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="95d30-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 





