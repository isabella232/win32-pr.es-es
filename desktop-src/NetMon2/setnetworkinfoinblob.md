---
description: La función SetNetworkInfoInBlob rellena la estructura NETWORKINFO del BLOB.
ms.assetid: 1a511c26-2fa7-4fe4-a5a9-23188c59bc34
title: Función SetNetworkInfoInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNetworkInfoInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a0019bfaf802b5d4dc80d73e75affa3c50d95de1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678130"
---
# <a name="setnetworkinfoinblob-function"></a><span data-ttu-id="3dbae-103">SetNetworkInfoInBlob función)</span><span class="sxs-lookup"><span data-stu-id="3dbae-103">SetNetworkInfoInBlob function</span></span>

<span data-ttu-id="3dbae-104">La función **SetNetworkInfoInBlob** rellena la estructura **NETWORKINFO** del BLOB.</span><span class="sxs-lookup"><span data-stu-id="3dbae-104">The **SetNetworkInfoInBlob** function fills in the **NETWORKINFO** structure in the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dbae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3dbae-105">Syntax</span></span>


```C++
DWORD SetNetworkInfoInBlob(
  _In_ HBLOB         hBlob,
  _In_ LPNETWORKINFO lpNetworkInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3dbae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3dbae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dbae-107">*hBlob* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3dbae-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbae-108">Identificador de un BLOB.</span><span class="sxs-lookup"><span data-stu-id="3dbae-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="3dbae-109">*lpNetworkInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3dbae-109">*lpNetworkInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbae-110">Puntero a la estructura [NETWORKINFO](networkinfo.md) asignada por el usuario que la función rellena.</span><span class="sxs-lookup"><span data-stu-id="3dbae-110">Pointer to the user-allocated [NETWORKINFO](networkinfo.md) structure that the function fills in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dbae-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3dbae-111">Return value</span></span>

<span data-ttu-id="3dbae-112">Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3dbae-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3dbae-113">Si la función no es correcta, el valor devuelto es un valor de NMERR que indica el error.</span><span class="sxs-lookup"><span data-stu-id="3dbae-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dbae-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dbae-114">Requirements</span></span>



| <span data-ttu-id="3dbae-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dbae-115">Requirement</span></span> | <span data-ttu-id="3dbae-116">Value</span><span class="sxs-lookup"><span data-stu-id="3dbae-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dbae-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dbae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3dbae-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3dbae-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3dbae-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dbae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3dbae-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="3dbae-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3dbae-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3dbae-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dbae-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dbae-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3dbae-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3dbae-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3dbae-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dbae-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3dbae-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3dbae-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dbae-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dbae-126"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dbae-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3dbae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dbae-128">GetNetworkInfoFromBlob</span><span class="sxs-lookup"><span data-stu-id="3dbae-128">GetNetworkInfoFromBlob</span></span>](getnetworkinfofromblob.md)
</dt> <dt>

[<span data-ttu-id="3dbae-129">SetBoolInBlob</span><span class="sxs-lookup"><span data-stu-id="3dbae-129">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="3dbae-130">SetClassIDInBlob</span><span class="sxs-lookup"><span data-stu-id="3dbae-130">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="3dbae-131">SetDwordInBlob</span><span class="sxs-lookup"><span data-stu-id="3dbae-131">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="3dbae-132">SetMacAddressInBlob</span><span class="sxs-lookup"><span data-stu-id="3dbae-132">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="3dbae-133">SetNPPAddressFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="3dbae-133">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="3dbae-134">SetNPPPatternFilterInBlob</span><span class="sxs-lookup"><span data-stu-id="3dbae-134">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="3dbae-135">SetNPPTriggerInBlob</span><span class="sxs-lookup"><span data-stu-id="3dbae-135">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="3dbae-136">SetStringInBlob</span><span class="sxs-lookup"><span data-stu-id="3dbae-136">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




