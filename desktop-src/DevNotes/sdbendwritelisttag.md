---
description: Finaliza las operaciones de escritura para la lista especificada.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: SdbEndWriteListTag función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666157"
---
# <a name="sdbendwritelisttag-function"></a><span data-ttu-id="7b513-103">SdbEndWriteListTag función)</span><span class="sxs-lookup"><span data-stu-id="7b513-103">SdbEndWriteListTag function</span></span>

<span data-ttu-id="7b513-104">Finaliza las operaciones de escritura para la lista especificada.</span><span class="sxs-lookup"><span data-stu-id="7b513-104">Ends the write operations for the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b513-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b513-105">Syntax</span></span>


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a><span data-ttu-id="7b513-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b513-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b513-107">archivo *PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7b513-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b513-108">Identificador de la base de datos de correcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="7b513-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="7b513-109">*tiList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7b513-109">*tiList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b513-110">El [**TAGID**](tagid.md) de la lista</span><span class="sxs-lookup"><span data-stu-id="7b513-110">The [**TAGID**](tagid.md) of the list</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b513-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b513-111">Return value</span></span>

<span data-ttu-id="7b513-112">La función devuelve **true** si se ejecuta correctamente o **false** en caso de error.</span><span class="sxs-lookup"><span data-stu-id="7b513-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b513-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b513-113">Remarks</span></span>

<span data-ttu-id="7b513-114">Llame a esta función después de escribir todas las entradas de la lista; marcará el final de la lista.</span><span class="sxs-lookup"><span data-stu-id="7b513-114">Call this function after writing all list entries; it will mark the end of the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b513-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b513-115">Requirements</span></span>



| <span data-ttu-id="7b513-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b513-116">Requirement</span></span> | <span data-ttu-id="7b513-117">Value</span><span class="sxs-lookup"><span data-stu-id="7b513-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b513-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b513-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7b513-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7b513-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7b513-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7b513-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7b513-121">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b513-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7b513-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b513-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b513-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b513-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b513-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b513-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b513-125">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="7b513-125">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="7b513-126">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="7b513-126">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="7b513-127">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="7b513-127">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




