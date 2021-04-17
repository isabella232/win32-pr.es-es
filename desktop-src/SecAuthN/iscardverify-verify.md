---
description: Solicita una comprobación del usuario.
ms.assetid: e8b7155c-3444-4aa8-8a15-3b3624a44a77
title: 'ISCardVerify:: verify (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.Verify
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68f3a97df672d97e635180f41405a75c4cb84661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652655"
---
# <a name="iscardverifyverify-method"></a><span data-ttu-id="e50fb-103">ISCardVerify:: verify (método)</span><span class="sxs-lookup"><span data-stu-id="e50fb-103">ISCardVerify::Verify method</span></span>

<span data-ttu-id="e50fb-104">\[El método **Verify** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="e50fb-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e50fb-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e50fb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e50fb-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="e50fb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="e50fb-107">El método **Verify** solicita una comprobación del usuario.</span><span class="sxs-lookup"><span data-stu-id="e50fb-107">The **Verify** method requests a verification of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="e50fb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e50fb-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in] LPBYTEBUFFER pCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="e50fb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e50fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e50fb-110">*Pcode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e50fb-110">*pCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50fb-111">Contiene el código que se va a presentar a la [*tarjeta inteligente*](../secgloss/s-gly.md) en el proceso CHV (comprobación del titular de la tarjeta).</span><span class="sxs-lookup"><span data-stu-id="e50fb-111">Contains the code to be presented to the [*smart card*](../secgloss/s-gly.md) in the CHV (card holder verification) process.</span></span>

</dd> <dt>

<span data-ttu-id="e50fb-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e50fb-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50fb-113">Indica si el código es global o local.</span><span class="sxs-lookup"><span data-stu-id="e50fb-113">Indicates whether the code is global or local.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="e50fb-114">**SC \_ FL \_ \_ global**</span><span class="sxs-lookup"><span data-stu-id="e50fb-114">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="e50fb-115">**SC \_ FL \_ \_ local**</span><span class="sxs-lookup"><span data-stu-id="e50fb-115">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="e50fb-116">*lRef* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e50fb-116">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e50fb-117">Referencia específica de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="e50fb-117">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e50fb-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e50fb-118">Return value</span></span>

<span data-ttu-id="e50fb-119">El método **Verify** devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e50fb-119">The **Verify** method returns one of the following values:</span></span>



| <span data-ttu-id="e50fb-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e50fb-120">Return code</span></span>                                                                                   | <span data-ttu-id="e50fb-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e50fb-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e50fb-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e50fb-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e50fb-123">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="e50fb-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e50fb-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e50fb-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e50fb-125">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="e50fb-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="e50fb-126"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e50fb-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e50fb-127">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="e50fb-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="e50fb-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e50fb-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e50fb-129">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="e50fb-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e50fb-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e50fb-130">Remarks</span></span>

<span data-ttu-id="e50fb-131">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="e50fb-131">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="e50fb-132">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e50fb-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="e50fb-133">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="e50fb-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e50fb-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e50fb-134">Requirements</span></span>



| <span data-ttu-id="e50fb-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e50fb-135">Requirement</span></span> | <span data-ttu-id="e50fb-136">Value</span><span class="sxs-lookup"><span data-stu-id="e50fb-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e50fb-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e50fb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e50fb-138">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e50fb-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e50fb-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e50fb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e50fb-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e50fb-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e50fb-141">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="e50fb-141">End of client support</span></span><br/>    | <span data-ttu-id="e50fb-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e50fb-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="e50fb-143">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="e50fb-143">End of server support</span></span><br/>    | <span data-ttu-id="e50fb-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e50fb-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="e50fb-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="e50fb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e50fb-146">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="e50fb-146">**ISCardVerify**</span></span>](iscardverify.md)
</dt> </dl>

 

 
