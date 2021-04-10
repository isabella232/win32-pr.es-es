---
description: Recupera la etiqueta asociada al TAGID especificado.
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: SdbGetTagFromTagID función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d81dac026a9b6acc921586aaded54c8c90ad5bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153070"
---
# <a name="sdbgettagfromtagid-function"></a><span data-ttu-id="b5486-103">SdbGetTagFromTagID función)</span><span class="sxs-lookup"><span data-stu-id="b5486-103">SdbGetTagFromTagID function</span></span>

<span data-ttu-id="b5486-104">Recupera la etiqueta asociada al **TAGID** especificado.</span><span class="sxs-lookup"><span data-stu-id="b5486-104">Retrieves the TAG associated with the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5486-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5486-105">Syntax</span></span>


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="b5486-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5486-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5486-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5486-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5486-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="b5486-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="b5486-109">*tiWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5486-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5486-110">**TAGID** de la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="b5486-110">The **TAGID** for the TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5486-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5486-111">Return value</span></span>

<span data-ttu-id="b5486-112">La función devuelve la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="b5486-112">The function returns the TAG.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5486-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5486-113">Requirements</span></span>



| <span data-ttu-id="b5486-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5486-114">Requirement</span></span> | <span data-ttu-id="b5486-115">Value</span><span class="sxs-lookup"><span data-stu-id="b5486-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5486-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5486-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b5486-117">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b5486-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b5486-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5486-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b5486-119">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5486-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b5486-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5486-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5486-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5486-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5486-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5486-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5486-123">**ETIQUETA**</span><span class="sxs-lookup"><span data-stu-id="b5486-123">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="b5486-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="b5486-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




