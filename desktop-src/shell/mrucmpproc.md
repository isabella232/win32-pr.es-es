---
description: Se usa para determinar si un elemento está presente en una lista de elementos usados más recientemente (MRU).
title: Función de devolución de llamada MRUCMPPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: f95856f6508ad728a15b3df3d6f5eafa4f5bd2ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001338"
---
# <a name="mrucmpproc-callback-function"></a><span data-ttu-id="6e182-103">Función de devolución de llamada MRUCMPPROC</span><span class="sxs-lookup"><span data-stu-id="6e182-103">MRUCMPPROC callback function</span></span>

<span data-ttu-id="6e182-104">Se usa para determinar si un elemento está presente en una lista de elementos usados más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="6e182-104">Used to determine whether an item is present in a most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e182-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e182-105">Syntax</span></span>


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a><span data-ttu-id="6e182-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e182-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e182-107">*pString1*</span><span class="sxs-lookup"><span data-stu-id="6e182-107">*pString1*</span></span> 
</dt> <dd>

<span data-ttu-id="6e182-108">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="6e182-108">Type: **LPCTSTR**</span></span>

<span data-ttu-id="6e182-109">La primera cadena.</span><span class="sxs-lookup"><span data-stu-id="6e182-109">The first string.</span></span>

</dd> <dt>

<span data-ttu-id="6e182-110">*pString2*</span><span class="sxs-lookup"><span data-stu-id="6e182-110">*pString2*</span></span> 
</dt> <dd>

<span data-ttu-id="6e182-111">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="6e182-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="6e182-112">Segunda cadena que se va a comparar con la primera.</span><span class="sxs-lookup"><span data-stu-id="6e182-112">A second string to compare to the first.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e182-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e182-113">Return value</span></span>

<span data-ttu-id="6e182-114">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="6e182-114">Type: **int**</span></span>

<span data-ttu-id="6e182-115">Devuelve 0 si los elementos son idénticos, un valor distinto de cero en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6e182-115">Returns 0 if the items are identical, a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e182-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e182-116">Remarks</span></span>

<span data-ttu-id="6e182-117">Esta función se puede especificar opcionalmente para su uso en la estructura [**MRUINFO**](mruinfo.md) pasada a [**CreateMRUListW**](createmrulist.md).</span><span class="sxs-lookup"><span data-stu-id="6e182-117">This function can be optionally specified for use in the [**MRUINFO**](mruinfo.md) structure passed to [**CreateMRUListW**](createmrulist.md).</span></span> <span data-ttu-id="6e182-118">Esto resulta útil cuando la lista MRU se creó con la **marca \_ binaria MRU** .</span><span class="sxs-lookup"><span data-stu-id="6e182-118">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="6e182-119">Cuando no se especifica esta función, se usan las funciones de comparación de cadenas estándar.</span><span class="sxs-lookup"><span data-stu-id="6e182-119">When this function is not specified, standard string comparison functions are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e182-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e182-120">Requirements</span></span>



| <span data-ttu-id="6e182-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e182-121">Requirement</span></span> | <span data-ttu-id="6e182-122">Value</span><span class="sxs-lookup"><span data-stu-id="6e182-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="6e182-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e182-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6e182-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6e182-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="6e182-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e182-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6e182-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6e182-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="6e182-127">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="6e182-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6e182-128">**MRUCMPPROCW** (Unicode) y **MRUCMPPROCA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6e182-128">**MRUCMPPROCW** (Unicode) and **MRUCMPPROCA** (ANSI)</span></span><br/> |



 

 




