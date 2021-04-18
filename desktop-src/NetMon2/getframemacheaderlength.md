---
description: La función GetFrameMacHeaderLength devuelve la longitud, en bytes, del encabezado MAC del marco.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: Función GetFrameMacHeaderLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4d11a0efac2086884e984edae986720ef704cf81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652365"
---
# <a name="getframemacheaderlength-function"></a><span data-ttu-id="30f4d-103">GetFrameMacHeaderLength función)</span><span class="sxs-lookup"><span data-stu-id="30f4d-103">GetFrameMacHeaderLength function</span></span>

<span data-ttu-id="30f4d-104">La función **GetFrameMacHeaderLength** devuelve la longitud, en bytes, del encabezado Mac del marco.</span><span class="sxs-lookup"><span data-stu-id="30f4d-104">The **GetFrameMacHeaderLength** function returns the length, in bytes, of the MAC header of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f4d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30f4d-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="30f4d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30f4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f4d-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="30f4d-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30f4d-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="30f4d-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f4d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30f4d-109">Return value</span></span>

<span data-ttu-id="30f4d-110">Si la función se realiza correctamente, el valor devuelto es la longitud en bytes del encabezado MAC.</span><span class="sxs-lookup"><span data-stu-id="30f4d-110">If the function is successful, the return value is the length   in bytes   of the MAC header.</span></span>

<span data-ttu-id="30f4d-111">Si la función no se realiza correctamente o se encuentra un tipo de MAC desconocido, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="30f4d-111">If the function is not successful, or an unknown MAC type is encountered, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f4d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30f4d-112">Remarks</span></span>

<span data-ttu-id="30f4d-113">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameMacHeaderLength** .</span><span class="sxs-lookup"><span data-stu-id="30f4d-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacHeaderLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f4d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30f4d-114">Requirements</span></span>



| <span data-ttu-id="30f4d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="30f4d-115">Requirement</span></span> | <span data-ttu-id="30f4d-116">Value</span><span class="sxs-lookup"><span data-stu-id="30f4d-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="30f4d-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30f4d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="30f4d-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="30f4d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="30f4d-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30f4d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="30f4d-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="30f4d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="30f4d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30f4d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="30f4d-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f4d-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="30f4d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30f4d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="30f4d-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30f4d-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="30f4d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30f4d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30f4d-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30f4d-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




