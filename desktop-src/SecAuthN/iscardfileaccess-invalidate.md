---
description: Hace que el archivo especificado (EF o DF) no sea válido. No se puede tener acceso a un archivo no válido mediante otros métodos antes de usar Rehabilitate.
ms.assetid: 5600fcf0-091c-437e-a45c-4de5b0a47d68
title: 'ISCardFileAccess:: Invalidate (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Invalidate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e1d74885f97eca64f403155f1dba52e398b9426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652914"
---
# <a name="iscardfileaccessinvalidate-method"></a><span data-ttu-id="6de3b-104">ISCardFileAccess:: Invalidate (método)</span><span class="sxs-lookup"><span data-stu-id="6de3b-104">ISCardFileAccess::Invalidate method</span></span>

<span data-ttu-id="6de3b-105">\[El método **Invalidate** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="6de3b-105">\[The **Invalidate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6de3b-106">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6de3b-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6de3b-107">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="6de3b-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6de3b-108">El método **Invalidate** hace que el archivo especificado (EF o DF) no sea válido.</span><span class="sxs-lookup"><span data-stu-id="6de3b-108">The **Invalidate** method makes the specified file (EF or DF) not valid.</span></span> <span data-ttu-id="6de3b-109">No se puede tener acceso a un archivo no válido mediante otros métodos antes de usar [**Rehabilitate**](iscardfileaccess-rehabilitate.md).</span><span class="sxs-lookup"><span data-stu-id="6de3b-109">A file that is not valid cannot be accessed by other methods prior to using [**Rehabilitate**](iscardfileaccess-rehabilitate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6de3b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6de3b-110">Syntax</span></span>


```C++
HRESULT Invalidate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="6de3b-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6de3b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6de3b-112">*bstrPathSpec* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6de3b-112">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6de3b-113">Archivo:</span><span class="sxs-lookup"><span data-stu-id="6de3b-113">File.</span></span>

</dd> <dt>

<span data-ttu-id="6de3b-114">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6de3b-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6de3b-115">Especifica si se debe usar la mensajería segura.</span><span class="sxs-lookup"><span data-stu-id="6de3b-115">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="6de3b-116">**\_ \_ mensajería segura de SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="6de3b-116">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6de3b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6de3b-117">Return value</span></span>

<span data-ttu-id="6de3b-118">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="6de3b-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6de3b-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6de3b-119">Return code</span></span>                                                                                   | <span data-ttu-id="6de3b-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="6de3b-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6de3b-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6de3b-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6de3b-122">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="6de3b-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6de3b-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6de3b-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6de3b-124">Un parámetro no es válido.</span><span class="sxs-lookup"><span data-stu-id="6de3b-124">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="6de3b-125"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="6de3b-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6de3b-126">Se pasó un puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="6de3b-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="6de3b-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6de3b-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6de3b-128">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="6de3b-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6de3b-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6de3b-129">Remarks</span></span>

<span data-ttu-id="6de3b-130">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="6de3b-130">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="6de3b-131">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6de3b-131">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6de3b-132">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6de3b-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6de3b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6de3b-133">Requirements</span></span>



| <span data-ttu-id="6de3b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6de3b-134">Requirement</span></span> | <span data-ttu-id="6de3b-135">Value</span><span class="sxs-lookup"><span data-stu-id="6de3b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6de3b-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6de3b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6de3b-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6de3b-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="6de3b-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6de3b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6de3b-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6de3b-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6de3b-140">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="6de3b-140">End of client support</span></span><br/>    | <span data-ttu-id="6de3b-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6de3b-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="6de3b-142">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="6de3b-142">End of server support</span></span><br/>    | <span data-ttu-id="6de3b-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6de3b-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6de3b-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="6de3b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de3b-145">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="6de3b-145">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="6de3b-146">**Rehabilitate**</span><span class="sxs-lookup"><span data-stu-id="6de3b-146">**Rehabilitate**</span></span>](iscardfileaccess-rehabilitate.md)
</dt> </dl>

 

 
