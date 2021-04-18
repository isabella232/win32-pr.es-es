---
Description: Recupera los datos binarios para el TAGID especificado.
ms.assetid: b349f2af-2505-4efc-bd59-203f7666ce61
title: SdbReadBinaryTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 024b432c3210b98721a0cf3058bad0f765287fde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656533"
---
# <a name="sdbreadbinarytag-function"></a><span data-ttu-id="da6fc-103">SdbReadBinaryTag función)</span><span class="sxs-lookup"><span data-stu-id="da6fc-103">SdbReadBinaryTag function</span></span>

<span data-ttu-id="da6fc-104">Recupera los datos binarios para el **TAGID** especificado.</span><span class="sxs-lookup"><span data-stu-id="da6fc-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="da6fc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="da6fc-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadBinaryTag(
  _In_  PDB   pdb,
  _In_  TAGID tiWhich,
  _Out_ PBYTE pBuffer,
  _In_  DWORD dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="da6fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="da6fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da6fc-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da6fc-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da6fc-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="da6fc-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="da6fc-109">*tiWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da6fc-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da6fc-110">**TAGID** que corresponde a los datos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="da6fc-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="da6fc-111">*pBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="da6fc-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da6fc-112">Búfer que recibe los datos binarios.</span><span class="sxs-lookup"><span data-stu-id="da6fc-112">The buffer that receives the binary data.</span></span> <span data-ttu-id="da6fc-113">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="da6fc-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="da6fc-114">*dwBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="da6fc-114">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da6fc-115">Tamaño del búfer de *pBuffer* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="da6fc-115">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da6fc-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="da6fc-116">Return value</span></span>

<span data-ttu-id="da6fc-117">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="da6fc-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="da6fc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da6fc-118">Requirements</span></span>



| <span data-ttu-id="da6fc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="da6fc-119">Requirement</span></span> | <span data-ttu-id="da6fc-120">Value</span><span class="sxs-lookup"><span data-stu-id="da6fc-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da6fc-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da6fc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="da6fc-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="da6fc-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="da6fc-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da6fc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="da6fc-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="da6fc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="da6fc-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="da6fc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da6fc-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da6fc-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da6fc-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="da6fc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da6fc-128">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="da6fc-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="da6fc-129">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="da6fc-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="da6fc-130">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="da6fc-130">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="da6fc-131">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="da6fc-131">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




