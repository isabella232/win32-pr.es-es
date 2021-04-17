---
description: 'Más información acerca de: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105678855"
---
# <a name="jet_grbit"></a><span data-ttu-id="43fda-103">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="43fda-103">JET_GRBIT</span></span>


<span data-ttu-id="43fda-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="43fda-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_grbit"></a><span data-ttu-id="43fda-105">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="43fda-105">JET_GRBIT</span></span>

<span data-ttu-id="43fda-106">El tipo de datos **JET_GRBIT** es un grupo de bits que contiene constantes que son específicas de las funciones y estructuras en las que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="43fda-106">The **JET_GRBIT** data type is a group of bits that contain constants that are specific to the functions and structures in which it is used.</span></span>

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a><span data-ttu-id="43fda-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="43fda-107">Data Types</span></span>

<span data-ttu-id="43fda-108">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="43fda-108">JET_GRBIT</span></span>

<span data-ttu-id="43fda-109">En general, las constantes que se usan como valores para este tipo de datos reflejan el nombre del elemento de la API en el que se usan.</span><span class="sxs-lookup"><span data-stu-id="43fda-109">In general, the constants that are used as values for this data type reflect the name of the API element in which they are used.</span></span> <span data-ttu-id="43fda-110">Por ejemplo, todas las constantes pasadas a [JetRetrieveColumn](./jetretrievecolumn-function.md) comienzan con "JET_bitRetrieve".</span><span class="sxs-lookup"><span data-stu-id="43fda-110">For example, all constants passed to [JetRetrieveColumn](./jetretrievecolumn-function.md) begin with "JET_bitRetrieve".</span></span> <span data-ttu-id="43fda-111">Del mismo modo, todas las constantes pasadas a [JetSetColumn](./jetsetcolumn-function.md) comienzan con "JET_bitSet".</span><span class="sxs-lookup"><span data-stu-id="43fda-111">Similarly, all constants passed to [JetSetColumn](./jetsetcolumn-function.md) begin with "JET_bitSet".</span></span>

<span data-ttu-id="43fda-112">Un valor de cero hace que el parámetro se omita.</span><span class="sxs-lookup"><span data-stu-id="43fda-112">A value of zero causes the parameter to be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="43fda-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="43fda-113">Remarks</span></span>

<span data-ttu-id="43fda-114">Para obtener más información, vea la función o estructura específica.</span><span class="sxs-lookup"><span data-stu-id="43fda-114">For more information, see the specific function or structure.</span></span> <span data-ttu-id="43fda-115">Normalmente, las opciones se pasan como un conjunto de marcas que se pueden combinar.</span><span class="sxs-lookup"><span data-stu-id="43fda-115">The options are usually passed as a set of flags that can be combined.</span></span>

### <a name="requirements"></a><span data-ttu-id="43fda-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43fda-116">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43fda-117"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="43fda-117"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="43fda-118">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="43fda-118">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43fda-119"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="43fda-119"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="43fda-120">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="43fda-120">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43fda-121"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="43fda-121"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="43fda-122">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="43fda-122">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="43fda-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="43fda-123">See Also</span></span>

[<span data-ttu-id="43fda-124">JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="43fda-124">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="43fda-125">JetSetColumn</span><span class="sxs-lookup"><span data-stu-id="43fda-125">JetSetColumn</span></span>](./jetsetcolumn-function.md)
