---
description: La función SetClassIDInBlob establece el valor de identificador de clase con nombre de un BLOB.
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: Función SetClassIDInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b617c39767038bac51d749a640ebcf2301e0c63f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677637"
---
# <a name="setclassidinblob-function"></a><span data-ttu-id="fc7e6-103">SetClassIDInBlob función)</span><span class="sxs-lookup"><span data-stu-id="fc7e6-103">SetClassIDInBlob function</span></span>

<span data-ttu-id="fc7e6-104">La función **SetClassIDInBlob** establece el valor de identificador de clase con nombre de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="fc7e6-104">The **SetClassIDInBlob** function sets the named class identifier value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc7e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc7e6-105">Syntax</span></span>


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="fc7e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc7e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc7e6-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc7e6-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc7e6-108">Identificador de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="fc7e6-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="fc7e6-109">*pOwnerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc7e6-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc7e6-110">Puntero al nombre del **propietario** del BLOB que se establece.</span><span class="sxs-lookup"><span data-stu-id="fc7e6-110">Pointer to the BLOB **Owner** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="fc7e6-111">*pCategoryName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc7e6-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc7e6-112">Puntero al nombre de la **categoría** de BLOB que se establece.</span><span class="sxs-lookup"><span data-stu-id="fc7e6-112">Pointer to the BLOB **Category** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="fc7e6-113">*pTagName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc7e6-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc7e6-114">Puntero al nombre de la **etiqueta** de BLOB que se establece.</span><span class="sxs-lookup"><span data-stu-id="fc7e6-114">Pointer to the BLOB **Tag** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="fc7e6-115">*pClsID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc7e6-115">*pClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc7e6-116">Puntero al identificador de clase del BLOB que se establece.</span><span class="sxs-lookup"><span data-stu-id="fc7e6-116">Pointer to the class identifier of the BLOB that is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc7e6-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc7e6-117">Return value</span></span>

<span data-ttu-id="fc7e6-118">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="fc7e6-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="fc7e6-119">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="fc7e6-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc7e6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc7e6-120">Requirements</span></span>



| <span data-ttu-id="fc7e6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc7e6-121">Requirement</span></span> | <span data-ttu-id="fc7e6-122">Value</span><span class="sxs-lookup"><span data-stu-id="fc7e6-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc7e6-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc7e6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fc7e6-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fc7e6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fc7e6-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc7e6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fc7e6-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fc7e6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fc7e6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc7e6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc7e6-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc7e6-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="fc7e6-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc7e6-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc7e6-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc7e6-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="fc7e6-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc7e6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc7e6-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc7e6-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc7e6-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc7e6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc7e6-134">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="fc7e6-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="fc7e6-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="fc7e6-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="fc7e6-136">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="fc7e6-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="fc7e6-137">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="fc7e6-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="fc7e6-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="fc7e6-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="fc7e6-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="fc7e6-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="fc7e6-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="fc7e6-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="fc7e6-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="fc7e6-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="fc7e6-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="fc7e6-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




