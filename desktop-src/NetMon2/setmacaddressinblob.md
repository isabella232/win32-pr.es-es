---
description: La función SetMacAddressInBlob establece la dirección MAC solicitada de un BLOB.
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: Función SetMacAddressInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2183f5635dcdb15362a86a77ae2b3c109c71dbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911317"
---
# <a name="setmacaddressinblob-function"></a><span data-ttu-id="714da-103">SetMacAddressInBlob función)</span><span class="sxs-lookup"><span data-stu-id="714da-103">SetMacAddressInBlob function</span></span>

<span data-ttu-id="714da-104">La función **SetMacAddressInBlob** establece la dirección Mac solicitada de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="714da-104">The **SetMacAddressInBlob** function sets the requested MAC address of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="714da-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="714da-105">Syntax</span></span>


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="714da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="714da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="714da-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="714da-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="714da-108">Identificador del BLOB que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="714da-108">Handle to the BLOB being set.</span></span>

</dd> <dt>

<span data-ttu-id="714da-109">*pOwnerName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="714da-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="714da-110">Puntero al nombre del **propietario** del BLOB que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="714da-110">Pointer to the BLOB **Owner** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="714da-111">*pCategoryName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="714da-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="714da-112">Puntero al nombre de la **categoría** de BLOB que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="714da-112">Pointer to the BLOB **Category** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="714da-113">*pTagName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="714da-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="714da-114">Puntero al nombre de la **etiqueta** de BLOB que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="714da-114">Pointer to the BLOB **Tag** name being set.</span></span>

</dd> <dt>

<span data-ttu-id="714da-115">*pMacAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="714da-115">*pMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="714da-116">Puntero a la dirección MAC del BLOB que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="714da-116">Pointer to the MAC address of the BLOB being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="714da-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="714da-117">Return value</span></span>

<span data-ttu-id="714da-118">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="714da-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="714da-119">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="714da-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="714da-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="714da-120">Requirements</span></span>



| <span data-ttu-id="714da-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="714da-121">Requirement</span></span> | <span data-ttu-id="714da-122">Value</span><span class="sxs-lookup"><span data-stu-id="714da-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="714da-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="714da-123">Minimum supported client</span></span><br/> | <span data-ttu-id="714da-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="714da-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="714da-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="714da-125">Minimum supported server</span></span><br/> | <span data-ttu-id="714da-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="714da-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="714da-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="714da-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="714da-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="714da-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="714da-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="714da-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="714da-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="714da-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="714da-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="714da-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="714da-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="714da-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="714da-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="714da-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="714da-134">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="714da-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="714da-135">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="714da-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="714da-136">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="714da-136">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="714da-137">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="714da-137">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="714da-138">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="714da-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="714da-139">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="714da-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="714da-140">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="714da-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="714da-141">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="714da-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="714da-142">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="714da-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




