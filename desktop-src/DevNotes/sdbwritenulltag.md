---
description: Escribe una entrada nula en la base de datos especificada.
ms.assetid: 2a29389b-d4f6-4527-a429-c9459b095f2f
title: SdbWriteNULLTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteNULLTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 662d5c4db31f199df8b3b9f7368aba118ea6e8fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274901"
---
# <a name="sdbwritenulltag-function"></a><span data-ttu-id="ccb16-103">SdbWriteNULLTag función)</span><span class="sxs-lookup"><span data-stu-id="ccb16-103">SdbWriteNULLTag function</span></span>

<span data-ttu-id="ccb16-104">Escribe una entrada **nula** en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="ccb16-104">Writes a **NULL** entry to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccb16-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteNULLTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="ccb16-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ccb16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccb16-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ccb16-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccb16-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="ccb16-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="ccb16-109">*tTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ccb16-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccb16-110">ETIQUETA de la entrada.</span><span class="sxs-lookup"><span data-stu-id="ccb16-110">The TAG for the entry.</span></span> <span data-ttu-id="ccb16-111">Esta etiqueta debe ser de tipo **etiqueta \_ \_ null**.</span><span class="sxs-lookup"><span data-stu-id="ccb16-111">This TAG must be of type **TAG\_TYPE\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccb16-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ccb16-112">Return value</span></span>

<span data-ttu-id="ccb16-113">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="ccb16-113">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccb16-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccb16-114">Requirements</span></span>



| <span data-ttu-id="ccb16-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccb16-115">Requirement</span></span> | <span data-ttu-id="ccb16-116">Value</span><span class="sxs-lookup"><span data-stu-id="ccb16-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb16-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccb16-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb16-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ccb16-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ccb16-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccb16-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb16-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ccb16-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ccb16-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ccb16-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccb16-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccb16-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccb16-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccb16-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb16-124">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="ccb16-124">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="ccb16-125">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="ccb16-125">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="ccb16-126">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="ccb16-126">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="ccb16-127">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="ccb16-127">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




