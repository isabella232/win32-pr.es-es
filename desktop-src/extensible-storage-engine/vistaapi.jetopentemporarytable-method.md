---
description: 'Más información sobre: VistaApi. JetOpenTemporaryTable (método)'
title: Método VistaApi. JetOpenTemporaryTable (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOpenTemporaryTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetopentemporarytable(v=EXCHG.10)
ms:contentKeyID: 55104291
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a261494cf8b12039371c445a4cf2124f3ec1c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715671"
---
# <a name="vistaapijetopentemporarytable-method"></a><span data-ttu-id="b3cff-103">VistaApi. JetOpenTemporaryTable, método</span><span class="sxs-lookup"><span data-stu-id="b3cff-103">VistaApi.JetOpenTemporaryTable method</span></span>

<span data-ttu-id="b3cff-104">Crea una tabla temporal con un índice único.</span><span class="sxs-lookup"><span data-stu-id="b3cff-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="b3cff-105">Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="b3cff-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="b3cff-106">Sin embargo, las tablas temporales son mucho más rápidas que las normales debido a su naturaleza volátil.</span><span class="sxs-lookup"><span data-stu-id="b3cff-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="b3cff-107">También se pueden usar para ordenar de forma muy rápida y realizar una eliminación duplicada en conjuntos de registros cuando se tiene acceso a ellos de forma puramente secuencial.</span><span class="sxs-lookup"><span data-stu-id="b3cff-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="b3cff-108">Vea también [JetOpenTempTable (JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="b3cff-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span>

<span data-ttu-id="b3cff-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b3cff-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="b3cff-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b3cff-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b3cff-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3cff-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEVistaApi.JetOpenTemporaryTable(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a><span data-ttu-id="b3cff-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3cff-112">Parameters</span></span>

  - <span data-ttu-id="b3cff-113">sesid</span><span class="sxs-lookup"><span data-stu-id="b3cff-113">sesid</span></span>  
    <span data-ttu-id="b3cff-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b3cff-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b3cff-115">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b3cff-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b3cff-116">temporarytable</span><span class="sxs-lookup"><span data-stu-id="b3cff-116">temporarytable</span></span>  
    <span data-ttu-id="b3cff-117">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="b3cff-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="b3cff-118">Descripción de la tabla temporal que se va a crear en la entrada.</span><span class="sxs-lookup"><span data-stu-id="b3cff-118">Description of the temporary table to create on input.</span></span> <span data-ttu-id="b3cff-119">Después de una llamada correcta, la estructura contiene el identificador de la tabla temporal y las identificaciones de las columnas.</span><span class="sxs-lookup"><span data-stu-id="b3cff-119">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="b3cff-120">Use [JetCloseTable (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) para liberar la tabla temporal cuando termine.</span><span class="sxs-lookup"><span data-stu-id="b3cff-120">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3cff-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3cff-121">Remarks</span></span>

<span data-ttu-id="b3cff-122">Introducido en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3cff-122">Introduced in Windows Vista.</span></span> <span data-ttu-id="b3cff-123">Use [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md) para las versiones anteriores de esent.</span><span class="sxs-lookup"><span data-stu-id="b3cff-123">Use [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3cff-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3cff-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b3cff-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="b3cff-125">Reference</span></span>

[<span data-ttu-id="b3cff-126">Clase VistaApi</span><span class="sxs-lookup"><span data-stu-id="b3cff-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="b3cff-127">Miembros de VistaApi</span><span class="sxs-lookup"><span data-stu-id="b3cff-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="b3cff-128">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="b3cff-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
