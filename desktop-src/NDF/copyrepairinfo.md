---
title: Función CopyRepairInfo (Ndattributils. h)
description: Crea una copia de una estructura RepairInfo.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- CopyRepairInfo función NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996173"
---
# <a name="copyrepairinfo-function"></a><span data-ttu-id="445a4-104">CopyRepairInfo función)</span><span class="sxs-lookup"><span data-stu-id="445a4-104">CopyRepairInfo function</span></span>

<span data-ttu-id="445a4-105">La función **CopyRepairInfo** crea una copia de una estructura [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .</span><span class="sxs-lookup"><span data-stu-id="445a4-105">The **CopyRepairInfo** function creates a copy of a [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="445a4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="445a4-106">Syntax</span></span>


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="445a4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="445a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="445a4-108">*Dest* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="445a4-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="445a4-109">Tipo: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="445a4-109">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="445a4-110">Estructura que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="445a4-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="445a4-111">_Source \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="445a4-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="445a4-112">Tipo: \**const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="445a4-112">Type: \**const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="445a4-113">La estructura existente que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="445a4-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="445a4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="445a4-114">Return value</span></span>

<span data-ttu-id="445a4-115">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="445a4-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="445a4-116">Los valores devueltos posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="445a4-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="445a4-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="445a4-117">Return code</span></span>                                                                                   | <span data-ttu-id="445a4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="445a4-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="445a4-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="445a4-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="445a4-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="445a4-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="445a4-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="445a4-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="445a4-122">No se ha proporcionado correctamente uno o más parámetros.</span><span class="sxs-lookup"><span data-stu-id="445a4-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="445a4-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="445a4-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="445a4-124">No hay suficiente memoria disponible para completar esta operación.</span><span class="sxs-lookup"><span data-stu-id="445a4-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="445a4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="445a4-125">Requirements</span></span>



| <span data-ttu-id="445a4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="445a4-126">Requirement</span></span> | <span data-ttu-id="445a4-127">Value</span><span class="sxs-lookup"><span data-stu-id="445a4-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="445a4-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="445a4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="445a4-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="445a4-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="445a4-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="445a4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="445a4-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="445a4-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="445a4-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="445a4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="445a4-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="445a4-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="445a4-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="445a4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="445a4-135">**RepairInfo**</span><span class="sxs-lookup"><span data-stu-id="445a4-135">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





