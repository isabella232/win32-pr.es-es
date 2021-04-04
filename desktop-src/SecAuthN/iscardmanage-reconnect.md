---
description: Permite que una aplicación se vuelva a conectar a una tarjeta inteligente o lector sin tener que emitir una llamada detach seguida de una llamada a AttachByHandle o AttachByIFD, respectivamente.
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: 'ISCardManage:: reconnect (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8b05e6292a92267569eb1f53e10f6143554aba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908689"
---
# <a name="iscardmanagereconnect-method"></a><span data-ttu-id="f4a9f-103">ISCardManage:: reconnect (método)</span><span class="sxs-lookup"><span data-stu-id="f4a9f-103">ISCardManage::Reconnect method</span></span>

<span data-ttu-id="f4a9f-104">\[El método de **reconexión** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="f4a9f-104">\[The **Reconnect** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f4a9f-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f4a9f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f4a9f-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="f4a9f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f4a9f-107">El método de **reconexión** permite que una aplicación se vuelva a conectar a una [*tarjeta inteligente*](../secgloss/s-gly.md) o [*lector*](../secgloss/r-gly.md) sin tener que emitir una llamada de [**separación**](iscardmanage-detach.md) seguida de una llamada a [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD**](iscardmanage-attachbyifd.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f4a9f-107">The **Reconnect** method allows an application to reconnect to a [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) without having to issue a [**Detach**](iscardmanage-detach.md) call followed by an [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md) call respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a9f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4a9f-108">Syntax</span></span>


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a><span data-ttu-id="f4a9f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4a9f-109">Parameters</span></span>

<span data-ttu-id="f4a9f-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f4a9f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4a9f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f4a9f-111">Return value</span></span>

<span data-ttu-id="f4a9f-112">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="f4a9f-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="f4a9f-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f4a9f-113">Return code</span></span>                                                                                   | <span data-ttu-id="f4a9f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4a9f-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="f4a9f-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f4a9f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f4a9f-116">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="f4a9f-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="f4a9f-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f4a9f-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f4a9f-118">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="f4a9f-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f4a9f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4a9f-119">Remarks</span></span>

<span data-ttu-id="f4a9f-120">Para asociar una llamada de tarjeta inteligente [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="f4a9f-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="f4a9f-121">Para desasociar una tarjeta inteligente, llame a [**detach**](iscardmanage-detach.md).</span><span class="sxs-lookup"><span data-stu-id="f4a9f-121">To detach a smart card, call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="f4a9f-122">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="f4a9f-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="f4a9f-123">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f4a9f-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="f4a9f-124">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="f4a9f-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4a9f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4a9f-125">Requirements</span></span>



| <span data-ttu-id="f4a9f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4a9f-126">Requirement</span></span> | <span data-ttu-id="f4a9f-127">Value</span><span class="sxs-lookup"><span data-stu-id="f4a9f-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f4a9f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4a9f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f4a9f-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f4a9f-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f4a9f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4a9f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f4a9f-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4a9f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f4a9f-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f4a9f-132">End of client support</span></span><br/>    | <span data-ttu-id="f4a9f-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4a9f-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="f4a9f-134">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f4a9f-134">End of server support</span></span><br/>    | <span data-ttu-id="f4a9f-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4a9f-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="f4a9f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4a9f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a9f-137">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="f4a9f-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="f4a9f-138">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="f4a9f-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="f4a9f-139">**Conecta**</span><span class="sxs-lookup"><span data-stu-id="f4a9f-139">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="f4a9f-140">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="f4a9f-140">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
