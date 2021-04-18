---
description: 'Más información sobre: API. JetDeleteColumn2 (método)'
title: Método API. JetDeleteColumn2
TOCTitle: 'JetDeleteColumn2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.DeleteColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletecolumn2(v=EXCHG.10)
ms:contentKeyID: 55100680
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteColumn2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0426ca2557dac11c565211162438db6d5c77a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715047"
---
# <a name="apijetdeletecolumn2-method"></a><span data-ttu-id="a07a2-103">Método API. JetDeleteColumn2</span><span class="sxs-lookup"><span data-stu-id="a07a2-103">Api.JetDeleteColumn2 method</span></span>

<span data-ttu-id="a07a2-104">Elimina una columna de una tabla de base de datos.</span><span class="sxs-lookup"><span data-stu-id="a07a2-104">Deletes a column from a database table.</span></span>

<span data-ttu-id="a07a2-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a07a2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a07a2-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a07a2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a07a2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a07a2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDeleteColumn2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    column As String, _
    grbit As DeleteColumnGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim column As String
Dim grbit As DeleteColumnGrbitApi.JetDeleteColumn2(sesid, tableid, _
    column, grbit)
```

``` csharp
public static void JetDeleteColumn2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string column,
    DeleteColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="a07a2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a07a2-108">Parameters</span></span>

  - <span data-ttu-id="a07a2-109">sesid</span><span class="sxs-lookup"><span data-stu-id="a07a2-109">sesid</span></span>  
    <span data-ttu-id="a07a2-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a07a2-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a07a2-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="a07a2-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a07a2-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="a07a2-112">tableid</span></span>  
    <span data-ttu-id="a07a2-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a07a2-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a07a2-114">Cursor en la tabla de la que se va a eliminar la columna.</span><span class="sxs-lookup"><span data-stu-id="a07a2-114">A cursor on the table to delete the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="a07a2-115">columna</span><span class="sxs-lookup"><span data-stu-id="a07a2-115">column</span></span>  
    <span data-ttu-id="a07a2-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a07a2-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a07a2-117">Nombre de la columna que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="a07a2-117">The name of the column to be deleted.</span></span>

<!-- end list -->

  - <span data-ttu-id="a07a2-118">grbit</span><span class="sxs-lookup"><span data-stu-id="a07a2-118">grbit</span></span>  
    <span data-ttu-id="a07a2-119">Tipo: [Microsoft. ISAM. esent. Interop. DeleteColumnGrbit](./deletecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a07a2-119">Type: [Microsoft.Isam.Esent.Interop.DeleteColumnGrbit](./deletecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a07a2-120">Opciones de eliminación de columnas.</span><span class="sxs-lookup"><span data-stu-id="a07a2-120">Column deletion options.</span></span>

## <a name="see-also"></a><span data-ttu-id="a07a2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a07a2-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a07a2-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="a07a2-122">Reference</span></span>

[<span data-ttu-id="a07a2-123">Clase de API</span><span class="sxs-lookup"><span data-stu-id="a07a2-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a07a2-124">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="a07a2-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a07a2-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a07a2-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
