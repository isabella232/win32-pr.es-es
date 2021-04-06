---
title: IMsTscAxEvents OnFatalError, método
description: Se llama cuando el control de cliente encuentra un error irrecuperable.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- Método OnFatalError Servicios de Escritorio remoto
- Método OnFatalError Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnFatalError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73402ac178bcb2ac3dc03c0adda092d3b49f6ba3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905382"
---
# <a name="imstscaxeventsonfatalerror-method"></a><span data-ttu-id="c31bf-106">IMsTscAxEvents:: OnFatalError (método)</span><span class="sxs-lookup"><span data-stu-id="c31bf-106">IMsTscAxEvents::OnFatalError method</span></span>

<span data-ttu-id="c31bf-107">Se llama cuando el control de cliente encuentra un error irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="c31bf-107">Called when the client control encounters a fatal error.</span></span>

## <a name="syntax"></a><span data-ttu-id="c31bf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c31bf-108">Syntax</span></span>


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="c31bf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c31bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c31bf-110">*ErrorCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c31bf-110">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c31bf-111">Indica el código de error.</span><span class="sxs-lookup"><span data-stu-id="c31bf-111">Indicates the error code.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="c31bf-112"><span id="0"></span>**0,1**</span><span class="sxs-lookup"><span data-stu-id="c31bf-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="c31bf-113">Se ha producido un error desconocido.</span><span class="sxs-lookup"><span data-stu-id="c31bf-113">An unknown error has occurred.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="c31bf-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="c31bf-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="c31bf-115">Código de error interno 1.</span><span class="sxs-lookup"><span data-stu-id="c31bf-115">Internal error code 1.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="c31bf-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="c31bf-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="c31bf-117">Error de memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="c31bf-117">An out-of-memory error has occurred.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="c31bf-118"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="c31bf-118"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="c31bf-119">Se ha producido un error de creación de ventana.</span><span class="sxs-lookup"><span data-stu-id="c31bf-119">A window-creation error has occurred.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="c31bf-120"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="c31bf-120"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="c31bf-121">Código de error interno 2.</span><span class="sxs-lookup"><span data-stu-id="c31bf-121">Internal error code 2.</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="c31bf-122"><span id="5"></span>**5**</span><span class="sxs-lookup"><span data-stu-id="c31bf-122"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="c31bf-123">Código de error interno 3.</span><span class="sxs-lookup"><span data-stu-id="c31bf-123">Internal error code 3.</span></span> <span data-ttu-id="c31bf-124">No es un estado válido.</span><span class="sxs-lookup"><span data-stu-id="c31bf-124">This is not a valid state.</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="c31bf-125"><span id="6"></span>**1,8**</span><span class="sxs-lookup"><span data-stu-id="c31bf-125"><span id="6"></span>**6**</span></span>


</dt> <dd>

<span data-ttu-id="c31bf-126">Código de error 4 interno.</span><span class="sxs-lookup"><span data-stu-id="c31bf-126">Internal error code 4.</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="c31bf-127"><span id="7"></span>**7**</span><span class="sxs-lookup"><span data-stu-id="c31bf-127"><span id="7"></span>**7**</span></span>


</dt> <dd>

<span data-ttu-id="c31bf-128">Se ha producido un error irrecuperable durante la conexión del cliente.</span><span class="sxs-lookup"><span data-stu-id="c31bf-128">An unrecoverable error has occurred during client connection.</span></span>

</dd> <dt>

<span id="100"></span>

<span data-ttu-id="c31bf-129"><span id="100"></span>**100**</span><span class="sxs-lookup"><span data-stu-id="c31bf-129"><span id="100"></span>**100**</span></span>


</dt> <dd>

<span data-ttu-id="c31bf-130">Error de inicialización de Winsock.</span><span class="sxs-lookup"><span data-stu-id="c31bf-130">Winsock initialization error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c31bf-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c31bf-131">Return value</span></span>

<span data-ttu-id="c31bf-132">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c31bf-132">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c31bf-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c31bf-133">Remarks</span></span>

<span data-ttu-id="c31bf-134">En respuesta a este evento, el contenedor muestra un mensaje de error y se cierra.</span><span class="sxs-lookup"><span data-stu-id="c31bf-134">In response to this event, the container displays an error message and shuts down.</span></span>

<span data-ttu-id="c31bf-135">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c31bf-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c31bf-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c31bf-136">Requirements</span></span>



| <span data-ttu-id="c31bf-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c31bf-137">Requirement</span></span> | <span data-ttu-id="c31bf-138">Value</span><span class="sxs-lookup"><span data-stu-id="c31bf-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c31bf-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c31bf-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c31bf-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c31bf-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c31bf-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c31bf-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c31bf-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c31bf-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c31bf-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c31bf-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="c31bf-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c31bf-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c31bf-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c31bf-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c31bf-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c31bf-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c31bf-147">IID</span><span class="sxs-lookup"><span data-stu-id="c31bf-147">IID</span></span><br/>                      | <span data-ttu-id="c31bf-148">IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="c31bf-148">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="c31bf-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="c31bf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c31bf-150">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="c31bf-150">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





