---
description: La función GetNPPPatternFilterFromBlob recupera el filtro de coincidencia de patrones de un BLOB específico.
ms.assetid: b17cde55-8abb-4699-960f-676cbbb24326
title: Función GetNPPPatternFilterFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPPatternFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5758c53fe21231d300058a9168e556e9f9ceaa43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808713"
---
# <a name="getnpppatternfilterfromblob-function"></a><span data-ttu-id="5f4b3-103">GetNPPPatternFilterFromBlob función)</span><span class="sxs-lookup"><span data-stu-id="5f4b3-103">GetNPPPatternFilterFromBlob function</span></span>

<span data-ttu-id="5f4b3-104">La función **GetNPPPatternFilterFromBlob** recupera el filtro de coincidencia de patrones de un BLOB específico.</span><span class="sxs-lookup"><span data-stu-id="5f4b3-104">The **GetNPPPatternFilterFromBlob** function retrieves the pattern match filter from a specific BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f4b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f4b3-105">Syntax</span></span>


```C++
DWORD GetNPPPatternFilterFromBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="5f4b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f4b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f4b3-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5f4b3-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4b3-108">Identificador del BLOB.</span><span class="sxs-lookup"><span data-stu-id="5f4b3-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="5f4b3-109">*pExpression* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5f4b3-109">*pExpression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4b3-110">Puntero a la expresión de filtro.</span><span class="sxs-lookup"><span data-stu-id="5f4b3-110">Pointer to the filter expression.</span></span>

</dd> <dt>

<span data-ttu-id="5f4b3-111">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5f4b3-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f4b3-112">Identificador de un BLOB de error que especifica dónde se produjo el error (si existe) en el BLOB original.</span><span class="sxs-lookup"><span data-stu-id="5f4b3-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f4b3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5f4b3-113">Return value</span></span>

<span data-ttu-id="5f4b3-114">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5f4b3-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5f4b3-115">Si la función no es correcta, el valor devuelto es un NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="5f4b3-115">If the function is unsuccessful, the return value is a NMERR that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f4b3-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f4b3-116">Remarks</span></span>

<span data-ttu-id="5f4b3-117">La información del filtro de coincidencia de patrones se almacena en la categoría de **configuración** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="5f4b3-117">The pattern match filter information is stored in the **Config** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f4b3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f4b3-118">Requirements</span></span>



| <span data-ttu-id="5f4b3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f4b3-119">Requirement</span></span> | <span data-ttu-id="5f4b3-120">Value</span><span class="sxs-lookup"><span data-stu-id="5f4b3-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f4b3-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f4b3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f4b3-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5f4b3-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5f4b3-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f4b3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f4b3-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5f4b3-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f4b3-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f4b3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f4b3-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f4b3-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="5f4b3-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f4b3-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f4b3-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f4b3-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="5f4b3-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f4b3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f4b3-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f4b3-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f4b3-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f4b3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f4b3-132">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="5f4b3-132">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="5f4b3-133">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="5f4b3-133">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="5f4b3-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="5f4b3-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="5f4b3-135">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="5f4b3-135">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="5f4b3-136">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="5f4b3-136">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="5f4b3-137">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="5f4b3-137">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="5f4b3-138">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="5f4b3-138">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="5f4b3-139">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="5f4b3-139">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="5f4b3-140">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="5f4b3-140">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="5f4b3-141">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="5f4b3-141">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




