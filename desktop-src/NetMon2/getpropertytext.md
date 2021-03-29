---
description: La función GetPropertyText devuelve un puntero al texto de la propiedad.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: Función GetPropertyText (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360149"
---
# <a name="getpropertytext-function"></a><span data-ttu-id="0371a-103">GetPropertyText función)</span><span class="sxs-lookup"><span data-stu-id="0371a-103">GetPropertyText function</span></span>

<span data-ttu-id="0371a-104">La función **GetPropertyText** devuelve un puntero al texto de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0371a-104">The **GetPropertyText** function returns a pointer to the property text.</span></span>

## <a name="syntax"></a><span data-ttu-id="0371a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0371a-105">Syntax</span></span>


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="0371a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0371a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0371a-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0371a-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0371a-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="0371a-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="0371a-109">*lpPI* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0371a-109">*lpPI* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0371a-110">Puntero a una instancia de propiedad.</span><span class="sxs-lookup"><span data-stu-id="0371a-110">Pointer to a property instance.</span></span>

</dd> <dt>

<span data-ttu-id="0371a-111">*szBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0371a-111">*szBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0371a-112">Puntero a la cadena de texto de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0371a-112">Pointer to the property text string.</span></span>

</dd> <dt>

<span data-ttu-id="0371a-113">*BufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0371a-113">*BufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0371a-114">Tamaño del búfer de cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="0371a-114">Size of the text string buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0371a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0371a-115">Return value</span></span>

<span data-ttu-id="0371a-116">Si la función se realiza correctamente, el valor devuelto es un puntero al texto de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="0371a-116">If the function is successful, the return value is a pointer to the property text.</span></span>

<span data-ttu-id="0371a-117">Si la función no se realiza correctamente, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="0371a-117">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0371a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0371a-118">Remarks</span></span>

<span data-ttu-id="0371a-119">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetPropertyText** .</span><span class="sxs-lookup"><span data-stu-id="0371a-119">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyText** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0371a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0371a-120">Requirements</span></span>



| <span data-ttu-id="0371a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0371a-121">Requirement</span></span> | <span data-ttu-id="0371a-122">Value</span><span class="sxs-lookup"><span data-stu-id="0371a-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0371a-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0371a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0371a-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0371a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0371a-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0371a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0371a-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0371a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0371a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0371a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0371a-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0371a-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0371a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0371a-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0371a-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0371a-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0371a-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0371a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0371a-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0371a-132"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




