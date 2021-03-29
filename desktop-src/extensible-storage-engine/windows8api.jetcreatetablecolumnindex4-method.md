---
description: 'Más información sobre: Windows8Api. JetCreateTableColumnIndex4 (método)'
title: Método Windows8Api. JetCreateTableColumnIndex4 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetCreateTableColumnIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateTableColumnIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_TABLECREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetcreatetablecolumnindex4(v=EXCHG.10)
ms:contentKeyID: 55107827
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateTableColumnIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetCreateTableColumnIndex4
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1551c3e243ef45b7f261fd01a6b1c7926478437d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811377"
---
# <a name="windows8apijetcreatetablecolumnindex4-method"></a><span data-ttu-id="30f15-103">Windows8Api. JetCreateTableColumnIndex4, método</span><span class="sxs-lookup"><span data-stu-id="30f15-103">Windows8Api.JetCreateTableColumnIndex4 method</span></span>

<span data-ttu-id="30f15-104">Crea una tabla, agrega columnas e índices en esa tabla.</span><span class="sxs-lookup"><span data-stu-id="30f15-104">Creates a table, adds columns, and indices on that table.</span></span> [<span data-ttu-id="30f15-105">JetCreateTableColumnIndex3 (JET_SESID, JET_DBID, JET_TABLECREATE)</span><span class="sxs-lookup"><span data-stu-id="30f15-105">JetCreateTableColumnIndex3(JET_SESID, JET_DBID, JET_TABLECREATE)</span></span>](./api.jetcreatetablecolumnindex3-method.md)

<span data-ttu-id="30f15-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="30f15-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="30f15-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="30f15-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="30f15-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30f15-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTableColumnIndex4 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablecreate As JET_TABLECREATE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablecreate As JET_TABLECREATEWindows8Api.JetCreateTableColumnIndex4(sesid, _
    dbid, tablecreate)
```

``` csharp
public static void JetCreateTableColumnIndex4(
    JET_SESID sesid,
    JET_DBID dbid,
    JET_TABLECREATE tablecreate
)
```

#### <a name="parameters"></a><span data-ttu-id="30f15-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30f15-109">Parameters</span></span>

  - <span data-ttu-id="30f15-110">sesid</span><span class="sxs-lookup"><span data-stu-id="30f15-110">sesid</span></span>  
    <span data-ttu-id="30f15-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="30f15-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="30f15-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="30f15-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="30f15-113">dbid</span><span class="sxs-lookup"><span data-stu-id="30f15-113">dbid</span></span>  
    <span data-ttu-id="30f15-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="30f15-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="30f15-115">La base de datos a la que se va a agregar la nueva tabla.</span><span class="sxs-lookup"><span data-stu-id="30f15-115">The database to which to add the new table.</span></span>

<!-- end list -->

  - <span data-ttu-id="30f15-116">tablecreate</span><span class="sxs-lookup"><span data-stu-id="30f15-116">tablecreate</span></span>  
    <span data-ttu-id="30f15-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span><span class="sxs-lookup"><span data-stu-id="30f15-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLECREATE](./jet-tablecreate-class.md)</span></span>  
    
    <span data-ttu-id="30f15-118">Objeto que describe la tabla que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="30f15-118">Object describing the table to create.</span></span>

## <a name="see-also"></a><span data-ttu-id="30f15-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="30f15-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="30f15-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="30f15-120">Reference</span></span>

[<span data-ttu-id="30f15-121">Clase Windows8Api</span><span class="sxs-lookup"><span data-stu-id="30f15-121">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="30f15-122">Miembros de Windows8Api</span><span class="sxs-lookup"><span data-stu-id="30f15-122">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="30f15-123">Espacio de nombres Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="30f15-123">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
