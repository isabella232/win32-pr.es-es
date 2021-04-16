---
description: Escribe datos binarios en la base de datos especificada.
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: SdbWriteBinaryTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e79de8549eb4c0a0f1b8a914c59d21ccfb3bcf7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538644"
---
# <a name="sdbwritebinarytag-function"></a><span data-ttu-id="c678a-103">SdbWriteBinaryTag función)</span><span class="sxs-lookup"><span data-stu-id="c678a-103">SdbWriteBinaryTag function</span></span>

<span data-ttu-id="c678a-104">Escribe datos binarios en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="c678a-104">Writes binary data to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="c678a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c678a-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a><span data-ttu-id="c678a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c678a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c678a-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c678a-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c678a-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="c678a-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="c678a-109">*tTag* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c678a-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c678a-110">ETIQUETA de la entrada.</span><span class="sxs-lookup"><span data-stu-id="c678a-110">The TAG for the entry.</span></span> <span data-ttu-id="c678a-111">Esta etiqueta debe ser de tipo **etiqueta \_ \_ binaria**.</span><span class="sxs-lookup"><span data-stu-id="c678a-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="c678a-112">*pBuffer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c678a-112">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c678a-113">Búfer que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="c678a-113">The buffer that contains the data.</span></span> <span data-ttu-id="c678a-114">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="c678a-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c678a-115">*dwSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c678a-115">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c678a-116">Tamaño del búfer de *pBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="c678a-116">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c678a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c678a-117">Return value</span></span>

<span data-ttu-id="c678a-118">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="c678a-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c678a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c678a-119">Requirements</span></span>



| <span data-ttu-id="c678a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c678a-120">Requirement</span></span> | <span data-ttu-id="c678a-121">Value</span><span class="sxs-lookup"><span data-stu-id="c678a-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c678a-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c678a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c678a-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c678a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c678a-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c678a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c678a-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c678a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c678a-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c678a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c678a-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c678a-127"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c678a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c678a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c678a-129">**SdbWriteBinaryTagFromFile**</span><span class="sxs-lookup"><span data-stu-id="c678a-129">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
</dt> <dt>

[<span data-ttu-id="c678a-130">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="c678a-130">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="c678a-131">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="c678a-131">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="c678a-132">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="c678a-132">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="c678a-133">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="c678a-133">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




