---
description: La función GetNPPTriggerFromBlob recupera el desencadenador del BLOB especificado.
ms.assetid: 48a27cf3-57b0-4241-a925-4209e0d384e2
title: Función GetNPPTriggerFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPTriggerFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 11622078354012de4796ddd43a698ac812951742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677278"
---
# <a name="getnpptriggerfromblob-function"></a><span data-ttu-id="107bc-103">GetNPPTriggerFromBlob función)</span><span class="sxs-lookup"><span data-stu-id="107bc-103">GetNPPTriggerFromBlob function</span></span>

<span data-ttu-id="107bc-104">La función **GetNPPTriggerFromBlob** recupera el desencadenador del BLOB especificado.</span><span class="sxs-lookup"><span data-stu-id="107bc-104">The **GetNPPTriggerFromBlob** function retrieves the trigger from the given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="107bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="107bc-105">Syntax</span></span>


```C++
DWORD GetNPPTriggerFromBlob(
  _In_  HBLOB     hBlob,
  _Out_ LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="107bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="107bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="107bc-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="107bc-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="107bc-108">Identificador del BLOB.</span><span class="sxs-lookup"><span data-stu-id="107bc-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="107bc-109">*pTrigger* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="107bc-109">*pTrigger* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="107bc-110">Puntero al valor del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="107bc-110">Pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="107bc-111">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="107bc-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="107bc-112">Identificador de un BLOB de error que especifica dónde se produjo el error (si existe) en el BLOB original.</span><span class="sxs-lookup"><span data-stu-id="107bc-112">Handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="107bc-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="107bc-113">Return value</span></span>

<span data-ttu-id="107bc-114">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="107bc-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="107bc-115">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="107bc-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="107bc-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="107bc-116">Remarks</span></span>

<span data-ttu-id="107bc-117">La información del desencadenador se almacena en la categoría **desencadenador** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="107bc-117">The trigger information is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="107bc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="107bc-118">Requirements</span></span>



| <span data-ttu-id="107bc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="107bc-119">Requirement</span></span> | <span data-ttu-id="107bc-120">Value</span><span class="sxs-lookup"><span data-stu-id="107bc-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="107bc-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="107bc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="107bc-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="107bc-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="107bc-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="107bc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="107bc-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="107bc-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="107bc-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="107bc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="107bc-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="107bc-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="107bc-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="107bc-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="107bc-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="107bc-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="107bc-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="107bc-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="107bc-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="107bc-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="107bc-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="107bc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="107bc-132">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="107bc-132">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="107bc-133">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="107bc-133">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="107bc-134">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="107bc-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="107bc-135">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="107bc-135">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="107bc-136">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="107bc-136">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="107bc-137">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="107bc-137">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="107bc-138">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="107bc-138">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="107bc-139">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="107bc-139">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="107bc-140">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="107bc-140">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




