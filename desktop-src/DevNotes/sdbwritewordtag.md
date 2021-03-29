---
description: Escribe un valor de WORD en la base de datos especificada.
ms.assetid: 8f921e14-4a82-4d8e-83fa-beb78118ecb8
title: SdbWriteWORDTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75a5b3eb430901de36d5aca325f928aae266bc39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538638"
---
# <a name="sdbwritewordtag-function"></a><span data-ttu-id="69f62-103">SdbWriteWORDTag función)</span><span class="sxs-lookup"><span data-stu-id="69f62-103">SdbWriteWORDTag function</span></span>

<span data-ttu-id="69f62-104">Escribe un valor de **Word** en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="69f62-104">Writes a **WORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="69f62-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69f62-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteWORDTag(
  _In_ PDB  pdb,
  _In_ TAG  tTag,
  _In_ WORD wData
);
```



## <a name="parameters"></a><span data-ttu-id="69f62-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69f62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69f62-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69f62-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69f62-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="69f62-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="69f62-109">*tTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69f62-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69f62-110">ETIQUETA de la entrada.</span><span class="sxs-lookup"><span data-stu-id="69f62-110">The TAG for the entry.</span></span> <span data-ttu-id="69f62-111">Esta etiqueta debe ser de tipo **etiqueta \_ \_ palabra**.</span><span class="sxs-lookup"><span data-stu-id="69f62-111">This TAG must be of type **TAG\_TYPE\_WORD**.</span></span>

</dd> <dt>

<span data-ttu-id="69f62-112">*wData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="69f62-112">*wData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69f62-113">Valor.</span><span class="sxs-lookup"><span data-stu-id="69f62-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69f62-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69f62-114">Return value</span></span>

<span data-ttu-id="69f62-115">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="69f62-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="69f62-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69f62-116">Requirements</span></span>



| <span data-ttu-id="69f62-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="69f62-117">Requirement</span></span> | <span data-ttu-id="69f62-118">Value</span><span class="sxs-lookup"><span data-stu-id="69f62-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69f62-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69f62-119">Minimum supported client</span></span><br/> | <span data-ttu-id="69f62-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="69f62-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="69f62-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69f62-121">Minimum supported server</span></span><br/> | <span data-ttu-id="69f62-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="69f62-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="69f62-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="69f62-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69f62-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69f62-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69f62-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="69f62-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69f62-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="69f62-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="69f62-127">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="69f62-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="69f62-128">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="69f62-128">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="69f62-129">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="69f62-129">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> </dl>

 

 




