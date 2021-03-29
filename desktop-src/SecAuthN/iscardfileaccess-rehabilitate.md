---
description: Crea un archivo (EF o DF) que anteriormente no era válido mediante el método Invalidate, al que puede tener acceso la aplicación.
ms.assetid: 1906fcc5-ae76-4950-b2eb-e5ce1882637f
title: 'ISCardFileAccess:: Rehabilitate (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Rehabilitate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7ed02131de08104dab8aff23ee9054659fd4cd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652699"
---
# <a name="iscardfileaccessrehabilitate-method"></a><span data-ttu-id="ce88a-103">ISCardFileAccess:: Rehabilitate (método)</span><span class="sxs-lookup"><span data-stu-id="ce88a-103">ISCardFileAccess::Rehabilitate method</span></span>

<span data-ttu-id="ce88a-104">\[El método **Rehabilitate** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="ce88a-104">\[The **Rehabilitate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ce88a-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ce88a-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ce88a-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="ce88a-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="ce88a-107">El método **Rehabilitate** crea un archivo (EF o DF) que anteriormente no era válido mediante el método [**Invalidate**](iscardfileaccess-invalidate.md) , al que puede tener acceso la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ce88a-107">The **Rehabilitate** method makes a file (EF or DF) that was previously made not valid by using the [**Invalidate**](iscardfileaccess-invalidate.md) method, accessible by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce88a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce88a-108">Syntax</span></span>


```C++
HRESULT Rehabilitate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="ce88a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce88a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce88a-110">*bstrPathSpec* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ce88a-110">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce88a-111">Archivo en rehabilitate.</span><span class="sxs-lookup"><span data-stu-id="ce88a-111">File to rehabilitate.</span></span>

</dd> <dt>

<span data-ttu-id="ce88a-112">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ce88a-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce88a-113">Especifica si se debe usar la mensajería segura.</span><span class="sxs-lookup"><span data-stu-id="ce88a-113">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="ce88a-114">**\_ \_ mensajería segura de SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="ce88a-114">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce88a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce88a-115">Return value</span></span>

<span data-ttu-id="ce88a-116">El método devuelve uno de los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="ce88a-116">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="ce88a-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ce88a-117">Return code</span></span>                                                                                   | <span data-ttu-id="ce88a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce88a-118">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="ce88a-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ce88a-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ce88a-120">Operación completada correctamente.</span><span class="sxs-lookup"><span data-stu-id="ce88a-120">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="ce88a-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ce88a-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ce88a-122">Un parámetro no es válido.</span><span class="sxs-lookup"><span data-stu-id="ce88a-122">A parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="ce88a-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ce88a-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ce88a-124">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="ce88a-124">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="ce88a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce88a-125">Remarks</span></span>

<span data-ttu-id="ce88a-126">Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="ce88a-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="ce88a-127">Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce88a-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="ce88a-128">Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="ce88a-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce88a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce88a-129">Requirements</span></span>



| <span data-ttu-id="ce88a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce88a-130">Requirement</span></span> | <span data-ttu-id="ce88a-131">Value</span><span class="sxs-lookup"><span data-stu-id="ce88a-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce88a-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce88a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ce88a-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ce88a-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ce88a-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ce88a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ce88a-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ce88a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ce88a-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="ce88a-136">End of client support</span></span><br/>    | <span data-ttu-id="ce88a-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ce88a-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="ce88a-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="ce88a-138">End of server support</span></span><br/>    | <span data-ttu-id="ce88a-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ce88a-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="ce88a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce88a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce88a-141">**Invalidar**</span><span class="sxs-lookup"><span data-stu-id="ce88a-141">**Invalidate**</span></span>](iscardfileaccess-invalidate.md)
</dt> <dt>

[<span data-ttu-id="ce88a-142">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="ce88a-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
