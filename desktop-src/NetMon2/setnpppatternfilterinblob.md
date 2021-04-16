---
description: Establece el filtro de coincidencia de patrones de BLOB.
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: Función SetNPPPatternFilterInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b2e8989264a042368b37926bbb502f48ab2fb04b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542358"
---
# <a name="setnpppatternfilterinblob-function"></a><span data-ttu-id="6d6ac-103">SetNPPPatternFilterInBlob función)</span><span class="sxs-lookup"><span data-stu-id="6d6ac-103">SetNPPPatternFilterInBlob function</span></span>

<span data-ttu-id="6d6ac-104">La función **SetNPPPatternFilterInBlob** establece el filtro de coincidencia de patrones de BLOB.</span><span class="sxs-lookup"><span data-stu-id="6d6ac-104">The **SetNPPPatternFilterInBlob** function sets the BLOB pattern match filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d6ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d6ac-105">Syntax</span></span>


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="6d6ac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d6ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d6ac-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d6ac-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d6ac-108">Identificador del BLOB.</span><span class="sxs-lookup"><span data-stu-id="6d6ac-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="6d6ac-109">*pExpression* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6d6ac-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d6ac-110">Puntero a una estructura de [expresión](expression.md) que define la expresión de filtro que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="6d6ac-110">A pointer to an [EXPRESSION](expression.md) structure that defines the filter expression being set.</span></span>

</dd> <dt>

<span data-ttu-id="6d6ac-111">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6d6ac-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d6ac-112">Identificador de un BLOB de error que especifica dónde se produjo el error (si existe) en el BLOB original.</span><span class="sxs-lookup"><span data-stu-id="6d6ac-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d6ac-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d6ac-113">Return value</span></span>

<span data-ttu-id="6d6ac-114">Si la función **SetNPPPatternFilterInBlob** se ejecuta correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6d6ac-114">If the **SetNPPPatternFilterInBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6d6ac-115">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="6d6ac-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d6ac-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d6ac-116">Remarks</span></span>

<span data-ttu-id="6d6ac-117">Los datos del filtro de coincidencia de patrones almacenados en la categoría de **configuración** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="6d6ac-117">The pattern match filter data stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d6ac-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d6ac-118">Requirements</span></span>



| <span data-ttu-id="6d6ac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d6ac-119">Requirement</span></span> | <span data-ttu-id="6d6ac-120">Value</span><span class="sxs-lookup"><span data-stu-id="6d6ac-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d6ac-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d6ac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6d6ac-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6d6ac-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6d6ac-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d6ac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6d6ac-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6d6ac-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d6ac-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d6ac-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d6ac-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d6ac-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="6d6ac-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d6ac-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d6ac-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d6ac-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d6ac-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6d6ac-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d6ac-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d6ac-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d6ac-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d6ac-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d6ac-132">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="6d6ac-132">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="6d6ac-133">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="6d6ac-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="6d6ac-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="6d6ac-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="6d6ac-135">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="6d6ac-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="6d6ac-136">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="6d6ac-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="6d6ac-137">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="6d6ac-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="6d6ac-138">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="6d6ac-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="6d6ac-139">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="6d6ac-139">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="6d6ac-140">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="6d6ac-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




