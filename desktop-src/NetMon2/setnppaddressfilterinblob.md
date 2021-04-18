---
description: La función SetNPPAddressFilterInBlob establece el filtro de dirección determinado en el BLOB.
ms.assetid: bdd1482d-8be0-4999-9a7a-16b0400412fb
title: Función SetNPPAddressFilterInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPAddressFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 39e8a85599fa63b1320d707f648731a195dbb48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678427"
---
# <a name="setnppaddressfilterinblob-function"></a><span data-ttu-id="4880a-103">SetNPPAddressFilterInBlob función)</span><span class="sxs-lookup"><span data-stu-id="4880a-103">SetNPPAddressFilterInBlob function</span></span>

<span data-ttu-id="4880a-104">La función **SetNPPAddressFilterInBlob** establece el filtro de dirección determinado en el BLOB.</span><span class="sxs-lookup"><span data-stu-id="4880a-104">The **SetNPPAddressFilterInBlob** function sets the given address filter in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="4880a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4880a-105">Syntax</span></span>


```C++
DWORD SetNPPAddressFilterInBlob(
  _In_ HBLOB          hBlob,
  _In_ LPADDRESSTABLE pAddressTable
);
```



## <a name="parameters"></a><span data-ttu-id="4880a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4880a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4880a-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4880a-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4880a-108">Identificador de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="4880a-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="4880a-109">*pAddressTable* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4880a-109">*pAddressTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4880a-110">Puntero a una estructura [**ADDRESSTABLE**](addresstable.md) que define la tabla de direcciones asignada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="4880a-110">Pointer to an [**ADDRESSTABLE**](addresstable.md) structure that defines the user-allocated address table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4880a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4880a-111">Return value</span></span>

<span data-ttu-id="4880a-112">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4880a-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="4880a-113">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="4880a-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4880a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4880a-114">Requirements</span></span>



| <span data-ttu-id="4880a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4880a-115">Requirement</span></span> | <span data-ttu-id="4880a-116">Value</span><span class="sxs-lookup"><span data-stu-id="4880a-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4880a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4880a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4880a-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4880a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4880a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4880a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4880a-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4880a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4880a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4880a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="4880a-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="4880a-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="4880a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4880a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="4880a-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4880a-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="4880a-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4880a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4880a-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4880a-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4880a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4880a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4880a-128">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="4880a-128">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="4880a-129">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="4880a-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="4880a-130">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="4880a-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="4880a-131">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="4880a-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="4880a-132">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="4880a-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="4880a-133">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="4880a-133">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="4880a-134">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="4880a-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="4880a-135">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="4880a-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="4880a-136">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="4880a-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




