---
description: 'Más información sobre: VistaApi. JetGetColumnInfo (método)'
title: Método VistaApi. JetGetColumnInfo (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetGetColumnInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55104283
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ae090fa5279b9ec60a3be88b4ebda393322b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154548"
---
# <a name="vistaapijetgetcolumninfo-method"></a><span data-ttu-id="db044-103">VistaApi. JetGetColumnInfo, método</span><span class="sxs-lookup"><span data-stu-id="db044-103">VistaApi.JetGetColumnInfo method</span></span>

<span data-ttu-id="db044-104">Recupera información sobre una columna de una tabla.</span><span class="sxs-lookup"><span data-stu-id="db044-104">Retrieves information about a column in a table.</span></span>

<span data-ttu-id="db044-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="db044-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="db044-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="db044-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="db044-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="db044-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnid As JET_COLUMNID, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnid As JET_COLUMNID
Dim columnbase As JET_COLUMNBASEVistaApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnid, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    JET_COLUMNID columnid,
    out JET_COLUMNBASE columnbase
)
```

#### <a name="parameters"></a><span data-ttu-id="db044-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db044-108">Parameters</span></span>

  - <span data-ttu-id="db044-109">sesid</span><span class="sxs-lookup"><span data-stu-id="db044-109">sesid</span></span>  
    <span data-ttu-id="db044-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="db044-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="db044-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="db044-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="db044-112">dbid</span><span class="sxs-lookup"><span data-stu-id="db044-112">dbid</span></span>  
    <span data-ttu-id="db044-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="db044-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="db044-114">La base de datos que contiene la tabla.</span><span class="sxs-lookup"><span data-stu-id="db044-114">The database that contains the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="db044-115">tablename</span><span class="sxs-lookup"><span data-stu-id="db044-115">tablename</span></span>  
    <span data-ttu-id="db044-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="db044-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="db044-117">Nombre de la tabla que contiene la columna.</span><span class="sxs-lookup"><span data-stu-id="db044-117">The name of the table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="db044-118">columnid</span><span class="sxs-lookup"><span data-stu-id="db044-118">columnid</span></span>  
    <span data-ttu-id="db044-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="db044-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="db044-120">IDENTIFICADOR de la columna.</span><span class="sxs-lookup"><span data-stu-id="db044-120">The ID of the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="db044-121">columnbase</span><span class="sxs-lookup"><span data-stu-id="db044-121">columnbase</span></span>  
    <span data-ttu-id="db044-122">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="db044-122">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="db044-123">Se rellena con información acerca de las columnas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="db044-123">Filled in with information about the columns in the table.</span></span>

## <a name="see-also"></a><span data-ttu-id="db044-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="db044-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="db044-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="db044-125">Reference</span></span>

[<span data-ttu-id="db044-126">Clase VistaApi</span><span class="sxs-lookup"><span data-stu-id="db044-126">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="db044-127">Miembros de VistaApi</span><span class="sxs-lookup"><span data-stu-id="db044-127">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="db044-128">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="db044-128">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
