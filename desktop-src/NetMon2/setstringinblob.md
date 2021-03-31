---
description: Establece una cadena en una ubicación determinada dentro de un BLOB.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: Función SetStringInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 37278b9111818957e6d5fb3032f1bf33ad3a6ec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275548"
---
# <a name="setstringinblob-function"></a><span data-ttu-id="6944f-103">SetStringInBlob función)</span><span class="sxs-lookup"><span data-stu-id="6944f-103">SetStringInBlob function</span></span>

<span data-ttu-id="6944f-104">La función **SetStringInBlob** establece una cadena en una ubicación determinada dentro de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="6944f-104">The **SetStringInBlob** function sets a string at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="6944f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6944f-105">Syntax</span></span>


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
);
```



## <a name="parameters"></a><span data-ttu-id="6944f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6944f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6944f-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6944f-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6944f-108">Identificador del BLOB.</span><span class="sxs-lookup"><span data-stu-id="6944f-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="6944f-109">*pOwnerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6944f-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6944f-110">Un puntero a la sección de **propietario** del BLOB, donde se establece la cadena.</span><span class="sxs-lookup"><span data-stu-id="6944f-110">A pointer to the **Owner** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="6944f-111">*pCategoryName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6944f-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6944f-112">Un puntero a la sección de **categoría** del BLOB, donde se establece la cadena.</span><span class="sxs-lookup"><span data-stu-id="6944f-112">A pointer to the **Category** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="6944f-113">*pTagName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6944f-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6944f-114">Puntero a la **etiqueta** de la cadena solicitada.</span><span class="sxs-lookup"><span data-stu-id="6944f-114">A pointer to the **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="6944f-115">*pString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6944f-115">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6944f-116">Puntero a la variable en la que se devolverá un puntero a la cadena.</span><span class="sxs-lookup"><span data-stu-id="6944f-116">A pointer to the variable where a pointer to the string will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6944f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6944f-117">Return value</span></span>

<span data-ttu-id="6944f-118">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6944f-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6944f-119">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el problema.</span><span class="sxs-lookup"><span data-stu-id="6944f-119">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="6944f-120">Si la información de **propietario**, **categoría** o **etiqueta** especificada no existe, el valor devuelto es NMERR la entrada de \_ BLOB no \_ \_ \_ \_ existe.</span><span class="sxs-lookup"><span data-stu-id="6944f-120">If the specified **Owner**, **Category**, or **Tag** information does not exist, the return value is NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST.</span></span>

## <a name="requirements"></a><span data-ttu-id="6944f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6944f-121">Requirements</span></span>



| <span data-ttu-id="6944f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6944f-122">Requirement</span></span> | <span data-ttu-id="6944f-123">Value</span><span class="sxs-lookup"><span data-stu-id="6944f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6944f-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6944f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6944f-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6944f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6944f-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6944f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6944f-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6944f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6944f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6944f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6944f-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6944f-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="6944f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6944f-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="6944f-131"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6944f-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="6944f-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6944f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6944f-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6944f-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6944f-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="6944f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6944f-135">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="6944f-135">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="6944f-136">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="6944f-136">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="6944f-137">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="6944f-137">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="6944f-138">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="6944f-138">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="6944f-139">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="6944f-139">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="6944f-140">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="6944f-140">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="6944f-141">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="6944f-141">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="6944f-142">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="6944f-142">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="6944f-143">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="6944f-143">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> </dl>

 

 




