---
description: Bloquea una tarjeta inteligente conectada para su uso exclusivo.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: 'ISCardManage:: SCardLock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2198f512fde90d1c79173f5151fc4f759944500a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276273"
---
# <a name="iscardmanagescardlock-method"></a><span data-ttu-id="136a9-103">ISCardManage:: SCardLock (método)</span><span class="sxs-lookup"><span data-stu-id="136a9-103">ISCardManage::SCardLock method</span></span>

<span data-ttu-id="136a9-104">\[El método **SCardLock** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="136a9-104">\[The **SCardLock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="136a9-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="136a9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="136a9-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="136a9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="136a9-107">El método **SCardLock** bloquea una [*tarjeta inteligente*](../secgloss/s-gly.md) conectada para su uso exclusivo.</span><span class="sxs-lookup"><span data-stu-id="136a9-107">The **SCardLock** method locks a connected [*smart card*](../secgloss/s-gly.md) for exclusive use.</span></span>

## <a name="syntax"></a><span data-ttu-id="136a9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="136a9-108">Syntax</span></span>


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a><span data-ttu-id="136a9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="136a9-109">Parameters</span></span>

<span data-ttu-id="136a9-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="136a9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="136a9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="136a9-111">Return value</span></span>

<span data-ttu-id="136a9-112">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="136a9-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="136a9-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="136a9-113">Return code</span></span>                                                                            | <span data-ttu-id="136a9-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="136a9-114">Description</span></span>                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="136a9-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="136a9-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="136a9-116">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="136a9-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="136a9-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="136a9-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="136a9-118">No se pudo completar la operación.</span><span class="sxs-lookup"><span data-stu-id="136a9-118">Operation failed to complete.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="136a9-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="136a9-119">Remarks</span></span>

<span data-ttu-id="136a9-120">Para liberar el uso exclusivo de la tarjeta inteligente conectada, llame a [**SCardUnlock**](iscardmanage-scardunlock.md).</span><span class="sxs-lookup"><span data-stu-id="136a9-120">To releases exclusive use of the connected smart card, call [**SCardUnlock**](iscardmanage-scardunlock.md).</span></span>

<span data-ttu-id="136a9-121">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="136a9-121">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="136a9-122">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="136a9-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="136a9-123">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="136a9-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="136a9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="136a9-124">Requirements</span></span>



| <span data-ttu-id="136a9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="136a9-125">Requirement</span></span> | <span data-ttu-id="136a9-126">Value</span><span class="sxs-lookup"><span data-stu-id="136a9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="136a9-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="136a9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="136a9-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="136a9-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="136a9-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="136a9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="136a9-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="136a9-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="136a9-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="136a9-131">End of client support</span></span><br/>    | <span data-ttu-id="136a9-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="136a9-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="136a9-133">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="136a9-133">End of server support</span></span><br/>    | <span data-ttu-id="136a9-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="136a9-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="136a9-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="136a9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="136a9-136">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="136a9-136">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="136a9-137">**SCardUnlock**</span><span class="sxs-lookup"><span data-stu-id="136a9-137">**SCardUnlock**</span></span>](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
