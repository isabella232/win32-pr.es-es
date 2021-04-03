---
description: Busca una coincidencia de etiqueta en el elemento primario especificado y devuelve el TAGID de la primera coincidencia.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: SdbFindFirstTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: dc8b752d536be83d90ded55474166d14521f0f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998045"
---
# <a name="sdbfindfirsttag-function"></a><span data-ttu-id="ae489-103">SdbFindFirstTag función)</span><span class="sxs-lookup"><span data-stu-id="ae489-103">SdbFindFirstTag function</span></span>

<span data-ttu-id="ae489-104">Busca una coincidencia de etiqueta en el elemento primario especificado y devuelve el **TAGID** de la primera coincidencia.</span><span class="sxs-lookup"><span data-stu-id="ae489-104">Searches for a TAG match within the specified parent and returns the **TAGID** of the first match.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae489-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae489-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
);
```



## <a name="parameters"></a><span data-ttu-id="ae489-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae489-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae489-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae489-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae489-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="ae489-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="ae489-109">*tiParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae489-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae489-110">El **TAGID** del inicio de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae489-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="ae489-111">Este parámetro puede ser **la \_ raíz de TAGID** o la **lista de \_ tipos \_ de etiqueta**.</span><span class="sxs-lookup"><span data-stu-id="ae489-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="ae489-112">*tTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ae489-112">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae489-113">ETIQUETA que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="ae489-113">The TAG to be matched.</span></span> <span data-ttu-id="ae489-114">Vea [etiqueta](tag.md) para obtener una lista de valores posibles.</span><span class="sxs-lookup"><span data-stu-id="ae489-114">See [TAG](tag.md) for a list of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae489-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae489-115">Return value</span></span>

<span data-ttu-id="ae489-116">**TAGID** de la primera coincidencia.</span><span class="sxs-lookup"><span data-stu-id="ae489-116">The **TAGID** of the first match.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae489-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae489-117">Requirements</span></span>



| <span data-ttu-id="ae489-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae489-118">Requirement</span></span> | <span data-ttu-id="ae489-119">Value</span><span class="sxs-lookup"><span data-stu-id="ae489-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae489-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae489-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae489-121">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ae489-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ae489-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae489-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae489-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ae489-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ae489-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae489-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae489-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae489-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae489-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae489-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae489-127">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="ae489-127">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="ae489-128">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="ae489-128">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




