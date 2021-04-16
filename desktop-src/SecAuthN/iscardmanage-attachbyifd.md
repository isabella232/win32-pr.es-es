---
description: Crea un vínculo de comunicación a un lector, utilizando un nombre para mostrar proporcionado para el lector.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'ISCardManage:: AttachByIFD (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648457"
---
# <a name="iscardmanageattachbyifd-method"></a><span data-ttu-id="0192f-103">ISCardManage:: AttachByIFD (método)</span><span class="sxs-lookup"><span data-stu-id="0192f-103">ISCardManage::AttachByIFD method</span></span>

<span data-ttu-id="0192f-104">\[El método **AttachByIFD** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="0192f-104">\[The **AttachByIFD** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0192f-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0192f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0192f-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="0192f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="0192f-107">El método **AttachByIFD** crea un vínculo de comunicación a un [*lector*](../secgloss/r-gly.md), utilizando un nombre para mostrar proporcionado para el lector.</span><span class="sxs-lookup"><span data-stu-id="0192f-107">The **AttachByIFD** method creates a communication link to a [*reader*](../secgloss/r-gly.md), using a supplied display name for the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="0192f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0192f-108">Syntax</span></span>


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a><span data-ttu-id="0192f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0192f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0192f-110">*bstrIFDName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0192f-110">*bstrIFDName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0192f-111">Nombre para mostrar del lector.</span><span class="sxs-lookup"><span data-stu-id="0192f-111">The display name of the reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0192f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0192f-112">Return value</span></span>

<span data-ttu-id="0192f-113">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="0192f-113">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="0192f-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0192f-114">Return code</span></span>                                                                                   | <span data-ttu-id="0192f-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="0192f-115">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="0192f-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0192f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0192f-117">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="0192f-117">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="0192f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0192f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0192f-119">El parámetro *bstrIFDName* no es válido.</span><span class="sxs-lookup"><span data-stu-id="0192f-119">The *bstrIFDName* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="0192f-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0192f-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0192f-121">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="0192f-121">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="0192f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0192f-122">Remarks</span></span>

<span data-ttu-id="0192f-123">Para adjuntar una llamada de [*tarjeta inteligente*](../secgloss/s-gly.md) [**AttachByHandle**](iscardmanage-attachbyhandle.md).</span><span class="sxs-lookup"><span data-stu-id="0192f-123">To attach a [*smart card*](../secgloss/s-gly.md) call [**AttachByHandle**](iscardmanage-attachbyhandle.md).</span></span>

<span data-ttu-id="0192f-124">Para liberar la [**desasociación**](iscardmanage-detach.md)de una llamada de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0192f-124">To release an attachment call [**Detach**](iscardmanage-detach.md).</span></span>

<span data-ttu-id="0192f-125">Para volver a conectar con la tarjeta inteligente sin llamar a [**detach**](iscardmanage-detach.md) y **AttachByIFD**, llame a [**reconnect**](iscardmanage-reconnect.md).</span><span class="sxs-lookup"><span data-stu-id="0192f-125">To reconnect with the smart card without calling [**Detach**](iscardmanage-detach.md) and **AttachByIFD**, call [**Reconnect**](iscardmanage-reconnect.md).</span></span>

<span data-ttu-id="0192f-126">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="0192f-126">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="0192f-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0192f-127">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="0192f-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="0192f-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0192f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0192f-129">Requirements</span></span>



| <span data-ttu-id="0192f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0192f-130">Requirement</span></span> | <span data-ttu-id="0192f-131">Value</span><span class="sxs-lookup"><span data-stu-id="0192f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0192f-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0192f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0192f-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0192f-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0192f-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0192f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0192f-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0192f-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0192f-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0192f-136">End of client support</span></span><br/>    | <span data-ttu-id="0192f-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0192f-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="0192f-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="0192f-138">End of server support</span></span><br/>    | <span data-ttu-id="0192f-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0192f-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="0192f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0192f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0192f-141">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="0192f-141">**AttachByHandle**</span></span>](iscardmanage-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="0192f-142">**Conecta**</span><span class="sxs-lookup"><span data-stu-id="0192f-142">**Detach**</span></span>](iscardmanage-detach.md)
</dt> <dt>

[<span data-ttu-id="0192f-143">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="0192f-143">**ISCardManage**</span></span>](iscardmanage.md)
</dt> <dt>

[<span data-ttu-id="0192f-144">**Volver a conectar**</span><span class="sxs-lookup"><span data-stu-id="0192f-144">**Reconnect**</span></span>](iscardmanage-reconnect.md)
</dt> </dl>

 

 
