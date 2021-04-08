---
title: Función CopyRootCauseInfo (Ndattributils. h)
description: Crea una copia de una estructura RootCauseInfo.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- CopyRootCauseInfo función NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5093d7af6458668a763aa206cacd22a0526aa521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996174"
---
# <a name="copyrootcauseinfo-function"></a><span data-ttu-id="75a4f-104">CopyRootCauseInfo función)</span><span class="sxs-lookup"><span data-stu-id="75a4f-104">CopyRootCauseInfo function</span></span>

<span data-ttu-id="75a4f-105">La función **CopyRootCauseInfo** crea una copia de una estructura [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .</span><span class="sxs-lookup"><span data-stu-id="75a4f-105">The **CopyRootCauseInfo** function creates a copy of a [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="75a4f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75a4f-106">Syntax</span></span>


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="75a4f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75a4f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75a4f-108">*Dest* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="75a4f-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75a4f-109">Tipo: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="75a4f-109">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="75a4f-110">Estructura que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="75a4f-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="75a4f-111">_Source \* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="75a4f-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75a4f-112">Tipo: \**const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="75a4f-112">Type: \**const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="75a4f-113">La estructura existente que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="75a4f-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75a4f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75a4f-114">Return value</span></span>

<span data-ttu-id="75a4f-115">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="75a4f-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="75a4f-116">Los valores devueltos posibles incluyen, entre otros, lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="75a4f-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="75a4f-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="75a4f-117">Return code</span></span>                                                                                   | <span data-ttu-id="75a4f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="75a4f-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="75a4f-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="75a4f-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="75a4f-120">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="75a4f-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="75a4f-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="75a4f-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="75a4f-122">No se ha proporcionado correctamente uno o más parámetros.</span><span class="sxs-lookup"><span data-stu-id="75a4f-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="75a4f-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="75a4f-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="75a4f-124">No hay suficiente memoria disponible para completar esta operación.</span><span class="sxs-lookup"><span data-stu-id="75a4f-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="75a4f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75a4f-125">Requirements</span></span>



| <span data-ttu-id="75a4f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="75a4f-126">Requirement</span></span> | <span data-ttu-id="75a4f-127">Value</span><span class="sxs-lookup"><span data-stu-id="75a4f-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="75a4f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75a4f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="75a4f-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="75a4f-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="75a4f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75a4f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="75a4f-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="75a4f-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="75a4f-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75a4f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="75a4f-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="75a4f-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75a4f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="75a4f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75a4f-135">**RootCauseInfo**</span><span class="sxs-lookup"><span data-stu-id="75a4f-135">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





