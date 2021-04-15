---
title: IMsTscAxEvents OnRemoteDesktopSizeChange, método
description: Se llama para indicar que el tamaño del control de cliente en el escritorio remoto ha cambiado en respuesta a una operación de control de cliente.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- Método OnRemoteDesktopSizeChange Servicios de Escritorio remoto
- Método OnRemoteDesktopSizeChange Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRemoteDesktopSizeChange
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aee74049ea726b4e2686a028359afe01d2d7632
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534438"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a><span data-ttu-id="ff498-106">IMsTscAxEvents:: OnRemoteDesktopSizeChange (método)</span><span class="sxs-lookup"><span data-stu-id="ff498-106">IMsTscAxEvents::OnRemoteDesktopSizeChange method</span></span>

<span data-ttu-id="ff498-107">Se llama para indicar que el tamaño del control de cliente en el escritorio remoto ha cambiado en respuesta a una operación de control de cliente.</span><span class="sxs-lookup"><span data-stu-id="ff498-107">Called to indicate that the size of the client control on the remote desktop has changed in response to a client control operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff498-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff498-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="ff498-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff498-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff498-110">*ancho* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ff498-110">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff498-111">Ancho, en píxeles, del escritorio remoto cuyo tamaño se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ff498-111">Width, in pixels, of the resized remote desktop.</span></span>

</dd> <dt>

<span data-ttu-id="ff498-112">*alto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ff498-112">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff498-113">Alto, en píxeles, del escritorio remoto cuyo tamaño se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ff498-113">Height, in pixels, of the resized remote desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff498-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff498-114">Return value</span></span>

<span data-ttu-id="ff498-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ff498-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff498-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff498-116">Remarks</span></span>

<span data-ttu-id="ff498-117">Este evento permite al contenedor determinar si debe cambiar su tamaño en respuesta a una operación de control de cliente, lo que podría dar lugar a un mayor tamaño de escritorio visible.</span><span class="sxs-lookup"><span data-stu-id="ff498-117">This event allows the container to determine if it must resize itself in response to a client control operation, which could result in a larger viewable desktop size.</span></span> <span data-ttu-id="ff498-118">Tenga en cuenta que el control ajustará automáticamente las barras de desplazamiento para el nuevo tamaño de la sesión.</span><span class="sxs-lookup"><span data-stu-id="ff498-118">Note that the control will automatically adjust scroll bars for the new session size.</span></span>

<span data-ttu-id="ff498-119">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ff498-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff498-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff498-120">Requirements</span></span>



| <span data-ttu-id="ff498-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff498-121">Requirement</span></span> | <span data-ttu-id="ff498-122">Value</span><span class="sxs-lookup"><span data-stu-id="ff498-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff498-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff498-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ff498-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff498-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ff498-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff498-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ff498-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff498-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ff498-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ff498-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="ff498-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff498-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff498-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ff498-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff498-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff498-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff498-131">IID</span><span class="sxs-lookup"><span data-stu-id="ff498-131">IID</span></span><br/>                      | <span data-ttu-id="ff498-132">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="ff498-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="ff498-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff498-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff498-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="ff498-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





