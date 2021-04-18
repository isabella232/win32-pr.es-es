---
description: 'Más información sobre: Windows8Api. JetOpenTemporaryTable2 (método)'
title: Método Windows8Api. JetOpenTemporaryTable2 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetOpenTemporaryTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetopentemporarytable2(v=EXCHG.10)
ms:contentKeyID: 55107829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetOpenTemporaryTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5ebb96af18e655c9f9304e2fe7a339663c0206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705861"
---
# <a name="windows8apijetopentemporarytable2-method"></a><span data-ttu-id="46dea-103">Windows8Api. JetOpenTemporaryTable2, método</span><span class="sxs-lookup"><span data-stu-id="46dea-103">Windows8Api.JetOpenTemporaryTable2 method</span></span>

<span data-ttu-id="46dea-104">Crea una tabla temporal con un índice único.</span><span class="sxs-lookup"><span data-stu-id="46dea-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="46dea-105">Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="46dea-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="46dea-106">Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil.</span><span class="sxs-lookup"><span data-stu-id="46dea-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="46dea-107">También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.</span><span class="sxs-lookup"><span data-stu-id="46dea-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="46dea-108">Vea también [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), "API. JetOpenTempTable2", [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="46dea-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="46dea-109">[JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="46dea-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="46dea-110">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="46dea-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="46dea-111">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="46dea-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="46dea-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46dea-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable2 ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEWindows8Api.JetOpenTemporaryTable2(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable2(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="46dea-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46dea-113">Parameters</span></span>

  - <span data-ttu-id="46dea-114">sesid</span><span class="sxs-lookup"><span data-stu-id="46dea-114">sesid</span></span>  
    <span data-ttu-id="46dea-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="46dea-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="46dea-116">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="46dea-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="46dea-117">temporarytable</span><span class="sxs-lookup"><span data-stu-id="46dea-117">temporarytable</span></span>  
    <span data-ttu-id="46dea-118">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="46dea-118">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="46dea-119">Descripción de la tabla temporal que se va a crear en la entrada.</span><span class="sxs-lookup"><span data-stu-id="46dea-119">Description of the temporary table to create on input.</span></span> <span data-ttu-id="46dea-120">Después de una llamada correcta, la estructura contiene el identificador de la tabla temporal y las identificaciones de las columnas.</span><span class="sxs-lookup"><span data-stu-id="46dea-120">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="46dea-121">Use [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) para liberar la tabla temporal cuando termine.</span><span class="sxs-lookup"><span data-stu-id="46dea-121">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="46dea-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46dea-122">Remarks</span></span>

<span data-ttu-id="46dea-123">Use [JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) para versiones anteriores de esent.</span><span class="sxs-lookup"><span data-stu-id="46dea-123">Use [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="46dea-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="46dea-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="46dea-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="46dea-125">Reference</span></span>

[<span data-ttu-id="46dea-126">Clase Windows8Api</span><span class="sxs-lookup"><span data-stu-id="46dea-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="46dea-127">Miembros de Windows8Api</span><span class="sxs-lookup"><span data-stu-id="46dea-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="46dea-128">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="46dea-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
