---
description: Crea un vínculo de comunicación a una tarjeta inteligente (ICC) mediante un identificador devuelto por el administrador de recursos de tarjeta inteligente.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: 'ISCardManage:: AttachByHandle (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910630"
---
# <a name="iscardmanageattachbyhandle-method"></a><span data-ttu-id="afb6d-103">ISCardManage:: AttachByHandle (método)</span><span class="sxs-lookup"><span data-stu-id="afb6d-103">ISCardManage::AttachByHandle method</span></span>

<span data-ttu-id="afb6d-104">\[El método **AttachByHandle** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="afb6d-104">\[The **AttachByHandle** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="afb6d-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="afb6d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="afb6d-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="afb6d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="afb6d-107">El método **AttachByHandle** crea un vínculo de comunicación a una [*tarjeta inteligente*](../secgloss/s-gly.md) (ICC) mediante un identificador devuelto por el [*Administrador de recursos*](../secgloss/r-gly.md)de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="afb6d-107">The **AttachByHandle** method creates a communication link to a [*smart card*](../secgloss/s-gly.md) (ICC) using a handle returned by the smart card [*resource manager*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="afb6d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afb6d-108">Syntax</span></span>


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a><span data-ttu-id="afb6d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afb6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afb6d-110">*hICC* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="afb6d-110">*hICC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afb6d-111">Identificador de una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="afb6d-111">A handle to a smart card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afb6d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afb6d-112">Return value</span></span>

<span data-ttu-id="afb6d-113">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="afb6d-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="afb6d-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="afb6d-114">Return code</span></span>                                                                                   | <span data-ttu-id="afb6d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="afb6d-115">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="afb6d-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="afb6d-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="afb6d-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="afb6d-117">Operation completed successfully.</span></span><br/>  |
| <dl> <span data-ttu-id="afb6d-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="afb6d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="afb6d-119">El parámetro *hICC* no es válido.</span><span class="sxs-lookup"><span data-stu-id="afb6d-119">The *hICC* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="afb6d-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="afb6d-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="afb6d-121">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="afb6d-121">Out of memory.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="afb6d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afb6d-122">Remarks</span></span>

<span data-ttu-id="afb6d-123">Para adjuntar una llamada de [*lector*](../secgloss/r-gly.md) [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="afb6d-123">To attach a [*reader*](../secgloss/r-gly.md) call [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="afb6d-124">Para liberar la [**desasociación**](iscardmanage-detach.md)de una llamada de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="afb6d-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="afb6d-125">Para volver a conectar con la tarjeta inteligente sin llamar a [**detach**](iscardmanage-detach.md) y **AttachByHandle**, llame a [**reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="afb6d-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByHandle**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="afb6d-126">Para obtener una lista de todos los métodos definidos por la interfaz [**ISCardManage**](iscardmanage.md) , vea [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="afb6d-126">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="afb6d-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="afb6d-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="afb6d-128">Para obtener información sobre los códigos de error de las tarjetas inteligentes, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="afb6d-128">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="afb6d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afb6d-129">Requirements</span></span>



| <span data-ttu-id="afb6d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="afb6d-130">Requirement</span></span> | <span data-ttu-id="afb6d-131">Value</span><span class="sxs-lookup"><span data-stu-id="afb6d-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="afb6d-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afb6d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="afb6d-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="afb6d-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="afb6d-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="afb6d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="afb6d-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="afb6d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="afb6d-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="afb6d-136">End of client support</span></span><br/>    | <span data-ttu-id="afb6d-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="afb6d-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="afb6d-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="afb6d-138">End of server support</span></span><br/>    | <span data-ttu-id="afb6d-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="afb6d-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="afb6d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="afb6d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afb6d-141">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="afb6d-141">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="afb6d-142">**Conecta**</span><span class="sxs-lookup"><span data-stu-id="afb6d-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="afb6d-143">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="afb6d-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="afb6d-144">**Volver a conectar**</span><span class="sxs-lookup"><span data-stu-id="afb6d-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
