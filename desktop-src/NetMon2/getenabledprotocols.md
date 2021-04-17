---
description: La función GetEnabledProtocols devuelve una tabla de todos los protocolos que están marcados como habilitados.
ms.assetid: 11feac64-c770-47b2-a740-fc372e97b8ed
title: Función GetEnabledProtocols (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetEnabledProtocols
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 284d6c87bf5a3b26d6c3f379a710966be21006d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652367"
---
# <a name="getenabledprotocols-function"></a><span data-ttu-id="76dc6-103">GetEnabledProtocols función)</span><span class="sxs-lookup"><span data-stu-id="76dc6-103">GetEnabledProtocols function</span></span>

<span data-ttu-id="76dc6-104">La función **GetEnabledProtocols** devuelve una tabla de todos los protocolos que están marcados como habilitados.</span><span class="sxs-lookup"><span data-stu-id="76dc6-104">The **GetEnabledProtocols** function returns a table of all protocols that are marked Enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="76dc6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76dc6-105">Syntax</span></span>


```C++
LPPROTOCOLTABLE WINAPI GetEnabledProtocols(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="76dc6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76dc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76dc6-107">*hCapture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="76dc6-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76dc6-108">Identificador de la captura.</span><span class="sxs-lookup"><span data-stu-id="76dc6-108">Handle to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76dc6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76dc6-109">Return value</span></span>

<span data-ttu-id="76dc6-110">Si la función se realiza correctamente, el valor devuelto es un puntero a una estructura [PROTOCOLTABLE](protocoltable.md) que enumera todos los protocolos habilitados en la captura.</span><span class="sxs-lookup"><span data-stu-id="76dc6-110">If the function is successful, the return value is a pointer to a [PROTOCOLTABLE](protocoltable.md) structure that lists all the enabled protocols in the capture.</span></span>

<span data-ttu-id="76dc6-111">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="76dc6-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="76dc6-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76dc6-112">Remarks</span></span>

<span data-ttu-id="76dc6-113">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetEnabledProtocols** .</span><span class="sxs-lookup"><span data-stu-id="76dc6-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetEnabledProtocols** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="76dc6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76dc6-114">Requirements</span></span>



| <span data-ttu-id="76dc6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="76dc6-115">Requirement</span></span> | <span data-ttu-id="76dc6-116">Value</span><span class="sxs-lookup"><span data-stu-id="76dc6-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76dc6-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76dc6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="76dc6-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="76dc6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="76dc6-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="76dc6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="76dc6-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="76dc6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="76dc6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="76dc6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="76dc6-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="76dc6-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="76dc6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="76dc6-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="76dc6-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76dc6-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="76dc6-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="76dc6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76dc6-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76dc6-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76dc6-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="76dc6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76dc6-128">PROTOCOLTABLE</span><span class="sxs-lookup"><span data-stu-id="76dc6-128">PROTOCOLTABLE</span></span>](protocoltable.md)
</dt> </dl>

 

 




