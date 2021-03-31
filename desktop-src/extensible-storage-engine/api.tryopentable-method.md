---
description: 'Más información sobre: API. TryOpenTable (método)'
title: Método API. TryOpenTable
TOCTitle: 'TryOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryopentable(v=EXCHG.10)
ms:contentKeyID: 55100889
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 556d3f12f24229326a6b26f357e5b19801119b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423748"
---
# <a name="apitryopentable-method"></a><span data-ttu-id="aca43-103">Método API. TryOpenTable</span><span class="sxs-lookup"><span data-stu-id="aca43-103">Api.TryOpenTable method</span></span>

<span data-ttu-id="aca43-104">Intente abrir una tabla.</span><span class="sxs-lookup"><span data-stu-id="aca43-104">Try to open a table.</span></span>

<span data-ttu-id="aca43-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aca43-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aca43-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aca43-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aca43-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aca43-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryOpenTable(sesid, _
    dbid, tablename, grbit, tableid)
```

``` csharp
public static bool TryOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="aca43-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aca43-108">Parameters</span></span>

  - <span data-ttu-id="aca43-109">sesid</span><span class="sxs-lookup"><span data-stu-id="aca43-109">sesid</span></span>  
    <span data-ttu-id="aca43-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aca43-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="aca43-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="aca43-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="aca43-112">dbid</span><span class="sxs-lookup"><span data-stu-id="aca43-112">dbid</span></span>  
    <span data-ttu-id="aca43-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aca43-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="aca43-114">La base de datos para buscar la tabla en.</span><span class="sxs-lookup"><span data-stu-id="aca43-114">The database to look for the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="aca43-115">tablename</span><span class="sxs-lookup"><span data-stu-id="aca43-115">tablename</span></span>  
    <span data-ttu-id="aca43-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="aca43-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="aca43-117">Nombre de la tabla.</span><span class="sxs-lookup"><span data-stu-id="aca43-117">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="aca43-118">grbit</span><span class="sxs-lookup"><span data-stu-id="aca43-118">grbit</span></span>  
    <span data-ttu-id="aca43-119">Tipo: [Microsoft. ISAM. esent. Interop. OpenTableGrbit](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="aca43-119">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="aca43-120">Opciones de apertura de tabla.</span><span class="sxs-lookup"><span data-stu-id="aca43-120">Table open options.</span></span>

<!-- end list -->

  - <span data-ttu-id="aca43-121">TABLEID</span><span class="sxs-lookup"><span data-stu-id="aca43-121">tableid</span></span>  
    <span data-ttu-id="aca43-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aca43-122">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="aca43-123">Devuelve el TABLEID abierto.</span><span class="sxs-lookup"><span data-stu-id="aca43-123">Returns the opened tableid.</span></span>

#### <a name="return-value"></a><span data-ttu-id="aca43-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aca43-124">Return value</span></span>

<span data-ttu-id="aca43-125">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="aca43-125">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="aca43-126">True si se abrió la tabla, false si la tabla no existe.</span><span class="sxs-lookup"><span data-stu-id="aca43-126">True if the table was opened, false if the table doesn't exist.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aca43-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="aca43-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aca43-128">Referencia</span><span class="sxs-lookup"><span data-stu-id="aca43-128">Reference</span></span>

[<span data-ttu-id="aca43-129">Clase de API</span><span class="sxs-lookup"><span data-stu-id="aca43-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="aca43-130">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="aca43-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="aca43-131">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="aca43-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
