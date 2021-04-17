---
description: La función GetMacAddressFromBlob recupera la dirección MAC con nombre de un BLOB.
ms.assetid: 1769c92c-0946-447c-885a-fcf175fa1bf3
title: Función GetMacAddressFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetMacAddressFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 022d4f618c09652c368f6664b194b4ebafc81717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688446"
---
# <a name="getmacaddressfromblob-function"></a><span data-ttu-id="28ff5-103">GetMacAddressFromBlob función)</span><span class="sxs-lookup"><span data-stu-id="28ff5-103">GetMacAddressFromBlob function</span></span>

<span data-ttu-id="28ff5-104">La función **GetMacAddressFromBlob** recupera la dirección Mac con nombre de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="28ff5-104">The **GetMacAddressFromBlob** function retrieves the named MAC address from a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ff5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28ff5-105">Syntax</span></span>


```C++
DWORD GetMacAddressFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="28ff5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28ff5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28ff5-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28ff5-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ff5-108">Identificador de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="28ff5-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="28ff5-109">*pOwnerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28ff5-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ff5-110">Puntero al nombre del propietario del BLOB.</span><span class="sxs-lookup"><span data-stu-id="28ff5-110">Pointer to the BLOB owner name.</span></span>

</dd> <dt>

<span data-ttu-id="28ff5-111">*pCategoryName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28ff5-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ff5-112">Puntero al nombre de la categoría de BLOB.</span><span class="sxs-lookup"><span data-stu-id="28ff5-112">Pointer to the BLOB category name.</span></span>

</dd> <dt>

<span data-ttu-id="28ff5-113">*pTagName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="28ff5-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28ff5-114">Puntero al nombre de la etiqueta de BLOB.</span><span class="sxs-lookup"><span data-stu-id="28ff5-114">Pointer to the BLOB tag name.</span></span>

</dd> <dt>

<span data-ttu-id="28ff5-115">*pMacAddress* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="28ff5-115">*pMacAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28ff5-116">Puntero a la dirección MAC del BLOB.</span><span class="sxs-lookup"><span data-stu-id="28ff5-116">Pointer to the MAC address of the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28ff5-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28ff5-117">Return value</span></span>

<span data-ttu-id="28ff5-118">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="28ff5-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="28ff5-119">Si la función no es correcta, el valor devuelto es un valor de NMERR que describe el error.</span><span class="sxs-lookup"><span data-stu-id="28ff5-119">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="28ff5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28ff5-120">Requirements</span></span>



| <span data-ttu-id="28ff5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="28ff5-121">Requirement</span></span> | <span data-ttu-id="28ff5-122">Value</span><span class="sxs-lookup"><span data-stu-id="28ff5-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28ff5-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28ff5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="28ff5-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="28ff5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="28ff5-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28ff5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="28ff5-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="28ff5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="28ff5-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28ff5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="28ff5-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="28ff5-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="28ff5-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28ff5-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="28ff5-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28ff5-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="28ff5-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28ff5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28ff5-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28ff5-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28ff5-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="28ff5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28ff5-134">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="28ff5-134">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="28ff5-135">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="28ff5-135">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="28ff5-136">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="28ff5-136">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="28ff5-137">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="28ff5-137">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="28ff5-138">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="28ff5-138">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="28ff5-139">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="28ff5-139">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="28ff5-140">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="28ff5-140">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="28ff5-141">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="28ff5-141">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="28ff5-142">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="28ff5-142">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="28ff5-143">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="28ff5-143">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




