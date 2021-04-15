---
description: Devuelve una cadena ubicada en una posición determinada dentro de un BLOB.
ms.assetid: 5930a30b-f0ed-4d5b-a0ba-6cead55c2fcd
title: Función GetStringFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 475600fb6128b5dbbaf9333f8c550351831f0a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496996"
---
# <a name="getstringfromblob-function"></a><span data-ttu-id="f5aee-103">GetStringFromBlob función)</span><span class="sxs-lookup"><span data-stu-id="f5aee-103">GetStringFromBlob function</span></span>

<span data-ttu-id="f5aee-104">La función **GetStringFromBlob** devuelve una cadena ubicada en una posición determinada dentro de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="f5aee-104">The **GetStringFromBlob** function returns a string located at a given position within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5aee-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5aee-105">Syntax</span></span>


```C++
DWORD GetStringFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_ const char  **ppString
);
```



## <a name="parameters"></a><span data-ttu-id="f5aee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5aee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5aee-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5aee-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5aee-108">Identificador del BLOB.</span><span class="sxs-lookup"><span data-stu-id="f5aee-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="f5aee-109">*pOwnerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5aee-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5aee-110">Una sección del **propietario** del BLOB donde se encuentra la cadena.</span><span class="sxs-lookup"><span data-stu-id="f5aee-110">A BLOB **Owner** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="f5aee-111">*pCategoryName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5aee-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5aee-112">Una sección de **categoría** de BLOB donde se encuentra la cadena.</span><span class="sxs-lookup"><span data-stu-id="f5aee-112">A BLOB **Category** section where the string is located.</span></span>

</dd> <dt>

<span data-ttu-id="f5aee-113">*pTagName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5aee-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5aee-114">**Etiqueta** de la cadena solicitada.</span><span class="sxs-lookup"><span data-stu-id="f5aee-114">The **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="f5aee-115">*ppString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f5aee-115">*ppString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5aee-116">Puntero a una variable que apunta a la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="f5aee-116">A pointer to a variable that points to the returned string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5aee-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5aee-117">Return value</span></span>

<span data-ttu-id="f5aee-118">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f5aee-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f5aee-119">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="f5aee-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

<span data-ttu-id="f5aee-120">Si el **propietario**, la **categoría** o los datos de **etiqueta** especificados no existen, la función devuelve la **entrada de BLOB NMERR no \_ \_ \_ \_ \_ existe**.</span><span class="sxs-lookup"><span data-stu-id="f5aee-120">If the specified **Owner**, **Category**, or **Tag** data does not exist, the function returns **NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5aee-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5aee-121">Requirements</span></span>



| <span data-ttu-id="f5aee-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5aee-122">Requirement</span></span> | <span data-ttu-id="f5aee-123">Value</span><span class="sxs-lookup"><span data-stu-id="f5aee-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5aee-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5aee-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f5aee-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f5aee-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f5aee-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5aee-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f5aee-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f5aee-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5aee-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5aee-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5aee-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5aee-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="f5aee-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5aee-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5aee-131"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5aee-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="f5aee-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5aee-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5aee-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5aee-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5aee-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5aee-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5aee-135">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="f5aee-135">SetStringInBlob</span></span>](setstringinblob.md)
</dt> <dt>

[<span data-ttu-id="f5aee-136">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="f5aee-136">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="f5aee-137">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="f5aee-137">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="f5aee-138">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="f5aee-138">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="f5aee-139">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="f5aee-139">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="f5aee-140">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="f5aee-140">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="f5aee-141">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="f5aee-141">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="f5aee-142">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="f5aee-142">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="f5aee-143">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="f5aee-143">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="f5aee-144">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="f5aee-144">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




