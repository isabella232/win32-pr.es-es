---
description: Declara un nuevo índice en la base de datos especificada.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: SdbDeclareIndex función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666195"
---
# <a name="sdbdeclareindex-function"></a><span data-ttu-id="531c4-103">SdbDeclareIndex función)</span><span class="sxs-lookup"><span data-stu-id="531c4-103">SdbDeclareIndex function</span></span>

<span data-ttu-id="531c4-104">Declara un nuevo índice en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="531c4-104">Declares a new index in the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="531c4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="531c4-105">Syntax</span></span>


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a><span data-ttu-id="531c4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="531c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="531c4-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="531c4-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="531c4-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="531c4-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="531c4-109">*tWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="531c4-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="531c4-110">Este parámetro debe ser **una \_ \_ lista de tipo de etiqueta**.</span><span class="sxs-lookup"><span data-stu-id="531c4-110">This parameter must be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="531c4-111">*tKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="531c4-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="531c4-112">ETIQUETA que especifica el tipo que se va a usar como clave.</span><span class="sxs-lookup"><span data-stu-id="531c4-112">The TAG that specifies the type to be used as the key.</span></span> <span data-ttu-id="531c4-113">Este parámetro no puede ser una **\_ \_ lista de tipo de etiqueta**.</span><span class="sxs-lookup"><span data-stu-id="531c4-113">This parameter cannot be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="531c4-114">*dwEntries* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="531c4-114">*dwEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="531c4-115">Número de entradas que se van a asignar en el índice.</span><span class="sxs-lookup"><span data-stu-id="531c4-115">The number of entries to allocate in the index.</span></span>

</dd> <dt>

<span data-ttu-id="531c4-116">*bUniqueKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="531c4-116">*bUniqueKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="531c4-117">Si este parámetro es **true**, el índice es un índice de clave única.</span><span class="sxs-lookup"><span data-stu-id="531c4-117">If this parameter is **TRUE**, the index is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="531c4-118">*piiIndex* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="531c4-118">*piiIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="531c4-119">**INDEXID** resultante del índice recién declarado.</span><span class="sxs-lookup"><span data-stu-id="531c4-119">The resulting **INDEXID** of the newly declared index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="531c4-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="531c4-120">Return value</span></span>

<span data-ttu-id="531c4-121">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="531c4-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="531c4-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="531c4-122">Remarks</span></span>

<span data-ttu-id="531c4-123">Llame a esta función antes de escribir etiquetas en el nuevo índice.</span><span class="sxs-lookup"><span data-stu-id="531c4-123">Call this function before writing tags to the new index.</span></span>

## <a name="requirements"></a><span data-ttu-id="531c4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="531c4-124">Requirements</span></span>



| <span data-ttu-id="531c4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="531c4-125">Requirement</span></span> | <span data-ttu-id="531c4-126">Value</span><span class="sxs-lookup"><span data-stu-id="531c4-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="531c4-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="531c4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="531c4-128">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="531c4-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="531c4-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="531c4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="531c4-130">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="531c4-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="531c4-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="531c4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="531c4-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="531c4-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="531c4-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="531c4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="531c4-134">**INDEXID**</span><span class="sxs-lookup"><span data-stu-id="531c4-134">**INDEXID**</span></span>](indexid.md)
</dt> <dt>

[<span data-ttu-id="531c4-135">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="531c4-135">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="531c4-136">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="531c4-136">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="531c4-137">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="531c4-137">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




