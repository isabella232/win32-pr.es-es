---
description: Identificador del índice al que se va a obtener acceso en una base de datos.
ms.assetid: 559e73bf-91c2-4dbf-a667-e5c0431aaffa
title: INDEXID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b6ef6b79dd19183f575930e9793a6ab2f1f5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153314"
---
# <a name="indexid"></a><span data-ttu-id="0e3c6-103">INDEXID</span><span class="sxs-lookup"><span data-stu-id="0e3c6-103">INDEXID</span></span>

<span data-ttu-id="0e3c6-104">Identificador del índice al que se va a obtener acceso en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="0e3c6-104">The identifier of the index to be accessed in a database.</span></span>


```C++
typedef DWORD INDEXID;
```



## <a name="remarks"></a><span data-ttu-id="0e3c6-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e3c6-105">Remarks</span></span>

<span data-ttu-id="0e3c6-106">Un **INDEXID** puede ser un valor entero que representa el índice o el valor siguiente:</span><span class="sxs-lookup"><span data-stu-id="0e3c6-106">An **INDEXID** can be an integer value that represents the index, or the following value:</span></span>

<dl> <dt>

<span data-ttu-id="0e3c6-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID \_ null ((INDEXID)-1)</span><span class="sxs-lookup"><span data-stu-id="0e3c6-107"><span id="INDEXID_NULL___INDEXID_-1_"></span><span id="indexid_null___indexid_-1_"></span>INDEXID\_NULL ((INDEXID)-1)</span></span>
</dt> <dd>

<span data-ttu-id="0e3c6-108">Un **INDEXID** no válido.</span><span class="sxs-lookup"><span data-stu-id="0e3c6-108">An invalid **INDEXID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e3c6-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e3c6-109">Requirements</span></span>



| <span data-ttu-id="0e3c6-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e3c6-110">Requirement</span></span> | <span data-ttu-id="0e3c6-111">Value</span><span class="sxs-lookup"><span data-stu-id="0e3c6-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0e3c6-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e3c6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0e3c6-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0e3c6-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0e3c6-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e3c6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0e3c6-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0e3c6-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e3c6-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e3c6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e3c6-117">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="0e3c6-117">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="0e3c6-118">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="0e3c6-118">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="0e3c6-119">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="0e3c6-119">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




