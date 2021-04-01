---
title: Mensaje EM_SETEDITSTYLEEX (RichEdit. h)
description: Establece las marcas de estilo de edición extendida actual.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- EM_SETEDITSTYLEEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996927"
---
# <a name="em_seteditstyleex-message"></a><span data-ttu-id="e8a9a-104">\_Mensaje SETEDITSTYLEEX em</span><span class="sxs-lookup"><span data-stu-id="e8a9a-104">EM\_SETEDITSTYLEEX message</span></span>

<span data-ttu-id="e8a9a-105">Establece las marcas de estilo de edición extendida actual.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-105">Sets the current extended edit style flags.</span></span>


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a><span data-ttu-id="e8a9a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8a9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8a9a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8a9a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a9a-108">Especifica una o más marcas de estilo de edición extendida.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-108">Specifies one or more extended edit style flags.</span></span> <span data-ttu-id="e8a9a-109">Para obtener una lista de los valores posibles, vea [**em \_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).</span><span class="sxs-lookup"><span data-stu-id="e8a9a-109">For a list of possible values, see [**EM\_GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).</span></span>

</dd> <dt>

<span data-ttu-id="e8a9a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8a9a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a9a-111">Máscara formada por uno o varios de los valores de *wParam* .</span><span class="sxs-lookup"><span data-stu-id="e8a9a-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="e8a9a-112">Solo se establecerán o se borrarán los valores especificados en esta máscara.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="e8a9a-113">Esto permite establecer o borrar una sola marca sin leer los Estados actuales de la marca.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8a9a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8a9a-114">Return value</span></span>

<span data-ttu-id="e8a9a-115">El valor devuelto es el estado de las marcas de estilo de edición extendidas después de que la edición enriquecida haya intentado implementar los cambios de estilo de edición.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-115">The return value is the state of the extended edit style flags after rich edit has attempted to implement your edit style changes.</span></span> <span data-ttu-id="e8a9a-116">Las marcas de estilo de edición son un conjunto de marcas que indican el estilo de edición actual.</span><span class="sxs-lookup"><span data-stu-id="e8a9a-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8a9a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8a9a-117">Requirements</span></span>



| <span data-ttu-id="e8a9a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8a9a-118">Requirement</span></span> | <span data-ttu-id="e8a9a-119">Value</span><span class="sxs-lookup"><span data-stu-id="e8a9a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a9a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8a9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e8a9a-121">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8a9a-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e8a9a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8a9a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e8a9a-123">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8a9a-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e8a9a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8a9a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8a9a-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8a9a-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8a9a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8a9a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a9a-127">**\_GETEDITSTYLEEX em**</span><span class="sxs-lookup"><span data-stu-id="e8a9a-127">**EM\_GETEDITSTYLEEX**</span></span>](em-geteditstyleex.md)
</dt> </dl>

 

