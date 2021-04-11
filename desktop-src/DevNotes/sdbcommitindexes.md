---
description: Confirma los índices recién creados en la base de datos especificada.
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: SdbCommitIndexes función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0709a913dc78cefdf405a0a3bd29030801941c37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152886"
---
# <a name="sdbcommitindexes-function"></a><span data-ttu-id="64535-103">SdbCommitIndexes función)</span><span class="sxs-lookup"><span data-stu-id="64535-103">SdbCommitIndexes function</span></span>

<span data-ttu-id="64535-104">Confirma los índices recién creados en la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="64535-104">Commits newly created indexes to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="64535-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="64535-105">Syntax</span></span>


```C++
BOOL WINAPI SdbCommitIndexes(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="64535-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="64535-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64535-107">archivo *PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="64535-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="64535-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="64535-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64535-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="64535-109">Return value</span></span>

<span data-ttu-id="64535-110">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="64535-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="64535-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64535-111">Requirements</span></span>



| <span data-ttu-id="64535-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="64535-112">Requirement</span></span> | <span data-ttu-id="64535-113">Value</span><span class="sxs-lookup"><span data-stu-id="64535-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64535-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64535-114">Minimum supported client</span></span><br/> | <span data-ttu-id="64535-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="64535-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="64535-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="64535-116">Minimum supported server</span></span><br/> | <span data-ttu-id="64535-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="64535-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="64535-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="64535-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64535-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64535-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64535-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="64535-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64535-121">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="64535-121">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="64535-122">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="64535-122">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="64535-123">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="64535-123">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




