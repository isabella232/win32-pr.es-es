---
description: 'Más información sobre: API. JetOpenTable (método)'
title: Método API. JetOpenTable
TOCTitle: 'JetOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentable(v=EXCHG.10)
ms:contentKeyID: 55100776
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5764138d4ea387b68c94805c6966f7ce0e817c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002941"
---
# <a name="apijetopentable-method"></a><span data-ttu-id="e82cc-103">Método API. JetOpenTable</span><span class="sxs-lookup"><span data-stu-id="e82cc-103">Api.JetOpenTable method</span></span>

<span data-ttu-id="e82cc-104">Abre un cursor en una tabla creada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e82cc-104">Opens a cursor on a previously created table.</span></span>

<span data-ttu-id="e82cc-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e82cc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e82cc-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e82cc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e82cc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e82cc-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    parameters As Byte(), _
    parametersSize As Integer, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim parameters As Byte()
Dim parametersSize As Integer
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As JET_wrn

returnValue = Api.JetOpenTable(sesid, _
    dbid, tablename, parameters, parametersSize, _
    grbit, tableid)
```

``` csharp
public static JET_wrn JetOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    byte[] parameters,
    int parametersSize,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="e82cc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e82cc-108">Parameters</span></span>

  - <span data-ttu-id="e82cc-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e82cc-109">sesid</span></span>  
    <span data-ttu-id="e82cc-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e82cc-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e82cc-111">La sesión de base de datos que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="e82cc-111">The database session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e82cc-112">dbid</span><span class="sxs-lookup"><span data-stu-id="e82cc-112">dbid</span></span>  
    <span data-ttu-id="e82cc-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e82cc-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="e82cc-114">Base de datos en la que se va a abrir la tabla.</span><span class="sxs-lookup"><span data-stu-id="e82cc-114">The database to open the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="e82cc-115">tablename</span><span class="sxs-lookup"><span data-stu-id="e82cc-115">tablename</span></span>  
    <span data-ttu-id="e82cc-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e82cc-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e82cc-117">Nombre de la tabla que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="e82cc-117">The name of the table to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="e82cc-118">parámetros</span><span class="sxs-lookup"><span data-stu-id="e82cc-118">parameters</span></span>  
    <span data-ttu-id="e82cc-119">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="e82cc-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="e82cc-120">No se utiliza el parámetro.</span><span class="sxs-lookup"><span data-stu-id="e82cc-120">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="e82cc-121">parametersSize</span><span class="sxs-lookup"><span data-stu-id="e82cc-121">parametersSize</span></span>  
    <span data-ttu-id="e82cc-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e82cc-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e82cc-123">No se utiliza el parámetro.</span><span class="sxs-lookup"><span data-stu-id="e82cc-123">The parameter is not used.</span></span>

<!-- end list -->

  - <span data-ttu-id="e82cc-124">grbit</span><span class="sxs-lookup"><span data-stu-id="e82cc-124">grbit</span></span>  
    <span data-ttu-id="e82cc-125">Tipo: [Microsoft. ISAM. esent. Interop. OpenTableGrbit](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e82cc-125">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e82cc-126">Opciones de apertura de tabla.</span><span class="sxs-lookup"><span data-stu-id="e82cc-126">Table open options.</span></span>

<!-- end list -->

  - <span data-ttu-id="e82cc-127">TABLEID</span><span class="sxs-lookup"><span data-stu-id="e82cc-127">tableid</span></span>  
    <span data-ttu-id="e82cc-128">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e82cc-128">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e82cc-129">Devuelve la tabla abierta.</span><span class="sxs-lookup"><span data-stu-id="e82cc-129">Returns the opened table.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e82cc-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e82cc-130">Return value</span></span>

<span data-ttu-id="e82cc-131">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e82cc-131">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="e82cc-132">Una advertencia de ESENT.</span><span class="sxs-lookup"><span data-stu-id="e82cc-132">An ESENT warning.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e82cc-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e82cc-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e82cc-134">Referencia</span><span class="sxs-lookup"><span data-stu-id="e82cc-134">Reference</span></span>

[<span data-ttu-id="e82cc-135">Clase de API</span><span class="sxs-lookup"><span data-stu-id="e82cc-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e82cc-136">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="e82cc-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e82cc-137">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e82cc-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
