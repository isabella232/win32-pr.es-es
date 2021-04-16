---
description: La función SetDwordInBlob establece el valor DWORD con nombre de un BLOB.
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: Función SetDwordInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9bca0efe61824c6fb8dd41b0b241791b6303799d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677638"
---
# <a name="setdwordinblob-function"></a><span data-ttu-id="0aa2b-103">SetDwordInBlob función)</span><span class="sxs-lookup"><span data-stu-id="0aa2b-103">SetDwordInBlob function</span></span>

<span data-ttu-id="0aa2b-104">La función **SetDwordInBlob** establece el valor **DWORD** con nombre de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="0aa2b-104">The **SetDwordInBlob** function sets the named **DWORD** value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa2b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0aa2b-105">Syntax</span></span>


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a><span data-ttu-id="0aa2b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0aa2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0aa2b-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aa2b-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa2b-108">Identificador de un BLOB que se está configurando.</span><span class="sxs-lookup"><span data-stu-id="0aa2b-108">Handle to a BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="0aa2b-109">*pOwnerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aa2b-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa2b-110">Puntero al nombre del **propietario** del BLOB que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="0aa2b-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="0aa2b-111">*pCategoryName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aa2b-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa2b-112">Puntero al nombre de la **categoría** de BLOB que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="0aa2b-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="0aa2b-113">*pTagName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aa2b-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa2b-114">Puntero al nombre de la **etiqueta** de BLOB que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="0aa2b-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="0aa2b-115">*DWORD* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0aa2b-115">*Dword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0aa2b-116">Valor **DWORD** del BLOB que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="0aa2b-116">**DWORD** value of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0aa2b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0aa2b-117">Return value</span></span>

<span data-ttu-id="0aa2b-118">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0aa2b-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0aa2b-119">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="0aa2b-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa2b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0aa2b-120">Requirements</span></span>



| <span data-ttu-id="0aa2b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa2b-121">Requirement</span></span> | <span data-ttu-id="0aa2b-122">Value</span><span class="sxs-lookup"><span data-stu-id="0aa2b-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa2b-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0aa2b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa2b-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0aa2b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0aa2b-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0aa2b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa2b-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0aa2b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0aa2b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0aa2b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa2b-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aa2b-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="0aa2b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0aa2b-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0aa2b-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0aa2b-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="0aa2b-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0aa2b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0aa2b-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0aa2b-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aa2b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0aa2b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa2b-134">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="0aa2b-134">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="0aa2b-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="0aa2b-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="0aa2b-136">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="0aa2b-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="0aa2b-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="0aa2b-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="0aa2b-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="0aa2b-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="0aa2b-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="0aa2b-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="0aa2b-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="0aa2b-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="0aa2b-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="0aa2b-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="0aa2b-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="0aa2b-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




