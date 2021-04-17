---
title: Función CopyHelperAttribute (Ndattributils. h)
description: Crea una copia de una estructura de \_ atributo auxiliar.
ms.assetid: ff49be29-4cd8-4730-929f-c66a7325704f
keywords:
- CopyHelperAttribute función NDF
topic_type:
- apiref
api_name:
- CopyHelperAttribute
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59fac3449ee48659980681c836d24406c4db7e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676695"
---
# <a name="copyhelperattribute-function"></a><span data-ttu-id="4acbb-104">CopyHelperAttribute función)</span><span class="sxs-lookup"><span data-stu-id="4acbb-104">CopyHelperAttribute function</span></span>

<span data-ttu-id="4acbb-105">La función **CopyHelperAttribute** crea una copia de una estructura de [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .</span><span class="sxs-lookup"><span data-stu-id="4acbb-105">The **CopyHelperAttribute** function creates a copy of a [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4acbb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4acbb-106">Syntax</span></span>


```C++
HRESULT CopyHelperAttribute(
  _Out_       HELPER_ATTRIBUTE *Dest,
  _In_  const HELPER_ATTRIBUTE *Source
);
```



## <a name="parameters"></a><span data-ttu-id="4acbb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4acbb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4acbb-108">*Dest* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4acbb-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4acbb-109">Tipo: \**\* [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _</span><span class="sxs-lookup"><span data-stu-id="4acbb-109">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="4acbb-110">Estructura que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="4acbb-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="4acbb-111">_Source \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="4acbb-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4acbb-112">Tipo: \**\* [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)const* _</span><span class="sxs-lookup"><span data-stu-id="4acbb-112">Type: \**const [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="4acbb-113">La estructura existente que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="4acbb-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4acbb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4acbb-114">Return value</span></span>

<span data-ttu-id="4acbb-115">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4acbb-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4acbb-116">Los valores devueltos posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="4acbb-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="4acbb-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4acbb-117">Return code</span></span>                                                                                   | <span data-ttu-id="4acbb-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4acbb-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4acbb-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4acbb-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4acbb-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="4acbb-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="4acbb-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4acbb-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4acbb-122">No se ha proporcionado correctamente uno o más parámetros.</span><span class="sxs-lookup"><span data-stu-id="4acbb-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="4acbb-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4acbb-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4acbb-124">No hay suficiente memoria disponible para completar esta operación.</span><span class="sxs-lookup"><span data-stu-id="4acbb-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4acbb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4acbb-125">Requirements</span></span>



| <span data-ttu-id="4acbb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4acbb-126">Requirement</span></span> | <span data-ttu-id="4acbb-127">Value</span><span class="sxs-lookup"><span data-stu-id="4acbb-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4acbb-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4acbb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4acbb-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4acbb-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4acbb-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4acbb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4acbb-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4acbb-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4acbb-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4acbb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4acbb-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="4acbb-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4acbb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="4acbb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4acbb-135">**atributo auxiliar \_**</span><span class="sxs-lookup"><span data-stu-id="4acbb-135">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> </dl>

 

 





