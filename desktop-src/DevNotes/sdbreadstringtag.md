---
Description: Recupera la cadena para el TAGID especificado.
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: SdbReadStringTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3f368d66e0fbc144a46683a04655cd7f650c3bce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997013"
---
# <a name="sdbreadstringtag-function"></a><span data-ttu-id="3b6d0-103">SdbReadStringTag función)</span><span class="sxs-lookup"><span data-stu-id="3b6d0-103">SdbReadStringTag function</span></span>

<span data-ttu-id="3b6d0-104">Recupera la cadena para el **TAGID** especificado.</span><span class="sxs-lookup"><span data-stu-id="3b6d0-104">Retrieves the string for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b6d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b6d0-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="3b6d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3b6d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b6d0-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b6d0-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6d0-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="3b6d0-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="3b6d0-109">*tiWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b6d0-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6d0-110">**TAGID** que corresponde a los datos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="3b6d0-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="3b6d0-111">*pwszBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="3b6d0-111">*pwszBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6d0-112">Búfer que recibe la cadena.</span><span class="sxs-lookup"><span data-stu-id="3b6d0-112">The buffer that receives the string.</span></span> <span data-ttu-id="3b6d0-113">Este parámetro no puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="3b6d0-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3b6d0-114">*cchBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3b6d0-114">*cchBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6d0-115">Tamaño del búfer de *pwszBuffer* , en caracteres.</span><span class="sxs-lookup"><span data-stu-id="3b6d0-115">The size of the *pwszBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b6d0-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3b6d0-116">Return value</span></span>

<span data-ttu-id="3b6d0-117">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="3b6d0-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b6d0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b6d0-118">Requirements</span></span>



| <span data-ttu-id="3b6d0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b6d0-119">Requirement</span></span> | <span data-ttu-id="3b6d0-120">Value</span><span class="sxs-lookup"><span data-stu-id="3b6d0-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b6d0-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b6d0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3b6d0-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3b6d0-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3b6d0-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b6d0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3b6d0-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b6d0-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3b6d0-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b6d0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b6d0-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b6d0-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b6d0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b6d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b6d0-128">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="3b6d0-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="3b6d0-129">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="3b6d0-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="3b6d0-130">**SdbReadBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="3b6d0-130">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
</dt> <dt>

[<span data-ttu-id="3b6d0-131">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3b6d0-131">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> </dl>

 

 




