---
description: 'Más información sobre: API. GetColumnDictionary (método)'
title: Método API. GetColumnDictionary
TOCTitle: 'GetColumnDictionary method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getcolumndictionary(v=EXCHG.10)
ms:contentKeyID: 55100653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetColumnDictionary
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ab359c5b8b163ce67f576f35250dd521eb14472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714951"
---
# <a name="apigetcolumndictionary-method"></a><span data-ttu-id="cb373-103">Método API. GetColumnDictionary</span><span class="sxs-lookup"><span data-stu-id="cb373-103">Api.GetColumnDictionary method</span></span>

<span data-ttu-id="cb373-104">Crea un diccionario que asigna nombres de columna a los identificadores de columna.</span><span class="sxs-lookup"><span data-stu-id="cb373-104">Creates a dictionary which maps column names to their column IDs.</span></span>

<span data-ttu-id="cb373-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb373-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cb373-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cb373-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb373-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb373-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetColumnDictionary ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IDictionary(Of String, JET_COLUMNID)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IDictionary(Of String, JET_COLUMNID)

returnValue = Api.GetColumnDictionary(sesid, _
    tableid)
```

``` csharp
public static IDictionary<string, JET_COLUMNID> GetColumnDictionary(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="cb373-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb373-108">Parameters</span></span>

  - <span data-ttu-id="cb373-109">sesid</span><span class="sxs-lookup"><span data-stu-id="cb373-109">sesid</span></span>  
    <span data-ttu-id="cb373-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cb373-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cb373-111">Sesid que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="cb373-111">The sesid to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cb373-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="cb373-112">tableid</span></span>  
    <span data-ttu-id="cb373-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cb373-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="cb373-114">Tabla para la que se va a recuperar la información.</span><span class="sxs-lookup"><span data-stu-id="cb373-114">The table to retrieve the information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cb373-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb373-115">Return value</span></span>

<span data-ttu-id="cb373-116">Tipo: [System. Collections. Generic. IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span><span class="sxs-lookup"><span data-stu-id="cb373-116">Type: [System.Collections.Generic.IDictionary](/dotnet/api/system.collections.generic.idictionary-2)\<[String](/dotnet/api/system.string), [JET_COLUMNID](./jet-columnid-structure.md)\></span></span>  
<span data-ttu-id="cb373-117">Un diccionario que asigna nombres de columna a los identificadores de columna.</span><span class="sxs-lookup"><span data-stu-id="cb373-117">A dictionary mapping column names to column IDs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cb373-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb373-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb373-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="cb373-119">Reference</span></span>

[<span data-ttu-id="cb373-120">Clase de API</span><span class="sxs-lookup"><span data-stu-id="cb373-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cb373-121">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="cb373-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cb373-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cb373-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
