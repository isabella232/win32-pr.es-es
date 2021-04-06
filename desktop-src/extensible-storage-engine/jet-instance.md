---
description: 'Más información acerca de: JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e1fde3e01c8328d2fdaf6609c6772fda9cd1428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002513"
---
# <a name="jet_instance"></a><span data-ttu-id="4a87c-103">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4a87c-103">JET_INSTANCE</span></span>


<span data-ttu-id="4a87c-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4a87c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_instance"></a><span data-ttu-id="4a87c-105">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4a87c-105">JET_INSTANCE</span></span>

<span data-ttu-id="4a87c-106">El tipo de datos **JET_INSTANCE** contiene un identificador para la instancia de la base de datos que se va a usar para una llamada a la API de jet.</span><span class="sxs-lookup"><span data-stu-id="4a87c-106">The **JET_INSTANCE** data type contains a handle to the instance of the database to use for a call to the JET API.</span></span>

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a><span data-ttu-id="4a87c-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4a87c-107">Data Types</span></span>

<span data-ttu-id="4a87c-108">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="4a87c-108">JET_INSTANCE</span></span>

<span data-ttu-id="4a87c-109">Se puede utilizar **null** o [JET_instanceNil](./invalid-handle-constants.md) para indicar un identificador de instancia no válido.</span><span class="sxs-lookup"><span data-stu-id="4a87c-109">Either **NULL** or [JET_instanceNil](./invalid-handle-constants.md) can be used to indicate an invalid instance handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="4a87c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a87c-110">Remarks</span></span>

<span data-ttu-id="4a87c-111">Este identificador se obtiene cuando se crea una instancia de la base de datos mediante una llamada a las funciones [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)o [JetInit2](./jetinit2-function.md) .</span><span class="sxs-lookup"><span data-stu-id="4a87c-111">This handle is obtained when you create an instance of the database by calling the [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md), or [JetInit2](./jetinit2-function.md) functions.</span></span>

<span data-ttu-id="4a87c-112">**Windows XP:**  El uso explícito de instancias solo se admite en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="4a87c-112">**Windows XP:**  The explicit use of instances is only supported on Windows XP and later releases.</span></span>

<span data-ttu-id="4a87c-113">**Windows 2000:**  Solo se admite una instancia global por proceso.</span><span class="sxs-lookup"><span data-stu-id="4a87c-113">**Windows 2000:**  Only one global instance is supported per process.</span></span>

### <a name="requirements"></a><span data-ttu-id="4a87c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a87c-114">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a87c-115"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="4a87c-115"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="4a87c-116">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="4a87c-116">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a87c-117"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="4a87c-117"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="4a87c-118">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="4a87c-118">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a87c-119"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="4a87c-119"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="4a87c-120">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="4a87c-120">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="4a87c-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4a87c-121">See Also</span></span>

[<span data-ttu-id="4a87c-122">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="4a87c-122">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="4a87c-123">JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="4a87c-123">JetCreateInstance2</span></span>](./jetcreateinstance2-function.md)  
[<span data-ttu-id="4a87c-124">JetInit</span><span class="sxs-lookup"><span data-stu-id="4a87c-124">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="4a87c-125">JetInit2</span><span class="sxs-lookup"><span data-stu-id="4a87c-125">JetInit2</span></span>](./jetinit2-function.md)
