---
description: Más información sobre el método Windows8Api.JetOpenTemporaryTable2
title: Método Windows8Api.JetOpenTemporaryTable2 (Microsoft.Isam.Esent.Interop.Windows8)
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
- DllExport
api_location:
- Microsoft.Isam.Esent.Interop.dll
- esent.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb01792608ec542918f4bd8ff6ec06ef27091bb1
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691734"
---
# <a name="windows8apijetopentemporarytable2-method"></a><span data-ttu-id="5eaf3-103">Método Windows8Api.JetOpenTemporaryTable2</span><span class="sxs-lookup"><span data-stu-id="5eaf3-103">Windows8Api.JetOpenTemporaryTable2 method</span></span>

<span data-ttu-id="5eaf3-104">Crea una tabla temporal con un único índice.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="5eaf3-105">Una tabla temporal almacena y recupera registros como una tabla normal creada mediante JetCreateTableColumnIndex.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="5eaf3-106">Sin embargo, las tablas temporales son mucho más rápidas que las tablas normales debido a su naturaleza volátil.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="5eaf3-107">También se pueden usar para ordenar y realizar la eliminación de duplicados rápidamente en conjuntos de registros cuando se accede a ellos de una manera puramente secuencial.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="5eaf3-108">Vea también [JetOpenTempTable(JET_SESID, \[ \] , Int32, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="5eaf3-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), "Api.JetOpenTempTable2", [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="5eaf3-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="5eaf3-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="5eaf3-110">**Espacio de nombres:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5eaf3-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="5eaf3-111">**Ensamblado:**  Microsoft.Isam.Esent.Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5eaf3-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5eaf3-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5eaf3-112">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="5eaf3-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5eaf3-113">Parameters</span></span>

  - <span data-ttu-id="5eaf3-114">sesid</span><span class="sxs-lookup"><span data-stu-id="5eaf3-114">sesid</span></span>  
    <span data-ttu-id="5eaf3-115">Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5eaf3-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5eaf3-116">Sesión que se usará.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5eaf3-117">temporarytable</span><span class="sxs-lookup"><span data-stu-id="5eaf3-117">temporarytable</span></span>  
    <span data-ttu-id="5eaf3-118">Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span><span class="sxs-lookup"><span data-stu-id="5eaf3-118">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)</span></span>  
    
    <span data-ttu-id="5eaf3-119">Descripción de la tabla temporal que se creará en la entrada.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-119">Description of the temporary table to create on input.</span></span> <span data-ttu-id="5eaf3-120">Después de una llamada correcta, la estructura contiene el identificador de la tabla temporal y las identificaciones de columna.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-120">After a successful call, the structure contains the handle to the temporary table and column identifications.</span></span> <span data-ttu-id="5eaf3-121">Use [JetCloseTable(JET_SESID, JET_TABLEID) para](./api.jetclosetable-method.md) liberar la tabla temporal cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-121">Use [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) to free the temporary table when finished.</span></span>

## <a name="remarks"></a><span data-ttu-id="5eaf3-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5eaf3-122">Remarks</span></span>

<span data-ttu-id="5eaf3-123">Use [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) para versiones anteriores de Esent.</span><span class="sxs-lookup"><span data-stu-id="5eaf3-123">Use [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md) for earlier versions of Esent.</span></span>

## <a name="see-also"></a><span data-ttu-id="5eaf3-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5eaf3-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5eaf3-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="5eaf3-125">Reference</span></span>

[<span data-ttu-id="5eaf3-126">Clase Windows8Api</span><span class="sxs-lookup"><span data-stu-id="5eaf3-126">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="5eaf3-127">Miembros de Windows8Api</span><span class="sxs-lookup"><span data-stu-id="5eaf3-127">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="5eaf3-128">Espacio de nombres Microsoft.Isam.Esent.Interop.Windows8</span><span class="sxs-lookup"><span data-stu-id="5eaf3-128">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
