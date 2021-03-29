---
description: 'Más información sobre: API. JetRenameColumn (método)'
title: Método API. JetRenameColumn
TOCTitle: 'JetRenameColumn method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRenameColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.String,Microsoft.Isam.Esent.Interop.RenameColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrenamecolumn(v=EXCHG.10)
ms:contentKeyID: 55100786
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRenameColumn
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRenameColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 007bce82d8749611f0fe2b0eae28b54ddedab98f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818022"
---
# <a name="apijetrenamecolumn-method"></a><span data-ttu-id="5f1de-103">Método API. JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="5f1de-103">Api.JetRenameColumn method</span></span>

<span data-ttu-id="5f1de-104">Cambia el nombre de una columna existente.</span><span class="sxs-lookup"><span data-stu-id="5f1de-104">Changes the name of an existing column.</span></span>

<span data-ttu-id="5f1de-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5f1de-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5f1de-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5f1de-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5f1de-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f1de-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRenameColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    name As String, _
    newName As String, _
    grbit As RenameColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim name As String
Dim newName As String
Dim grbit As RenameColumnGrbitApi.JetRenameColumn(sesid, tableid, _
    name, newName, grbit)
```

``` csharp
public static void JetRenameColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string name,
    string newName,
    RenameColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5f1de-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5f1de-108">Parameters</span></span>

  - <span data-ttu-id="5f1de-109">sesid</span><span class="sxs-lookup"><span data-stu-id="5f1de-109">sesid</span></span>  
    <span data-ttu-id="5f1de-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5f1de-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5f1de-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="5f1de-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5f1de-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="5f1de-112">tableid</span></span>  
    <span data-ttu-id="5f1de-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5f1de-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5f1de-114">Tabla que contiene la columna.</span><span class="sxs-lookup"><span data-stu-id="5f1de-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="5f1de-115">name</span><span class="sxs-lookup"><span data-stu-id="5f1de-115">name</span></span>  
    <span data-ttu-id="5f1de-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5f1de-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5f1de-117">El nombre de la columna.</span><span class="sxs-lookup"><span data-stu-id="5f1de-117">The name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="5f1de-118">newName</span><span class="sxs-lookup"><span data-stu-id="5f1de-118">newName</span></span>  
    <span data-ttu-id="5f1de-119">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5f1de-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5f1de-120">El nuevo nombre de la columna.</span><span class="sxs-lookup"><span data-stu-id="5f1de-120">The new name of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="5f1de-121">grbit</span><span class="sxs-lookup"><span data-stu-id="5f1de-121">grbit</span></span>  
    <span data-ttu-id="5f1de-122">Tipo: [Microsoft. ISAM. esent. Interop. RenameColumnGrbit](./renamecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5f1de-122">Type: [Microsoft.Isam.Esent.Interop.RenameColumnGrbit](./renamecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5f1de-123">Opciones de cambio de nombre de columna.</span><span class="sxs-lookup"><span data-stu-id="5f1de-123">Column rename options.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f1de-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f1de-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5f1de-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="5f1de-125">Reference</span></span>

[<span data-ttu-id="5f1de-126">Clase de API</span><span class="sxs-lookup"><span data-stu-id="5f1de-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5f1de-127">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="5f1de-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5f1de-128">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5f1de-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
