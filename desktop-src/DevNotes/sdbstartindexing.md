---
description: Habilita la creación y modificación de índices para la base de datos especificada.
ms.assetid: f780034e-6963-423c-8ffa-9fbe98dca7e1
title: SdbStartIndexing función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStartIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e3324b4cb0d42ca33ee7c3234a1acc099adcb743
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152959"
---
# <a name="sdbstartindexing-function"></a><span data-ttu-id="db14b-103">SdbStartIndexing función)</span><span class="sxs-lookup"><span data-stu-id="db14b-103">SdbStartIndexing function</span></span>

<span data-ttu-id="db14b-104">Habilita la creación y modificación de índices para la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="db14b-104">Enables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="db14b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db14b-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStartIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="db14b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db14b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db14b-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="db14b-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db14b-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="db14b-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="db14b-109">*iiWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="db14b-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db14b-110">Id. de índice.</span><span class="sxs-lookup"><span data-stu-id="db14b-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db14b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db14b-111">Return value</span></span>

<span data-ttu-id="db14b-112">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="db14b-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="db14b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db14b-113">Requirements</span></span>



| <span data-ttu-id="db14b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="db14b-114">Requirement</span></span> | <span data-ttu-id="db14b-115">Value</span><span class="sxs-lookup"><span data-stu-id="db14b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db14b-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db14b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="db14b-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="db14b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="db14b-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="db14b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="db14b-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="db14b-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="db14b-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="db14b-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db14b-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db14b-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db14b-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="db14b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db14b-123">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="db14b-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="db14b-124">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="db14b-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="db14b-125">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="db14b-125">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




