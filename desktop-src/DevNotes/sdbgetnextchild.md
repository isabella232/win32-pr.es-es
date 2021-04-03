---
description: Busca la siguiente etiqueta secundaria dentro del elemento primario especificado y devuelve el TAGID del siguiente elemento secundario.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: SdbGetNextChild función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907190"
---
# <a name="sdbgetnextchild-function"></a><span data-ttu-id="5c42e-103">SdbGetNextChild función)</span><span class="sxs-lookup"><span data-stu-id="5c42e-103">SdbGetNextChild function</span></span>

<span data-ttu-id="5c42e-104">Busca la siguiente etiqueta secundaria dentro del elemento primario especificado y devuelve el **TAGID** del siguiente elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="5c42e-104">Searches for the next child TAG within the specified parent and returns the **TAGID** of the next child.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c42e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c42e-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="5c42e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c42e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c42e-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5c42e-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c42e-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="5c42e-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="5c42e-109">*tiParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5c42e-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c42e-110">El **TAGID** del inicio de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5c42e-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="5c42e-111">Este parámetro puede ser **la \_ raíz de TAGID** o la **lista de \_ tipos \_ de etiqueta**.</span><span class="sxs-lookup"><span data-stu-id="5c42e-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="5c42e-112">*tiPrev* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5c42e-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c42e-113">**TAGID** del elemento secundario anterior.</span><span class="sxs-lookup"><span data-stu-id="5c42e-113">The **TAGID** of the previous child.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c42e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c42e-114">Return value</span></span>

<span data-ttu-id="5c42e-115">**TagID** del elemento secundario o **TagID \_ null** si no se encuentra ningún elemento secundario.</span><span class="sxs-lookup"><span data-stu-id="5c42e-115">The **TAGID** of the child or **TAGID\_NULL** if no child is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c42e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c42e-116">Remarks</span></span>

<span data-ttu-id="5c42e-117">Antes de llamar a esta función, llame a la función [**SdbGetFirstChild**](sdbgetfirstchild.md) .</span><span class="sxs-lookup"><span data-stu-id="5c42e-117">Before calling this function, call the [**SdbGetFirstChild**](sdbgetfirstchild.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c42e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c42e-118">Requirements</span></span>



| <span data-ttu-id="5c42e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c42e-119">Requirement</span></span> | <span data-ttu-id="5c42e-120">Value</span><span class="sxs-lookup"><span data-stu-id="5c42e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c42e-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c42e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5c42e-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5c42e-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5c42e-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c42e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5c42e-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c42e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5c42e-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c42e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c42e-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c42e-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c42e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c42e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c42e-128">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="5c42e-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="5c42e-129">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="5c42e-129">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="5c42e-130">**SdbGetFirstChild**</span><span class="sxs-lookup"><span data-stu-id="5c42e-130">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
</dt> </dl>

 

 




