---
title: Método IMsRdpClient7 GetStatusText (OpenService. h)
description: Recupera el texto de estado para el código de estado especificado.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- Método GetStatusText Servicios de Escritorio remoto
- Método GetStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método GetStatusText
- Método GetStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método GetStatusText
- Método GetStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método GetStatusText
- Método GetStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método GetStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820628bfba59ec980e5128b9d9df3ee21b49a064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802756"
---
# <a name="imsrdpclient7getstatustext-method"></a><span data-ttu-id="21259-112">IMsRdpClient7:: GetStatusText (método)</span><span class="sxs-lookup"><span data-stu-id="21259-112">IMsRdpClient7::GetStatusText method</span></span>

<span data-ttu-id="21259-113">Recupera el texto de estado para el código de estado especificado.</span><span class="sxs-lookup"><span data-stu-id="21259-113">Retrieves the status text for the specified status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="21259-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21259-114">Syntax</span></span>


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a><span data-ttu-id="21259-115">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21259-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21259-116">*StatusCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="21259-116">*statusCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21259-117">Un **uint** que especifica el código de estado para el que se va a recuperar el texto.</span><span class="sxs-lookup"><span data-stu-id="21259-117">A **UINT** that specifies the status code to retrieve the text for.</span></span>

</dd> <dt>

<span data-ttu-id="21259-118">*pBstrStatusText* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="21259-118">*pBstrStatusText* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="21259-119">Dirección de un **BSTR** que recibe el texto de estado.</span><span class="sxs-lookup"><span data-stu-id="21259-119">The address of a **BSTR** that receives the status text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21259-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21259-120">Return value</span></span>

<span data-ttu-id="21259-121">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="21259-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21259-122">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21259-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="21259-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21259-123">Requirements</span></span>



| <span data-ttu-id="21259-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="21259-124">Requirement</span></span> | <span data-ttu-id="21259-125">Value</span><span class="sxs-lookup"><span data-stu-id="21259-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21259-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21259-126">Minimum supported client</span></span><br/> | <span data-ttu-id="21259-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="21259-127">Windows 7</span></span><br/>                                                                     |
| <span data-ttu-id="21259-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="21259-128">Minimum supported server</span></span><br/> | <span data-ttu-id="21259-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="21259-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="21259-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21259-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="21259-131"><dt>OpenService. h</dt></span><span class="sxs-lookup"><span data-stu-id="21259-131"><dt>Openservice.h</dt></span></span> </dl> |
| <span data-ttu-id="21259-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="21259-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="21259-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21259-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="21259-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="21259-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21259-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21259-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="21259-136">IID</span><span class="sxs-lookup"><span data-stu-id="21259-136">IID</span></span><br/>                      | <span data-ttu-id="21259-137">IID \_ IMsRdpClient7 se define como b2a5b5ce-3461-444A-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="21259-137">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="21259-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="21259-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21259-139">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="21259-139">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="21259-140">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="21259-140">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="21259-141">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="21259-141">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="21259-142">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="21259-142">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





