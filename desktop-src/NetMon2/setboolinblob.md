---
description: La función SetBoolInBlob establece un valor booleano en una ubicación determinada dentro de un BLOB.
ms.assetid: 354d22be-b8c4-4068-8356-19b30ac188d0
title: Función SetBoolInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetBoolInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5cfbb9a3410d511ab143f1d77584a0144435c230
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544878"
---
# <a name="setboolinblob-function"></a><span data-ttu-id="2be02-103">SetBoolInBlob función)</span><span class="sxs-lookup"><span data-stu-id="2be02-103">SetBoolInBlob function</span></span>

<span data-ttu-id="2be02-104">La función **SetBoolInBlob** establece un valor booleano en una ubicación determinada dentro de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="2be02-104">The **SetBoolInBlob** function sets a Boolean value at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be02-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2be02-105">Syntax</span></span>


```C++
DWORD SetBoolInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       BOOL  Bool
);
```



## <a name="parameters"></a><span data-ttu-id="2be02-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2be02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be02-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2be02-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2be02-108">Identificador de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="2be02-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="2be02-109">*pOwnerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2be02-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2be02-110">Puntero al nombre del **propietario** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="2be02-110">Pointer to the BLOB **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="2be02-111">*pCategoryName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2be02-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2be02-112">Puntero al nombre de la **categoría** de BLOB.</span><span class="sxs-lookup"><span data-stu-id="2be02-112">Pointer to the BLOB **Category** name.</span></span>

</dd> <dt>

<span data-ttu-id="2be02-113">*pTagName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2be02-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2be02-114">Puntero al nombre de la **etiqueta** de BLOB.</span><span class="sxs-lookup"><span data-stu-id="2be02-114">Pointer to the BLOB **Tag** name.</span></span>

</dd> <dt>

<span data-ttu-id="2be02-115">*Booleano* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2be02-115">*Bool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2be02-116">Valor booleano que se establece en la ubicación especificada.</span><span class="sxs-lookup"><span data-stu-id="2be02-116">Boolean value that is set at the given location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2be02-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2be02-117">Return value</span></span>

<span data-ttu-id="2be02-118">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2be02-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2be02-119">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="2be02-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2be02-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2be02-120">Requirements</span></span>



| <span data-ttu-id="2be02-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2be02-121">Requirement</span></span> | <span data-ttu-id="2be02-122">Value</span><span class="sxs-lookup"><span data-stu-id="2be02-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2be02-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2be02-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2be02-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2be02-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2be02-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2be02-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2be02-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2be02-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2be02-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2be02-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2be02-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2be02-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="2be02-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2be02-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="2be02-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2be02-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="2be02-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2be02-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2be02-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2be02-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2be02-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2be02-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be02-134">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="2be02-134">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="2be02-135">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="2be02-135">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="2be02-136">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="2be02-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="2be02-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="2be02-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="2be02-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="2be02-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="2be02-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="2be02-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="2be02-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="2be02-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="2be02-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="2be02-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="2be02-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="2be02-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




