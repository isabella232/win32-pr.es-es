---
description: Libera el uso exclusivo de la tarjeta inteligente conectada.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'ISCardManage:: SCardUnlock (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276271"
---
# <a name="iscardmanagescardunlock-method"></a><span data-ttu-id="861b3-103">ISCardManage:: SCardUnlock (método)</span><span class="sxs-lookup"><span data-stu-id="861b3-103">ISCardManage::SCardUnlock method</span></span>

<span data-ttu-id="861b3-104">\[El método **SCardUnlock** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="861b3-104">\[The **SCardUnlock** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="861b3-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="861b3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="861b3-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="861b3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="861b3-107">El método **SCardUnlock** libera el uso exclusivo de la [*tarjeta inteligente*](../secgloss/s-gly.md)conectada.</span><span class="sxs-lookup"><span data-stu-id="861b3-107">The **SCardUnlock** method releases exclusive use of the connected [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="861b3-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="861b3-108">Syntax</span></span>


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a><span data-ttu-id="861b3-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="861b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="861b3-110">*Disposición* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="861b3-110">*Disposition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="861b3-111">El estado al que se dejará la tarjeta inteligente cuando se lance el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="861b3-111">The state to leave the smart card in when the lock is released.</span></span>

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

<span data-ttu-id="861b3-112">**OMITI**</span><span class="sxs-lookup"><span data-stu-id="861b3-112">**LEAVE**</span></span>
</dt><span id="RESET"></span><span id="reset"></span><dt>

<span data-ttu-id="861b3-113">**RESET**</span><span class="sxs-lookup"><span data-stu-id="861b3-113">**RESET**</span></span>
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

<span data-ttu-id="861b3-114">**No energía**</span><span class="sxs-lookup"><span data-stu-id="861b3-114">**UNPOWER**</span></span>
</dt><span id="EJECT"></span><span id="eject"></span><dt>

<span data-ttu-id="861b3-115">**EXPULSAR**</span><span class="sxs-lookup"><span data-stu-id="861b3-115">**EJECT**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="861b3-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="861b3-116">Return value</span></span>

<span data-ttu-id="861b3-117">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="861b3-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="861b3-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="861b3-118">Return code</span></span>                                                                                  | <span data-ttu-id="861b3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="861b3-119">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="861b3-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="861b3-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="861b3-121">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="861b3-121">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="861b3-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="861b3-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="861b3-123">El parámetro de *disposición* no es válido.</span><span class="sxs-lookup"><span data-stu-id="861b3-123">The *Disposition* parameter is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="861b3-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="861b3-124">Remarks</span></span>

<span data-ttu-id="861b3-125">Para bloquear la tarjeta inteligente conectada, llame a [**SCardLock**](iscardmanage-scardlock.md).</span><span class="sxs-lookup"><span data-stu-id="861b3-125">To lock the connected smart card, call [**SCardLock**](iscardmanage-scardlock.md).</span></span>

<span data-ttu-id="861b3-126">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="861b3-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="861b3-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="861b3-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="861b3-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="861b3-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="861b3-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="861b3-129">Requirements</span></span>



| <span data-ttu-id="861b3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="861b3-130">Requirement</span></span> | <span data-ttu-id="861b3-131">Value</span><span class="sxs-lookup"><span data-stu-id="861b3-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="861b3-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="861b3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="861b3-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="861b3-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="861b3-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="861b3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="861b3-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="861b3-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="861b3-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="861b3-136">End of client support</span></span><br/>    | <span data-ttu-id="861b3-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="861b3-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="861b3-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="861b3-138">End of server support</span></span><br/>    | <span data-ttu-id="861b3-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="861b3-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="861b3-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="861b3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="861b3-141">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="861b3-141">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="861b3-142">**SCardLock**</span><span class="sxs-lookup"><span data-stu-id="861b3-142">**SCardLock**</span></span>](iscardmanage-scardlock.md)
</dt> </dl>

 

 
