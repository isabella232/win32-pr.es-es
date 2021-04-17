---
description: 'Más información acerca de: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105718579"
---
# <a name="jet_err"></a><span data-ttu-id="39c77-103">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="39c77-103">JET_ERR</span></span>


<span data-ttu-id="39c77-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="39c77-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_err"></a><span data-ttu-id="39c77-105">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="39c77-105">JET_ERR</span></span>

<span data-ttu-id="39c77-106">El tipo de datos **JET_ERR** contiene un [código de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="39c77-106">The **JET_ERR** data type contains an [Extensible Storage Engine error code](./extensible-storage-engine-error-codes.md).</span></span>

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a><span data-ttu-id="39c77-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="39c77-107">Data Types</span></span>

<span data-ttu-id="39c77-108">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="39c77-108">JET_ERR</span></span>

<span data-ttu-id="39c77-109">Un valor de cero (correspondiente a JET_errSuccess) indica que la llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="39c77-109">A zero value (corresponding to JET_errSuccess) indicates that the call succeeded.</span></span> <span data-ttu-id="39c77-110">Un valor positivo advierte de una condición no irrecuperable que se produjo durante una llamada correcta de otro modo.</span><span class="sxs-lookup"><span data-stu-id="39c77-110">A positive value warns of a non-fatal condition that occurred during an otherwise successful call.</span></span> <span data-ttu-id="39c77-111">Un valor negativo indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="39c77-111">A negative value indicates that the call failed.</span></span>

### <a name="remarks"></a><span data-ttu-id="39c77-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39c77-112">Remarks</span></span>

<span data-ttu-id="39c77-113">Para obtener información sobre cómo devolver los errores como valores HRESULT, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="39c77-113">For information about returning errors as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="39c77-114">Para obtener información acerca de las marcas para configurar la base de datos para controlar los errores, consulte [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="39c77-114">For information about flags for configuring the database to handle errors, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="39c77-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39c77-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39c77-116"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="39c77-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="39c77-117">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="39c77-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39c77-118"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="39c77-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="39c77-119">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="39c77-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39c77-120"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="39c77-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="39c77-121">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="39c77-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="39c77-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="39c77-122">See Also</span></span>

[<span data-ttu-id="39c77-123">Errores del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="39c77-123">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="39c77-124">Códigos de error del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="39c77-124">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="39c77-125">Parámetros de control de errores</span><span class="sxs-lookup"><span data-stu-id="39c77-125">Error Handling Parameters</span></span>](./error-handling-parameters.md)
