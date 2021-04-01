---
description: Establece el desencadenador de BLOBs.
ms.assetid: 88bfd5cd-f563-4d0c-81a3-54a846805b87
title: Función SetNPPTriggerInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPTriggerInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 05b8bb3f7f95dc3246ef10f3945b9ab0868550cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275549"
---
# <a name="setnpptriggerinblob-function"></a><span data-ttu-id="f0724-103">SetNPPTriggerInBlob función)</span><span class="sxs-lookup"><span data-stu-id="f0724-103">SetNPPTriggerInBlob function</span></span>

<span data-ttu-id="f0724-104">La función **SetNPPTriggerInBlob** establece el desencadenador de blobs.</span><span class="sxs-lookup"><span data-stu-id="f0724-104">The **SetNPPTriggerInBlob** function sets the BLOB trigger.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0724-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0724-105">Syntax</span></span>


```C++
DWORD SetNPPTriggerInBlob(
  _In_  HBLOB     hBlob,
  _In_  LPTRIGGER pTrigger,
  _Out_ HBLOB     hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="f0724-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0724-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0724-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0724-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0724-108">Identificador del BLOB.</span><span class="sxs-lookup"><span data-stu-id="f0724-108">The handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="f0724-109">*pTrigger* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f0724-109">*pTrigger* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0724-110">Puntero al valor del desencadenador.</span><span class="sxs-lookup"><span data-stu-id="f0724-110">A pointer to the trigger value.</span></span>

</dd> <dt>

<span data-ttu-id="f0724-111">*hErrorBlob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f0724-111">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0724-112">Identificador de un BLOB de error que especifica dónde se produjo el error (si existe) en el BLOB original.</span><span class="sxs-lookup"><span data-stu-id="f0724-112">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0724-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0724-113">Return value</span></span>

<span data-ttu-id="f0724-114">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f0724-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f0724-115">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="f0724-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0724-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0724-116">Remarks</span></span>

<span data-ttu-id="f0724-117">Estos datos del desencadenador se almacenan en la categoría **desencadenador** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="f0724-117">This trigger data is stored in the **Trigger** category of the BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0724-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0724-118">Requirements</span></span>



| <span data-ttu-id="f0724-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0724-119">Requirement</span></span> | <span data-ttu-id="f0724-120">Value</span><span class="sxs-lookup"><span data-stu-id="f0724-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0724-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0724-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f0724-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f0724-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f0724-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0724-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f0724-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f0724-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0724-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0724-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0724-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0724-126"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="f0724-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0724-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f0724-128"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0724-128"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="f0724-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0724-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0724-130"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0724-130"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0724-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0724-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0724-132">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="f0724-132">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="f0724-133">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="f0724-133">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="f0724-134">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="f0724-134">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="f0724-135">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="f0724-135">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="f0724-136">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="f0724-136">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="f0724-137">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="f0724-137">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="f0724-138">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="f0724-138">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="f0724-139">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="f0724-139">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="f0724-140">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="f0724-140">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




