---
description: Crea una nueva etiqueta de lista para las operaciones de escritura.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: SdbBeginWriteListTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9dcf6bdd3798b18e08b796eb268f93dc4ec6bbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807711"
---
# <a name="sdbbeginwritelisttag-function"></a><span data-ttu-id="5e030-103">SdbBeginWriteListTag función)</span><span class="sxs-lookup"><span data-stu-id="5e030-103">SdbBeginWriteListTag function</span></span>

<span data-ttu-id="5e030-104">Crea una nueva etiqueta de lista para las operaciones de escritura.</span><span class="sxs-lookup"><span data-stu-id="5e030-104">Creates a new list TAG for write operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e030-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e030-105">Syntax</span></span>


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="5e030-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e030-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e030-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e030-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e030-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="5e030-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="5e030-109">*tTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e030-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e030-110">ETIQUETA para la nueva entrada.</span><span class="sxs-lookup"><span data-stu-id="5e030-110">The TAG for the new entry.</span></span> <span data-ttu-id="5e030-111">Este valor debe ser de tipo **tag \_ Type \_ List**.</span><span class="sxs-lookup"><span data-stu-id="5e030-111">This value must be of type **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e030-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e030-112">Return value</span></span>

<span data-ttu-id="5e030-113">La función devuelve el valor de [**TagID**](tagid.md) de la nueva lista en Success o **TagID \_ null** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="5e030-113">The function returns the [**TAGID**](tagid.md) of the new list on success or **TAGID\_NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e030-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e030-114">Requirements</span></span>



| <span data-ttu-id="5e030-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e030-115">Requirement</span></span> | <span data-ttu-id="5e030-116">Value</span><span class="sxs-lookup"><span data-stu-id="5e030-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e030-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e030-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5e030-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e030-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5e030-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e030-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5e030-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e030-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5e030-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e030-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e030-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e030-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e030-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e030-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e030-124">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="5e030-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="5e030-125">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="5e030-125">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> <dt>

[<span data-ttu-id="5e030-126">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="5e030-126">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="5e030-127">**ETIQUETA**</span><span class="sxs-lookup"><span data-stu-id="5e030-127">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="5e030-128">Tipos de etiquetas</span><span class="sxs-lookup"><span data-stu-id="5e030-128">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="5e030-129">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="5e030-129">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




