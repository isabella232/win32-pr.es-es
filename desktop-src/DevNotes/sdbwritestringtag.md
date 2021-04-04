---
description: Escribe una cadena en la base de datos especificada.
ms.assetid: 72c62d91-0c1c-4ff8-8829-1c3ec1fa8648
title: SdbWriteStringTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4ac588d99408d0d7f13bc0fd13d8abe8a6580e69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907109"
---
# <a name="sdbwritestringtag-function"></a><span data-ttu-id="b0725-103">SdbWriteStringTag función)</span><span class="sxs-lookup"><span data-stu-id="b0725-103">SdbWriteStringTag function</span></span>

<span data-ttu-id="b0725-104">Escribe una cadena en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="b0725-104">Writes a string to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0725-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0725-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteStringTag(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszData
);
```



## <a name="parameters"></a><span data-ttu-id="b0725-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0725-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0725-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0725-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0725-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="b0725-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="b0725-109">*tTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0725-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0725-110">ETIQUETA de la entrada.</span><span class="sxs-lookup"><span data-stu-id="b0725-110">The TAG for the entry.</span></span> <span data-ttu-id="b0725-111">Esta etiqueta debe ser de tipo **tag \_ Type \_ STRINGREF**.</span><span class="sxs-lookup"><span data-stu-id="b0725-111">This TAG must be of type **TAG\_TYPE\_STRINGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="b0725-112">*pwszData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b0725-112">*pwszData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0725-113">Cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="b0725-113">The null-terminated string.</span></span> <span data-ttu-id="b0725-114">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="b0725-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0725-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0725-115">Return value</span></span>

<span data-ttu-id="b0725-116">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="b0725-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0725-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0725-117">Requirements</span></span>



| <span data-ttu-id="b0725-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0725-118">Requirement</span></span> | <span data-ttu-id="b0725-119">Value</span><span class="sxs-lookup"><span data-stu-id="b0725-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0725-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0725-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b0725-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b0725-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b0725-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0725-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b0725-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0725-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b0725-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0725-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0725-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0725-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0725-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0725-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0725-127">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="b0725-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="b0725-128">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="b0725-128">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="b0725-129">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="b0725-129">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="b0725-130">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="b0725-130">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




