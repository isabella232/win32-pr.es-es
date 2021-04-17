---
description: La función GetNetworkInfoFromBlob recupera información de red de un BLOB determinado.
ms.assetid: 217c33f4-e548-4072-9edd-ded61e6cd743
title: Función GetNetworkInfoFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNetworkInfoFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2f8b15dce010febdc952c2527a9f4ad31054fa3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678584"
---
# <a name="getnetworkinfofromblob-function"></a><span data-ttu-id="e2810-103">GetNetworkInfoFromBlob función)</span><span class="sxs-lookup"><span data-stu-id="e2810-103">GetNetworkInfoFromBlob function</span></span>

<span data-ttu-id="e2810-104">La función **GetNetworkInfoFromBlob** recupera información de red de un BLOB determinado.</span><span class="sxs-lookup"><span data-stu-id="e2810-104">The **GetNetworkInfoFromBlob** function retrieves network information from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2810-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2810-105">Syntax</span></span>


```C++
DWORD GetNetworkInfoFromBlob(
  _In_    HBLOB         hBlob,
  _Inout_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e2810-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e2810-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2810-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e2810-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2810-108">Identificador de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="e2810-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="e2810-109">*lpNetworkInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e2810-109">*lpNetworkInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2810-110">Puntero a la estructura [NETWORKINFO](networkinfo.md) asignada por el usuario que se rellena.</span><span class="sxs-lookup"><span data-stu-id="e2810-110">A pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that is filled in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2810-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2810-111">Return value</span></span>

<span data-ttu-id="e2810-112">Si la función **GetNetworkInfoFromBlob** se ejecuta correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e2810-112">If the **GetNetworkInfoFromBlob** function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e2810-113">Si la función no es correcta, el valor devuelto es un valor de NMERR que describe el error.</span><span class="sxs-lookup"><span data-stu-id="e2810-113">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2810-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2810-114">Remarks</span></span>

<span data-ttu-id="e2810-115">La información de red se almacena en la sección BLOB **NetworkInfo** de la categoría de **propietario** de BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="e2810-115">The network information is stored in the BLOB **NetworkInfo** section of the BLOB NPP **Owner** category.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2810-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2810-116">Requirements</span></span>



| <span data-ttu-id="e2810-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2810-117">Requirement</span></span> | <span data-ttu-id="e2810-118">Value</span><span class="sxs-lookup"><span data-stu-id="e2810-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2810-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2810-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e2810-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e2810-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e2810-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2810-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e2810-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e2810-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2810-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2810-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2810-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2810-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="e2810-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2810-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2810-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2810-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="e2810-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2810-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2810-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2810-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2810-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2810-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2810-130">SetNetworkInfoInBlob</span><span class="sxs-lookup"><span data-stu-id="e2810-130">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="e2810-131">GetBoolFromBlob</span><span class="sxs-lookup"><span data-stu-id="e2810-131">GetBoolFromBlob</span></span>](getboolfromblob.md)
</dt> <dt>

[<span data-ttu-id="e2810-132">GetClassIDFromBlob</span><span class="sxs-lookup"><span data-stu-id="e2810-132">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="e2810-133">GetDwordFromBlob</span><span class="sxs-lookup"><span data-stu-id="e2810-133">GetDwordFromBlob</span></span>](getdwordfromblob.md)
</dt> <dt>

[<span data-ttu-id="e2810-134">GetMacAddressFromBlob</span><span class="sxs-lookup"><span data-stu-id="e2810-134">GetMacAddressFromBlob</span></span>](getmacaddressfromblob.md)
</dt> <dt>

[<span data-ttu-id="e2810-135">GetNPPAddressFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="e2810-135">GetNPPAddressFilterFromBlob</span></span>](getnppaddressfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="e2810-136">GetNPPPatternFilterFromBlob</span><span class="sxs-lookup"><span data-stu-id="e2810-136">GetNPPPatternFilterFromBlob</span></span>](getnpppatternfilterfromblob.md)
</dt> <dt>

[<span data-ttu-id="e2810-137">GetNPPTriggerFromBlob</span><span class="sxs-lookup"><span data-stu-id="e2810-137">GetNPPTriggerFromBlob</span></span>](getnpptriggerfromblob.md)
</dt> <dt>

[<span data-ttu-id="e2810-138">GetStringFromBlob</span><span class="sxs-lookup"><span data-stu-id="e2810-138">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="e2810-139">GetStringsFromBlob</span><span class="sxs-lookup"><span data-stu-id="e2810-139">GetStringsFromBlob</span></span>](getstringsfromblob.md)
</dt> </dl>

 

 




