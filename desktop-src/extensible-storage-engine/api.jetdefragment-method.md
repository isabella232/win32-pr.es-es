---
description: 'Más información sobre: API. JetDefragment (método)'
title: Método API. JetDefragment
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69428d785bf9d607199cb62bfe02d2e373e7dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715049"
---
# <a name="apijetdefragment-method"></a><span data-ttu-id="6e91f-103">Método API. JetDefragment</span><span class="sxs-lookup"><span data-stu-id="6e91f-103">Api.JetDefragment method</span></span>

<span data-ttu-id="6e91f-104">Inicia y detiene las tareas de desfragmentación de bases de datos que mejora la organización de datos en una base de datos.</span><span class="sxs-lookup"><span data-stu-id="6e91f-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="6e91f-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6e91f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6e91f-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6e91f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6e91f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e91f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="6e91f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e91f-108">Parameters</span></span>

  - <span data-ttu-id="6e91f-109">sesid</span><span class="sxs-lookup"><span data-stu-id="6e91f-109">sesid</span></span>  
    <span data-ttu-id="6e91f-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6e91f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6e91f-111">La sesión que se va a usar para la llamada.</span><span class="sxs-lookup"><span data-stu-id="6e91f-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e91f-112">dbid</span><span class="sxs-lookup"><span data-stu-id="6e91f-112">dbid</span></span>  
    <span data-ttu-id="6e91f-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6e91f-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="6e91f-114">Base de datos que se va a desfragmentar.</span><span class="sxs-lookup"><span data-stu-id="6e91f-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e91f-115">tableName</span><span class="sxs-lookup"><span data-stu-id="6e91f-115">tableName</span></span>  
    <span data-ttu-id="6e91f-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6e91f-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6e91f-117">Parámetro sin usar.</span><span class="sxs-lookup"><span data-stu-id="6e91f-117">Unused parameter.</span></span> <span data-ttu-id="6e91f-118">La desfragmentación se realiza para toda la base de datos descrita por el identificador de base de datos especificado.</span><span class="sxs-lookup"><span data-stu-id="6e91f-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e91f-119">paso</span><span class="sxs-lookup"><span data-stu-id="6e91f-119">passes</span></span>  
    <span data-ttu-id="6e91f-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6e91f-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6e91f-121">Al iniciar una tarea de desfragmentación con conexión, este parámetro establece el número máximo de pasos de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="6e91f-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="6e91f-122">Al detener una tarea de desfragmentación con conexión, este parámetro se establece en el número de pasos realizados.</span><span class="sxs-lookup"><span data-stu-id="6e91f-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e91f-123">segundos</span><span class="sxs-lookup"><span data-stu-id="6e91f-123">seconds</span></span>  
    <span data-ttu-id="6e91f-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6e91f-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6e91f-125">Al iniciar una tarea de desfragmentación con conexión, este parámetro establece el tiempo máximo para la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="6e91f-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="6e91f-126">Al detener una tarea de desfragmentación en línea, este búfer de salida se establece en el período de tiempo utilizado para la desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="6e91f-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="6e91f-127">grbit</span><span class="sxs-lookup"><span data-stu-id="6e91f-127">grbit</span></span>  
    <span data-ttu-id="6e91f-128">Tipo: [Microsoft. ISAM. esent. Interop. DefragGrbit](./defraggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6e91f-128">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="6e91f-129">Opciones de desfragmentación.</span><span class="sxs-lookup"><span data-stu-id="6e91f-129">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6e91f-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e91f-130">Return value</span></span>

<span data-ttu-id="6e91f-131">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6e91f-131">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="6e91f-132">Código de advertencia.</span><span class="sxs-lookup"><span data-stu-id="6e91f-132">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6e91f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e91f-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6e91f-134">Referencia</span><span class="sxs-lookup"><span data-stu-id="6e91f-134">Reference</span></span>

[<span data-ttu-id="6e91f-135">Clase de API</span><span class="sxs-lookup"><span data-stu-id="6e91f-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6e91f-136">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="6e91f-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6e91f-137">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6e91f-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
