---
description: Restablece el contexto de seguridad actual de la tarjeta inteligente.
ms.assetid: fcd55b65-a741-4244-8597-ec61cea3f4b7
title: 'ISCardVerify:: ResetSecurityState (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ResetSecurityState
api_type:
- COM
api_location: ''
ms.openlocfilehash: ba96d400258fb58957c8c263438160d6710806db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907655"
---
# <a name="iscardverifyresetsecuritystate-method"></a><span data-ttu-id="7acbc-103">ISCardVerify:: ResetSecurityState (método)</span><span class="sxs-lookup"><span data-stu-id="7acbc-103">ISCardVerify::ResetSecurityState method</span></span>

<span data-ttu-id="7acbc-104">\[El método **ResetSecurityState** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="7acbc-104">\[The **ResetSecurityState** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7acbc-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7acbc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7acbc-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="7acbc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7acbc-107">El método **ResetSecurityState** restablece el contexto de [*seguridad*](../secgloss/s-gly.md) actual de la [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7acbc-107">The **ResetSecurityState** method resets the current [*security context*](../secgloss/s-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7acbc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7acbc-108">Syntax</span></span>


```C++
HRESULT ResetSecurityState();
```



## <a name="parameters"></a><span data-ttu-id="7acbc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7acbc-109">Parameters</span></span>

<span data-ttu-id="7acbc-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7acbc-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7acbc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7acbc-111">Return value</span></span>

<span data-ttu-id="7acbc-112">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="7acbc-112">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="7acbc-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7acbc-113">Return code</span></span>                                                                                   | <span data-ttu-id="7acbc-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="7acbc-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7acbc-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7acbc-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7acbc-116">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="7acbc-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="7acbc-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7acbc-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7acbc-118">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="7acbc-118">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="7acbc-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7acbc-119">Remarks</span></span>

<span data-ttu-id="7acbc-120">Para volver a habilitar el [*contexto de seguridad*](../secgloss/s-gly.md) sin restablecer, llame a [**unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7acbc-120">To re-enable the [*security context*](../secgloss/s-gly.md) without resetting, call [**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85)).</span></span>

<span data-ttu-id="7acbc-121">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="7acbc-121">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="7acbc-122">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7acbc-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7acbc-123">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7acbc-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7acbc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7acbc-124">Requirements</span></span>



| <span data-ttu-id="7acbc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7acbc-125">Requirement</span></span> | <span data-ttu-id="7acbc-126">Value</span><span class="sxs-lookup"><span data-stu-id="7acbc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7acbc-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7acbc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7acbc-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7acbc-128">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7acbc-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7acbc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7acbc-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7acbc-130">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7acbc-131">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7acbc-131">End of client support</span></span><br/>    | <span data-ttu-id="7acbc-132">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7acbc-132">Windows XP</span></span><br/>                                |
| <span data-ttu-id="7acbc-133">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7acbc-133">End of server support</span></span><br/>    | <span data-ttu-id="7acbc-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7acbc-134">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="7acbc-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="7acbc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7acbc-136">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="7acbc-136">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

<span data-ttu-id="7acbc-137">[**Desbloquear**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7acbc-137">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>
</dt> </dl>

 

 
