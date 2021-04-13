---
title: IMsRdpClient8 método de reconexión
description: Vuelve a conectarse a la sesión remota con el nuevo ancho y alto del escritorio.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Método de reconexión Servicios de Escritorio remoto
- Método de reconexión Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método de reconexión
- Método de reconexión Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método de reconexión
- Método de reconexión Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método de reconexión
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535584"
---
# <a name="imsrdpclient8reconnect-method"></a><span data-ttu-id="d8df0-110">IMsRdpClient8:: reconnect (método)</span><span class="sxs-lookup"><span data-stu-id="d8df0-110">IMsRdpClient8::Reconnect method</span></span>

<span data-ttu-id="d8df0-111">Vuelve a conectarse a la sesión remota con el nuevo ancho y alto del escritorio.</span><span class="sxs-lookup"><span data-stu-id="d8df0-111">Reconnects to the remote session with the new desktop width and height.</span></span> <span data-ttu-id="d8df0-112">El control ya debe estar conectado a una sesión remota para que este método se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8df0-112">The control must already be connected to a remote session for this method to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8df0-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8df0-113">Syntax</span></span>


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a><span data-ttu-id="d8df0-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8df0-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8df0-115">*ulWidth* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8df0-115">*ulWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8df0-116">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="d8df0-116">Type: **ULONG**</span></span>

<span data-ttu-id="d8df0-117">Nuevo ancho del escritorio, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="d8df0-117">The new desktop width, in pixels.</span></span> <span data-ttu-id="d8df0-118">Vea la propiedad [**DesktopWidth**](imstscax-desktopwidth.md) para conocer las restricciones de valor.</span><span class="sxs-lookup"><span data-stu-id="d8df0-118">See the [**DesktopWidth**](imstscax-desktopwidth.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="d8df0-119">*ulHeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8df0-119">*ulHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8df0-120">Tipo: **ULong**</span><span class="sxs-lookup"><span data-stu-id="d8df0-120">Type: **ULONG**</span></span>

<span data-ttu-id="d8df0-121">El nuevo alto del escritorio, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="d8df0-121">The new desktop height, in pixels.</span></span> <span data-ttu-id="d8df0-122">Vea la propiedad [**DesktopHeight**](imstscax-desktopheight.md) para conocer las restricciones de valor.</span><span class="sxs-lookup"><span data-stu-id="d8df0-122">See the [**DesktopHeight**](imstscax-desktopheight.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="d8df0-123">*pReconnectStatus* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d8df0-123">*pReconnectStatus* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d8df0-124">Tipo: \**[**ControlReconnectStatus**](controlreconnectstatus.md) \** _</span><span class="sxs-lookup"><span data-stu-id="d8df0-124">Type: \**[**ControlReconnectStatus**](controlreconnectstatus.md)\** _</span></span>

<span data-ttu-id="d8df0-125">Un puntero a una variable [_ *ControlReconnectStatus* \*](controlreconnectstatus.md) que recibe el estado de la operación de reconexión.</span><span class="sxs-lookup"><span data-stu-id="d8df0-125">A pointer to a [_ *ControlReconnectStatus*\*](controlreconnectstatus.md) variable that receives the status of the reconnect operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8df0-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8df0-126">Return value</span></span>

<span data-ttu-id="d8df0-127">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d8df0-127">Type: **HRESULT**</span></span>

<span data-ttu-id="d8df0-128">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d8df0-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8df0-129">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8df0-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8df0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8df0-130">Requirements</span></span>



| <span data-ttu-id="d8df0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8df0-131">Requirement</span></span> | <span data-ttu-id="d8df0-132">Value</span><span class="sxs-lookup"><span data-stu-id="d8df0-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8df0-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8df0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d8df0-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d8df0-134">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="d8df0-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8df0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d8df0-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d8df0-136">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="d8df0-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d8df0-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8df0-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8df0-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d8df0-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8df0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8df0-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8df0-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d8df0-141">IID</span><span class="sxs-lookup"><span data-stu-id="d8df0-141">IID</span></span><br/>                      | <span data-ttu-id="d8df0-142">IID \_ IMsRdpClient8 se define como 4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="d8df0-142">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d8df0-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8df0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8df0-144">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="d8df0-144">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="d8df0-145">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d8df0-145">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d8df0-146">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="d8df0-146">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="d8df0-147">**ControlReconnectStatus**</span><span class="sxs-lookup"><span data-stu-id="d8df0-147">**ControlReconnectStatus**</span></span>](controlreconnectstatus.md)
</dt> </dl>

 

 





