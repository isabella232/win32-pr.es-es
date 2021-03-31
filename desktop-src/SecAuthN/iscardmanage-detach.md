---
description: Libera los datos adjuntos a una tarjeta inteligente o lector específicos asignados por AttachByHandle y AttachByIFD, respectivamente.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: ISCardManage::D método Etach
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc5a48f76a643447b3e3d836d61ad7a769c56ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155500"
---
# <a name="iscardmanagedetach-method"></a><span data-ttu-id="b6ec8-103">ISCardManage::D método Etach</span><span class="sxs-lookup"><span data-stu-id="b6ec8-103">ISCardManage::Detach method</span></span>

<span data-ttu-id="b6ec8-104">\[El método **detach** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-104">\[The **Detach** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b6ec8-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b6ec8-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b6ec8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="b6ec8-107">El método **detach** libera los datos adjuntos a una [*tarjeta inteligente*](../secgloss/s-gly.md) o [*lector*](../secgloss/r-gly.md) específicos asignados por [**AttachByHandle**](iscardmanage-attachbyhandle.md) y [**AttachByIFD**](iscardmanage-attachbyifd.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-107">The **Detach** method releases the attachment to a particular [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md) allocated by [**AttachByHandle**](iscardmanage-attachbyhandle.md) and [**AttachByIFD**](iscardmanage-attachbyifd.md) respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6ec8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6ec8-108">Syntax</span></span>


```C++
HRESULT Detach();
```



## <a name="parameters"></a><span data-ttu-id="b6ec8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6ec8-109">Parameters</span></span>

<span data-ttu-id="b6ec8-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b6ec8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6ec8-111">Return value</span></span>

<span data-ttu-id="b6ec8-112">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="b6ec8-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="b6ec8-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b6ec8-113">Return code</span></span>                                                                                   | <span data-ttu-id="b6ec8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6ec8-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b6ec8-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b6ec8-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b6ec8-116">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b6ec8-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b6ec8-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b6ec8-118">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="b6ec8-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="b6ec8-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6ec8-119">Remarks</span></span>

<span data-ttu-id="b6ec8-120">Para asociar una llamada de tarjeta inteligente [**AttachByHandle**](iscardmanage-attachbyhandle.md) o [**AttachByIFD**](iscardmanage-attachbyifd.md).</span><span class="sxs-lookup"><span data-stu-id="b6ec8-120">To attach a smart card call [**AttachByHandle**](iscardmanage-attachbyhandle.md) or [**AttachByIFD**](iscardmanage-attachbyifd.md).</span></span>

<span data-ttu-id="b6ec8-121">Para volver a conectar con la tarjeta inteligente sin llamar a **detach** y [**AttachByHandle**](iscardmanage-attachbyhandle.md), llame a [**reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="b6ec8-121">To reconnect with the smart card without calling **Detach** and [**AttachByHandle**](iscardmanage-attachbyhandle.md), call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="b6ec8-122">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="b6ec8-122">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="b6ec8-123">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6ec8-123">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="b6ec8-124">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="b6ec8-124">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6ec8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6ec8-125">Requirements</span></span>



| <span data-ttu-id="b6ec8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6ec8-126">Requirement</span></span> | <span data-ttu-id="b6ec8-127">Value</span><span class="sxs-lookup"><span data-stu-id="b6ec8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b6ec8-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6ec8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b6ec8-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b6ec8-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b6ec8-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6ec8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b6ec8-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6ec8-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b6ec8-132">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b6ec8-132">End of client support</span></span><br/>    | <span data-ttu-id="b6ec8-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b6ec8-133">Windows XP</span></span><br/>                                |
| <span data-ttu-id="b6ec8-134">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b6ec8-134">End of server support</span></span><br/>    | <span data-ttu-id="b6ec8-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b6ec8-135">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="b6ec8-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6ec8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ec8-137">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-137">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="b6ec8-138">**AttachByIFD**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-138">**AttachByIFD**</span></span>](iscardmanage-attachbyifd.md)
</dt> <dt>

[<span data-ttu-id="b6ec8-139">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-139">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="b6ec8-140">**Volver a conectar**</span><span class="sxs-lookup"><span data-stu-id="b6ec8-140">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
