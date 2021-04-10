---
description: 'Más información sobre: API. JetComputeStats (método)'
title: Método API. JetComputeStats
TOCTitle: 'JetComputeStats method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetComputeStats(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcomputestats(v=EXCHG.10)
ms:contentKeyID: 55100667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetComputeStats
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b102aca5971656232fae02684aeab30322d208b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275166"
---
# <a name="apijetcomputestats-method"></a><span data-ttu-id="fb879-103">Método API. JetComputeStats</span><span class="sxs-lookup"><span data-stu-id="fb879-103">Api.JetComputeStats method</span></span>

<span data-ttu-id="fb879-104">Recorre cada índice de una tabla para calcular exactamente el número de entradas de un índice y el número de claves distintas de un índice.</span><span class="sxs-lookup"><span data-stu-id="fb879-104">Walks each index of a table to exactly compute the number of entries in an index, and the number of distinct keys in an index.</span></span> <span data-ttu-id="fb879-105">Esta información, junto con el número de páginas de base de datos asignadas para un índice y la hora actual del cálculo, se almacena en los metadatos de índice de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fb879-105">This information, together with the number of database pages allocated for an index and the current time of the computation is stored in index metadata in the database.</span></span> <span data-ttu-id="fb879-106">Estos datos se pueden recuperar posteriormente con operaciones de información.</span><span class="sxs-lookup"><span data-stu-id="fb879-106">This data can be subsequently retrieved with information operations.</span></span>

<span data-ttu-id="fb879-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fb879-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fb879-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fb879-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fb879-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb879-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetComputeStats ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetComputeStats(sesid, tableid)
```

``` csharp
public static void JetComputeStats(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="fb879-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb879-110">Parameters</span></span>

  - <span data-ttu-id="fb879-111">sesid</span><span class="sxs-lookup"><span data-stu-id="fb879-111">sesid</span></span>  
    <span data-ttu-id="fb879-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fb879-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fb879-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="fb879-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fb879-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="fb879-114">tableid</span></span>  
    <span data-ttu-id="fb879-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fb879-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fb879-116">Tabla en la que se calcularán las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="fb879-116">The table that the statistics will be computed on.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb879-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb879-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fb879-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="fb879-118">Reference</span></span>

[<span data-ttu-id="fb879-119">Clase de API</span><span class="sxs-lookup"><span data-stu-id="fb879-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fb879-120">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="fb879-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fb879-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fb879-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
