---
description: Busca el primer registro DWORD en el índice especificado que cumpla los criterios especificados.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: SdbFindFirstDWORDIndexedTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538265"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a><span data-ttu-id="aa22f-103">SdbFindFirstDWORDIndexedTag función)</span><span class="sxs-lookup"><span data-stu-id="aa22f-103">SdbFindFirstDWORDIndexedTag function</span></span>

<span data-ttu-id="aa22f-104">Busca el primer registro **DWORD** en el índice especificado que cumpla los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="aa22f-104">Finds the first **DWORD** record in the specified index that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa22f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa22f-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a><span data-ttu-id="aa22f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa22f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa22f-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa22f-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa22f-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="aa22f-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="aa22f-109">*tWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa22f-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa22f-110">Tipo de índice.</span><span class="sxs-lookup"><span data-stu-id="aa22f-110">The index type.</span></span> <span data-ttu-id="aa22f-111">Vea [**etiqueta**](tag.md) para obtener una lista de valores.</span><span class="sxs-lookup"><span data-stu-id="aa22f-111">See [**TAG**](tag.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="aa22f-112">*tKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa22f-112">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa22f-113">El tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="aa22f-113">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="aa22f-114">*dwName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa22f-114">*dwName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa22f-115">Nombre de los datos que se van a buscar.</span><span class="sxs-lookup"><span data-stu-id="aa22f-115">The name of the data to be found.</span></span> <span data-ttu-id="aa22f-116">Este valor se convertirá en una clave.</span><span class="sxs-lookup"><span data-stu-id="aa22f-116">This value will be converted into a key.</span></span>

</dd> <dt>

<span data-ttu-id="aa22f-117">*pFindInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aa22f-117">*pFindInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa22f-118">Una estructura de [**\_ información de búsqueda**](find-info.md) que recibe el registro.</span><span class="sxs-lookup"><span data-stu-id="aa22f-118">A [**FIND\_INFO**](find-info.md) structure that receives the record.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa22f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa22f-119">Return value</span></span>

<span data-ttu-id="aa22f-120">**TAGID** de la primera coincidencia o **etiqueta \_ null** si no se encuentra ninguna coincidencia.</span><span class="sxs-lookup"><span data-stu-id="aa22f-120">The **TAGID** of the first match or **TAG\_NULL** if no match is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa22f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa22f-121">Requirements</span></span>



| <span data-ttu-id="aa22f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa22f-122">Requirement</span></span> | <span data-ttu-id="aa22f-123">Value</span><span class="sxs-lookup"><span data-stu-id="aa22f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa22f-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa22f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aa22f-125">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="aa22f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="aa22f-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa22f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aa22f-127">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa22f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="aa22f-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa22f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa22f-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa22f-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa22f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa22f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa22f-131">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="aa22f-131">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> </dl>

 

 




