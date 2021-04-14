---
description: Obtiene el estado actual de la tarjeta inteligente o del lector.
ms.assetid: ae285e2e-6591-43ab-b92f-1ec755872379
title: 'ISCardManage:: status (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 26683823b5b709d86b36f4345b47f306f2000ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648298"
---
# <a name="iscardmanagestatus-method"></a><span data-ttu-id="46933-103">ISCardManage:: status (método)</span><span class="sxs-lookup"><span data-stu-id="46933-103">ISCardManage::Status method</span></span>

<span data-ttu-id="46933-104">\[El método de **Estado** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="46933-104">\[The **Status** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="46933-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="46933-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="46933-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="46933-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="46933-107">El método **status** obtiene el estado actual de la [*tarjeta inteligente*](../secgloss/s-gly.md) o del [*lector*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="46933-107">The **Status** method gets the current status of the [*smart card*](../secgloss/s-gly.md) or [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="46933-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46933-108">Syntax</span></span>


```C++
HRESULT Status(
  [out] SCARD_STATES    *pStatus,
  [out] SCARD_PROTOCOLS *pProtocols
);
```



## <a name="parameters"></a><span data-ttu-id="46933-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46933-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46933-110">*pStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="46933-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46933-111">Puntero a un valor de \_ enumeración de Estados de PPAC.</span><span class="sxs-lookup"><span data-stu-id="46933-111">Pointer to an SCARD\_STATES enumeration value.</span></span> <span data-ttu-id="46933-112">En la devolución, contiene el estado o estado actual.</span><span class="sxs-lookup"><span data-stu-id="46933-112">On return, contains the current status/state.</span></span>

</dd> <dt>

<span data-ttu-id="46933-113">*pProtocols* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="46933-113">*pProtocols* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46933-114">Puntero a un valor de \_ enumeración de protocolos de PPAC.</span><span class="sxs-lookup"><span data-stu-id="46933-114">Pointer to an SCARD\_PROTOCOLS enumeration value.</span></span> <span data-ttu-id="46933-115">En la devolución, contiene el protocolo actual.</span><span class="sxs-lookup"><span data-stu-id="46933-115">On return, contains the current protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46933-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46933-116">Return value</span></span>

<span data-ttu-id="46933-117">El método devuelve uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="46933-117">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="46933-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="46933-118">Return code</span></span>                                                                                   | <span data-ttu-id="46933-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="46933-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="46933-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="46933-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="46933-121">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="46933-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="46933-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="46933-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="46933-123">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="46933-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="46933-124"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="46933-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="46933-125">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="46933-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="46933-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="46933-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="46933-127">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="46933-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="46933-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46933-128">Remarks</span></span>

<span data-ttu-id="46933-129">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardManage**](iscardmanage.md).</span><span class="sxs-lookup"><span data-stu-id="46933-129">For a list of all the methods defined by this interface, see [**ISCardManage**](iscardmanage.md).</span></span>

<span data-ttu-id="46933-130">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="46933-130">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="46933-131">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="46933-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46933-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46933-132">Requirements</span></span>



| <span data-ttu-id="46933-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="46933-133">Requirement</span></span> | <span data-ttu-id="46933-134">Value</span><span class="sxs-lookup"><span data-stu-id="46933-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46933-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46933-135">Minimum supported client</span></span><br/> | <span data-ttu-id="46933-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="46933-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="46933-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46933-137">Minimum supported server</span></span><br/> | <span data-ttu-id="46933-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="46933-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="46933-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="46933-139">End of client support</span></span><br/>    | <span data-ttu-id="46933-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="46933-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="46933-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="46933-141">End of server support</span></span><br/>    | <span data-ttu-id="46933-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="46933-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="46933-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="46933-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46933-144">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="46933-144">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
