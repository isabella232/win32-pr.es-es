---
description: La función GetFrameStoredLength devuelve la longitud del marco.
ms.assetid: 7ac0e528-a45a-4c36-a99d-647347bdd143
title: Función GetFrameStoredLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameStoredLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e48f1d357645a9f50a85da4aba79d72baba4e4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678184"
---
# <a name="getframestoredlength-function"></a><span data-ttu-id="f6955-103">GetFrameStoredLength función)</span><span class="sxs-lookup"><span data-stu-id="f6955-103">GetFrameStoredLength function</span></span>

<span data-ttu-id="f6955-104">La función **GetFrameStoredLength** devuelve la longitud del marco.</span><span class="sxs-lookup"><span data-stu-id="f6955-104">The **GetFrameStoredLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6955-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6955-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameStoredLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="f6955-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6955-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6955-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f6955-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6955-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="f6955-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6955-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6955-109">Return value</span></span>

<span data-ttu-id="f6955-110">Si la función se realiza correctamente, el valor devuelto es la longitud del marco tal como está almacenado.</span><span class="sxs-lookup"><span data-stu-id="f6955-110">If the function is successful, the return value is the length of the frame as stored.</span></span>

<span data-ttu-id="f6955-111">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="f6955-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6955-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6955-112">Remarks</span></span>

<span data-ttu-id="f6955-113">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameStoredLength** .</span><span class="sxs-lookup"><span data-stu-id="f6955-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameStoredLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6955-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6955-114">Requirements</span></span>



| <span data-ttu-id="f6955-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6955-115">Requirement</span></span> | <span data-ttu-id="f6955-116">Value</span><span class="sxs-lookup"><span data-stu-id="f6955-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6955-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6955-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f6955-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f6955-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f6955-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6955-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f6955-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f6955-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f6955-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6955-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6955-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6955-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="f6955-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6955-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="f6955-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6955-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="f6955-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6955-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6955-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6955-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6955-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6955-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6955-128">GetFrameLength</span><span class="sxs-lookup"><span data-stu-id="f6955-128">GetFrameLength</span></span>](getframelength.md)
</dt> </dl>

 

 




