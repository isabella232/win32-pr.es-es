---
description: La función GetProtocolStartOffsetHandle devuelve el desplazamiento de fotogramas de un protocolo determinado.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: Función GetProtocolStartOffsetHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666275"
---
# <a name="getprotocolstartoffsethandle-function"></a><span data-ttu-id="2288f-103">GetProtocolStartOffsetHandle función)</span><span class="sxs-lookup"><span data-stu-id="2288f-103">GetProtocolStartOffsetHandle function</span></span>

<span data-ttu-id="2288f-104">La función **GetProtocolStartOffsetHandle** devuelve el desplazamiento de fotogramas de un protocolo determinado.</span><span class="sxs-lookup"><span data-stu-id="2288f-104">The **GetProtocolStartOffsetHandle** function returns the frame offset of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="2288f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2288f-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="2288f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2288f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2288f-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2288f-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2288f-108">Identificador de un marco.</span><span class="sxs-lookup"><span data-stu-id="2288f-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="2288f-109">*hProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2288f-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2288f-110">Identificador de un protocolo.</span><span class="sxs-lookup"><span data-stu-id="2288f-110">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2288f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2288f-111">Return value</span></span>

<span data-ttu-id="2288f-112">Si la función es correcta, el valor devuelto es el desplazamiento del marco medido en bytes.</span><span class="sxs-lookup"><span data-stu-id="2288f-112">If the function is successful, the return value is the offset of the frame   measured in bytes.</span></span>

<span data-ttu-id="2288f-113">Si la función no es correcta, el valor devuelto es uno (1).</span><span class="sxs-lookup"><span data-stu-id="2288f-113">If the function is unsuccessful, the return value is one (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="2288f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2288f-114">Remarks</span></span>

<span data-ttu-id="2288f-115">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetProtocolStartOffsetHandle** .</span><span class="sxs-lookup"><span data-stu-id="2288f-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolStartOffsetHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2288f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2288f-116">Requirements</span></span>



| <span data-ttu-id="2288f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2288f-117">Requirement</span></span> | <span data-ttu-id="2288f-118">Value</span><span class="sxs-lookup"><span data-stu-id="2288f-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2288f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2288f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2288f-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2288f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2288f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2288f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2288f-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2288f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2288f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2288f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2288f-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2288f-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2288f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2288f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="2288f-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2288f-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2288f-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2288f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2288f-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2288f-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




