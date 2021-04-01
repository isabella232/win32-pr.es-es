---
description: Busca la siguiente coincidencia de etiqueta en el elemento primario especificado y devuelve el TAGID de la coincidencia.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: SdbFindNextTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907112"
---
# <a name="sdbfindnexttag-function"></a><span data-ttu-id="91ea9-103">SdbFindNextTag función)</span><span class="sxs-lookup"><span data-stu-id="91ea9-103">SdbFindNextTag function</span></span>

<span data-ttu-id="91ea9-104">Busca la siguiente coincidencia de etiqueta en el elemento primario especificado y devuelve el **TAGID** de la coincidencia.</span><span class="sxs-lookup"><span data-stu-id="91ea9-104">Searches for the next TAG match within the specified parent and returns the **TAGID** of the match.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ea9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91ea9-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="91ea9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91ea9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91ea9-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91ea9-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91ea9-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="91ea9-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="91ea9-109">*tiParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91ea9-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91ea9-110">El **TAGID** del inicio de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="91ea9-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="91ea9-111">Este parámetro puede ser **la \_ raíz de TAGID** o la **lista de \_ tipos \_ de etiqueta**.</span><span class="sxs-lookup"><span data-stu-id="91ea9-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="91ea9-112">*tiPrev* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="91ea9-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91ea9-113">El **TAGID** de la coincidencia anterior.</span><span class="sxs-lookup"><span data-stu-id="91ea9-113">The **TAGID** of the previous match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91ea9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91ea9-114">Return value</span></span>

<span data-ttu-id="91ea9-115">**TAGID** de la coincidencia.</span><span class="sxs-lookup"><span data-stu-id="91ea9-115">The **TAGID** of the match.</span></span>

## <a name="remarks"></a><span data-ttu-id="91ea9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91ea9-116">Remarks</span></span>

<span data-ttu-id="91ea9-117">Antes de llamar a esta función, llame a la función [**SdbFindFirstTag**](sdbfindfirsttag.md) .</span><span class="sxs-lookup"><span data-stu-id="91ea9-117">Before calling this function, call the [**SdbFindFirstTag**](sdbfindfirsttag.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="91ea9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91ea9-118">Requirements</span></span>



| <span data-ttu-id="91ea9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="91ea9-119">Requirement</span></span> | <span data-ttu-id="91ea9-120">Value</span><span class="sxs-lookup"><span data-stu-id="91ea9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91ea9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91ea9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="91ea9-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="91ea9-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="91ea9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91ea9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="91ea9-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="91ea9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="91ea9-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="91ea9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91ea9-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91ea9-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91ea9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="91ea9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91ea9-128">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="91ea9-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="91ea9-129">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="91ea9-129">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




