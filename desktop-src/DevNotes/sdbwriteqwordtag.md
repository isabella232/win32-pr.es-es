---
description: Escribe un valor QWORD en la base de datos especificada.
ms.assetid: 8ce566ea-a941-45fa-b031-26c3144ca02c
title: SdbWriteQWORDTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58dcaad3487bb1f59a75dd6a671ecb43c9cf1751
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807219"
---
# <a name="sdbwriteqwordtag-function"></a><span data-ttu-id="883e0-103">SdbWriteQWORDTag función)</span><span class="sxs-lookup"><span data-stu-id="883e0-103">SdbWriteQWORDTag function</span></span>

<span data-ttu-id="883e0-104">Escribe un valor **QWord** en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="883e0-104">Writes a **QWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="883e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="883e0-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteQWORDTag(
  _In_ PDB       pdb,
  _In_ TAG       tTag,
  _In_ ULONGLONG qwData
);
```



## <a name="parameters"></a><span data-ttu-id="883e0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="883e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="883e0-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="883e0-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="883e0-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="883e0-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="883e0-109">*tTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="883e0-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="883e0-110">ETIQUETA de la entrada.</span><span class="sxs-lookup"><span data-stu-id="883e0-110">The TAG for the entry.</span></span> <span data-ttu-id="883e0-111">Esta etiqueta debe ser del tipo **de \_ etiqueta \_ QWord**.</span><span class="sxs-lookup"><span data-stu-id="883e0-111">This TAG must be of type **TAG\_TYPE\_QWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="883e0-112">*qwData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="883e0-112">*qwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="883e0-113">Valor.</span><span class="sxs-lookup"><span data-stu-id="883e0-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="883e0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="883e0-114">Return value</span></span>

<span data-ttu-id="883e0-115">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="883e0-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="883e0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="883e0-116">Requirements</span></span>



| <span data-ttu-id="883e0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="883e0-117">Requirement</span></span> | <span data-ttu-id="883e0-118">Value</span><span class="sxs-lookup"><span data-stu-id="883e0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="883e0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="883e0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="883e0-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="883e0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="883e0-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="883e0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="883e0-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="883e0-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="883e0-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="883e0-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="883e0-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="883e0-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="883e0-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="883e0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="883e0-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="883e0-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="883e0-127">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="883e0-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="883e0-128">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="883e0-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="883e0-129">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="883e0-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




