---
description: 'Más información sobre: API. JetCreateTableColumnIndex3 (método)'
title: Método API. JetCreateTableColumnIndex3
TOCTitle: 'JetCreateTableColumnIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetablecolumnindex3(v=EXCHG.10)
ms:contentKeyID: 55100678
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTableColumnIndex3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a967db8f6a322ac29ba8a1e9352972ff1f4f4b76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497159"
---
# <a name="apijetcreatetablecolumnindex3-method"></a><span data-ttu-id="86a41-103">Método API. JetCreateTableColumnIndex3</span><span class="sxs-lookup"><span data-stu-id="86a41-103">Api.JetCreateTableColumnIndex3 method</span></span>

<span data-ttu-id="86a41-104">Crea una tabla, agrega columnas e índices en esa tabla.</span><span class="sxs-lookup"><span data-stu-id="86a41-104">Creates a table, adds columns, and indices on that table.</span></span>

<span data-ttu-id="86a41-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="86a41-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="86a41-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="86a41-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="86a41-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86a41-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTableColumnIndex3 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablecreate As JET_TABLECREATE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablecreate As JET_TABLECREATEApi.JetCreateTableColumnIndex3(sesid, _
    dbid, tablecreate)
```

``` csharp
public static void JetCreateTableColumnIndex3(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLECREATE tablecreate
)
```

#### <a name="parameters"></a><span data-ttu-id="86a41-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="86a41-108">Parameters</span></span>

  - <span data-ttu-id="86a41-109">sesid</span><span class="sxs-lookup"><span data-stu-id="86a41-109">sesid</span></span>  
    <span data-ttu-id="86a41-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="86a41-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="86a41-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="86a41-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="86a41-112">dbid</span><span class="sxs-lookup"><span data-stu-id="86a41-112">dbid</span></span>  
    <span data-ttu-id="86a41-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="86a41-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="86a41-114">La base de datos a la que se va a agregar la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="86a41-114">The database to which to add the new table.</span></span>

<!-- end list -->

  - <span data-ttu-id="86a41-115">tablecreate</span><span class="sxs-lookup"><span data-stu-id="86a41-115">tablecreate</span></span>  
    <span data-ttu-id="86a41-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="86a41-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span></span>  
    
    <span data-ttu-id="86a41-117">Objeto que describe la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="86a41-117">Object describing the table to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="86a41-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="86a41-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="86a41-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="86a41-119">Reference</span></span>

[<span data-ttu-id="86a41-120">Clase de API</span><span class="sxs-lookup"><span data-stu-id="86a41-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="86a41-121">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="86a41-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="86a41-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="86a41-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
