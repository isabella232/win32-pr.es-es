---
description: 'Más información sobre: API. JetSetColumns (método)'
title: Método API. JetSetColumns
TOCTitle: 'JetSetColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_SETCOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumns(v=EXCHG.10)
ms:contentKeyID: 55100800
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 59d1d16a21996937357d0358625772a4b6712019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809217"
---
# <a name="apijetsetcolumns-method"></a><span data-ttu-id="c17cf-103">Método API. JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="c17cf-103">Api.JetSetColumns method</span></span>

<span data-ttu-id="c17cf-104">Permite que una aplicación establezca varios valores de columna en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="c17cf-104">Allows an application to set multiple column values in a single operation.</span></span> <span data-ttu-id="c17cf-105">Una matriz de estructuras [JET_SETCOLUMN](./jet-setcolumn-class.md) se utiliza para describir el conjunto de valores de columna que se va a establecer y para describir los búferes de entrada de cada valor de columna que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="c17cf-105">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures is used to describe the set of column values to be set, and to describe input buffers for each column value to be set.</span></span>

<span data-ttu-id="c17cf-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c17cf-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c17cf-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c17cf-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c17cf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c17cf-108">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Shared Function JetSetColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    setcolumns As JET_SETCOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim setcolumns As JET_SETCOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetSetColumns(sesid, _
    tableid, setcolumns, numColumns)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public static JET_wrn JetSetColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_SETCOLUMN[] setcolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="c17cf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c17cf-109">Parameters</span></span>

  - <span data-ttu-id="c17cf-110">sesid</span><span class="sxs-lookup"><span data-stu-id="c17cf-110">sesid</span></span>  
    <span data-ttu-id="c17cf-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c17cf-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c17cf-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="c17cf-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c17cf-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="c17cf-113">tableid</span></span>  
    <span data-ttu-id="c17cf-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c17cf-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c17cf-115">Cursor en el que se van a establecer las columnas.</span><span class="sxs-lookup"><span data-stu-id="c17cf-115">The cursor to set the columns on.</span></span>

<!-- end list -->

  - <span data-ttu-id="c17cf-116">SetColumns</span><span class="sxs-lookup"><span data-stu-id="c17cf-116">setcolumns</span></span>  
    <span data-ttu-id="c17cf-117">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="c17cf-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="c17cf-118">Matriz de estructuras [JET_SETCOLUMN](./jet-setcolumn-class.md) que describen los datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="c17cf-118">An array of [JET_SETCOLUMN](./jet-setcolumn-class.md) structures describing the data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="c17cf-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="c17cf-119">numColumns</span></span>  
    <span data-ttu-id="c17cf-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c17cf-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c17cf-121">Número de entradas en el parámetro SetColumns.</span><span class="sxs-lookup"><span data-stu-id="c17cf-121">Number of entries in the setcolumns parameter.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c17cf-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c17cf-122">Return value</span></span>

<span data-ttu-id="c17cf-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c17cf-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="c17cf-124">Una advertencia.</span><span class="sxs-lookup"><span data-stu-id="c17cf-124">A warning.</span></span> <span data-ttu-id="c17cf-125">Si el último conjunto de columnas tiene una advertencia, esta advertencia se devolverá desde JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="c17cf-125">If the last column set has a warning, then this warning will be returned from JetSetColumns itself.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c17cf-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c17cf-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c17cf-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="c17cf-127">Reference</span></span>

[<span data-ttu-id="c17cf-128">Clase de API</span><span class="sxs-lookup"><span data-stu-id="c17cf-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c17cf-129">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="c17cf-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c17cf-130">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c17cf-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
