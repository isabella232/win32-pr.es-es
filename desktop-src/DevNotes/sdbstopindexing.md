---
description: Deshabilita la creación y modificación de índices para la base de datos especificada.
ms.assetid: d079eae2-574e-4ac1-a0f9-11796e56a790
title: SdbStopIndexing función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStopIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3c9c6b34c265d611b57a3e73bb0c8fb1822fe752
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538649"
---
# <a name="sdbstopindexing-function"></a><span data-ttu-id="4b86f-103">SdbStopIndexing función)</span><span class="sxs-lookup"><span data-stu-id="4b86f-103">SdbStopIndexing function</span></span>

<span data-ttu-id="4b86f-104">Deshabilita la creación y modificación de índices para la base de datos especificada.</span><span class="sxs-lookup"><span data-stu-id="4b86f-104">Disables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b86f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b86f-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStopIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="4b86f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b86f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b86f-107">archivo *PDB* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b86f-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b86f-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="4b86f-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="4b86f-109">*iiWhich* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b86f-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b86f-110">Id. de índice.</span><span class="sxs-lookup"><span data-stu-id="4b86f-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b86f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b86f-111">Return value</span></span>

<span data-ttu-id="4b86f-112">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="4b86f-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b86f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b86f-113">Requirements</span></span>



| <span data-ttu-id="4b86f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b86f-114">Requirement</span></span> | <span data-ttu-id="4b86f-115">Value</span><span class="sxs-lookup"><span data-stu-id="4b86f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b86f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b86f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4b86f-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4b86f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4b86f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b86f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4b86f-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4b86f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4b86f-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b86f-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b86f-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b86f-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b86f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b86f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b86f-123">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="4b86f-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="4b86f-124">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="4b86f-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="4b86f-125">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="4b86f-125">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> </dl>

 

 




