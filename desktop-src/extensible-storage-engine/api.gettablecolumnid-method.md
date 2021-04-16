---
description: 'Más información sobre: API. GetTableColumnid (método)'
title: Método API. GetTableColumnid
TOCTitle: 'GetTableColumnid method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableColumnid(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettablecolumnid(v=EXCHG.10)
ms:contentKeyID: 55107215
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableColumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ec91b014401709b6312b3363d8dae9e7da3d200e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539747"
---
# <a name="apigettablecolumnid-method"></a><span data-ttu-id="73379-103">Método API. GetTableColumnid</span><span class="sxs-lookup"><span data-stu-id="73379-103">Api.GetTableColumnid method</span></span>

<span data-ttu-id="73379-104">Obtiene el columnid de la columna especificada.</span><span class="sxs-lookup"><span data-stu-id="73379-104">Get the columnid of the specified column.</span></span>

<span data-ttu-id="73379-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="73379-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="73379-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="73379-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="73379-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73379-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableColumnid ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnName As String _
) As JET_COLUMNID
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnName As String
Dim returnValue As JET_COLUMNID

returnValue = Api.GetTableColumnid(sesid, _
    tableid, columnName)
```

``` csharp
public static JET_COLUMNID GetTableColumnid(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string columnName
)
```

#### <a name="parameters"></a><span data-ttu-id="73379-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73379-108">Parameters</span></span>

  - <span data-ttu-id="73379-109">sesid</span><span class="sxs-lookup"><span data-stu-id="73379-109">sesid</span></span>  
    <span data-ttu-id="73379-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="73379-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="73379-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="73379-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="73379-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="73379-112">tableid</span></span>  
    <span data-ttu-id="73379-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="73379-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="73379-114">Tabla que contiene la columna.</span><span class="sxs-lookup"><span data-stu-id="73379-114">The table containing the column.</span></span>

<!-- end list -->

  - <span data-ttu-id="73379-115">columnName</span><span class="sxs-lookup"><span data-stu-id="73379-115">columnName</span></span>  
    <span data-ttu-id="73379-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="73379-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="73379-117">El nombre de la columna.</span><span class="sxs-lookup"><span data-stu-id="73379-117">The name of the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="73379-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73379-118">Return value</span></span>

<span data-ttu-id="73379-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="73379-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
<span data-ttu-id="73379-120">Identificador de la columna.</span><span class="sxs-lookup"><span data-stu-id="73379-120">The id of the column.</span></span>  

## <a name="see-also"></a><span data-ttu-id="73379-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="73379-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="73379-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="73379-122">Reference</span></span>

[<span data-ttu-id="73379-123">Clase de API</span><span class="sxs-lookup"><span data-stu-id="73379-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="73379-124">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="73379-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="73379-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="73379-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
