---
description: Recupera un valor booleano con nombre de un BLOB.
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: Función GetBoolFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBoolFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e09a35f71181343cd401b3288c2b2c74a46f677b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677284"
---
# <a name="getboolfromblob-function"></a><span data-ttu-id="652e2-103">GetBoolFromBlob función)</span><span class="sxs-lookup"><span data-stu-id="652e2-103">GetBoolFromBlob function</span></span>

<span data-ttu-id="652e2-104">La función **GetBoolFromBlob** recupera un valor booleano con nombre de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="652e2-104">The **GetBoolFromBlob** function retrieves a named Boolean value from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="652e2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="652e2-105">Syntax</span></span>


```C++
DWORD GetBoolFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BOOL  *pBool
);
```



## <a name="parameters"></a><span data-ttu-id="652e2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="652e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="652e2-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="652e2-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="652e2-108">Identificador de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="652e2-108">A handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="652e2-109">*pOwnerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="652e2-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="652e2-110">Puntero al nombre del propietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="652e2-110">A pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="652e2-111">*pCategoryName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="652e2-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="652e2-112">Puntero al nombre de la categoría de BLOB.</span><span class="sxs-lookup"><span data-stu-id="652e2-112">A pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="652e2-113">*pTagName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="652e2-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="652e2-114">Puntero al nombre de la etiqueta de BLOB.</span><span class="sxs-lookup"><span data-stu-id="652e2-114">A pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="652e2-115">*pBool* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="652e2-115">*pBool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="652e2-116">Puntero al valor booleano del BLOB.</span><span class="sxs-lookup"><span data-stu-id="652e2-116">Pointer to the Boolean value of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="652e2-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="652e2-117">Return value</span></span>

<span data-ttu-id="652e2-118">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="652e2-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="652e2-119">Si la función no es correcta, el valor devuelto es un valor de NMERR que describe el error.</span><span class="sxs-lookup"><span data-stu-id="652e2-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="652e2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="652e2-120">Requirements</span></span>



| <span data-ttu-id="652e2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="652e2-121">Requirement</span></span> | <span data-ttu-id="652e2-122">Value</span><span class="sxs-lookup"><span data-stu-id="652e2-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="652e2-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="652e2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="652e2-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="652e2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="652e2-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="652e2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="652e2-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="652e2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="652e2-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="652e2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="652e2-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="652e2-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="652e2-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="652e2-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="652e2-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="652e2-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="652e2-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="652e2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="652e2-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="652e2-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="652e2-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="652e2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="652e2-134">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="652e2-134">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="652e2-135">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="652e2-135">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="652e2-136">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="652e2-136">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="652e2-137">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="652e2-137">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="652e2-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="652e2-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="652e2-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="652e2-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="652e2-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="652e2-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="652e2-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="652e2-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="652e2-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="652e2-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="652e2-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="652e2-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




