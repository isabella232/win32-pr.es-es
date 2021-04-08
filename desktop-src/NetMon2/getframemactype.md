---
description: La función GetFrameMacType devuelve el tipo MAC del marco.
ms.assetid: 8d3da770-1392-4638-a267-32c2dae289b0
title: Función GetFrameMacType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b85accc64a6e29424e3f65d070bafcf29bb3ec0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000931"
---
# <a name="getframemactype-function"></a><span data-ttu-id="ead9f-103">GetFrameMacType función)</span><span class="sxs-lookup"><span data-stu-id="ead9f-103">GetFrameMacType function</span></span>

<span data-ttu-id="ead9f-104">La función **GetFrameMacType** devuelve el tipo Mac del marco.</span><span class="sxs-lookup"><span data-stu-id="ead9f-104">The **GetFrameMacType** function returns the MAC type of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead9f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ead9f-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacType(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="ead9f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ead9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ead9f-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ead9f-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ead9f-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="ead9f-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ead9f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ead9f-109">Return value</span></span>

<span data-ttu-id="ead9f-110">La función devuelve el tipo MAC del marco, que puede tener uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ead9f-110">The function returns the MAC type of the frame, which can have one of the following values.</span></span>

-   <span data-ttu-id="ead9f-111">tipo de MAC \_ \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="ead9f-111">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="ead9f-112">\_Ethernet de tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="ead9f-112">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="ead9f-113">\_TOKENRING de tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="ead9f-113">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="ead9f-114">\_FDDI de tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="ead9f-114">MAC\_TYPE\_FDDI</span></span>

## <a name="remarks"></a><span data-ttu-id="ead9f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ead9f-115">Remarks</span></span>

<span data-ttu-id="ead9f-116">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameMacType** .</span><span class="sxs-lookup"><span data-stu-id="ead9f-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ead9f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ead9f-117">Requirements</span></span>



| <span data-ttu-id="ead9f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ead9f-118">Requirement</span></span> | <span data-ttu-id="ead9f-119">Value</span><span class="sxs-lookup"><span data-stu-id="ead9f-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ead9f-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ead9f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ead9f-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ead9f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ead9f-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ead9f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ead9f-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ead9f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ead9f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ead9f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead9f-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ead9f-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ead9f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ead9f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="ead9f-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ead9f-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ead9f-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ead9f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ead9f-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ead9f-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




