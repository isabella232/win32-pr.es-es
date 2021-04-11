---
description: Escribe un valor DWORD en la base de datos especificada.
ms.assetid: 2ecbfcac-5bb1-4129-9501-79210672aa1b
title: SdbWriteDWORDTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5b549a91037aa308b5b88d0e3e2a51e153002bd5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274902"
---
# <a name="sdbwritedwordtag-function"></a><span data-ttu-id="076ca-103">SdbWriteDWORDTag función)</span><span class="sxs-lookup"><span data-stu-id="076ca-103">SdbWriteDWORDTag function</span></span>

<span data-ttu-id="076ca-104">Escribe un valor **DWORD** en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="076ca-104">Writes a **DWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="076ca-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="076ca-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteDWORDTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ DWORD dwData
);
```



## <a name="parameters"></a><span data-ttu-id="076ca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="076ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="076ca-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="076ca-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="076ca-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="076ca-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="076ca-109">*tTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="076ca-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="076ca-110">ETIQUETA de la entrada.</span><span class="sxs-lookup"><span data-stu-id="076ca-110">The TAG for the entry.</span></span> <span data-ttu-id="076ca-111">Esta etiqueta debe ser de tipo **etiqueta \_ \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="076ca-111">This TAG must be of type **TAG\_TYPE\_DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="076ca-112">*dwData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="076ca-112">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="076ca-113">Valor.</span><span class="sxs-lookup"><span data-stu-id="076ca-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="076ca-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="076ca-114">Return value</span></span>

<span data-ttu-id="076ca-115">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="076ca-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="076ca-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="076ca-116">Requirements</span></span>



| <span data-ttu-id="076ca-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="076ca-117">Requirement</span></span> | <span data-ttu-id="076ca-118">Value</span><span class="sxs-lookup"><span data-stu-id="076ca-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="076ca-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076ca-119">Minimum supported client</span></span><br/> | <span data-ttu-id="076ca-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="076ca-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="076ca-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076ca-121">Minimum supported server</span></span><br/> | <span data-ttu-id="076ca-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="076ca-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="076ca-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="076ca-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="076ca-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="076ca-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="076ca-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="076ca-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="076ca-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="076ca-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="076ca-127">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="076ca-127">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="076ca-128">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="076ca-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="076ca-129">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="076ca-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




