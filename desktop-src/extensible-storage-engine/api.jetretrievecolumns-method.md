---
description: 'Más información sobre: API. JetRetrieveColumns (método)'
title: Método API. JetRetrieveColumns
TOCTitle: 'JetRetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100797
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3fd4db2ce8cbcad5f74db7d4c95363aa68e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705514"
---
# <a name="apijetretrievecolumns-method"></a><span data-ttu-id="f2eb0-103">Método API. JetRetrieveColumns</span><span class="sxs-lookup"><span data-stu-id="f2eb0-103">Api.JetRetrieveColumns method</span></span>

<span data-ttu-id="f2eb0-104">Recupera varios valores de columna del registro actual en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-104">Retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="f2eb0-105">Una matriz de estructuras JET_RETRIEVECOLUMN se utiliza para describir el conjunto de valores de columna que se va a recuperar y para describir los búferes de salida de cada valor de columna que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-105">An array of JET_RETRIEVECOLUMN structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

<span data-ttu-id="f2eb0-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f2eb0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f2eb0-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f2eb0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f2eb0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2eb0-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    retrievecolumns As JET_RETRIEVECOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim retrievecolumns As JET_RETRIEVECOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumns(sesid, _
    tableid, retrievecolumns, numColumns)
```

``` csharp
public static JET_wrn JetRetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RETRIEVECOLUMN[] retrievecolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="f2eb0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2eb0-109">Parameters</span></span>

  - <span data-ttu-id="f2eb0-110">sesid</span><span class="sxs-lookup"><span data-stu-id="f2eb0-110">sesid</span></span>  
    <span data-ttu-id="f2eb0-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2eb0-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f2eb0-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2eb0-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="f2eb0-113">tableid</span></span>  
    <span data-ttu-id="f2eb0-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f2eb0-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f2eb0-115">Cursor del que se van a recuperar los datos.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-115">The cursor to retrieve the data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2eb0-116">retrievecolumns</span><span class="sxs-lookup"><span data-stu-id="f2eb0-116">retrievecolumns</span></span>  
    <span data-ttu-id="f2eb0-117">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="f2eb0-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="f2eb0-118">Matriz de uno o más objetos [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) que describen los datos que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-118">An array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) objects describing the data to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="f2eb0-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="f2eb0-119">numColumns</span></span>  
    <span data-ttu-id="f2eb0-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f2eb0-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f2eb0-121">Número de entradas de la matriz de columnas.</span><span class="sxs-lookup"><span data-stu-id="f2eb0-121">The number of entries in the columns array.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f2eb0-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2eb0-122">Return value</span></span>

<span data-ttu-id="f2eb0-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f2eb0-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="f2eb0-124">Si alguna columna recuperada se trunca debido a un búfer de longitud insuficiente, la API devolverá [BufferTruncated](./jet-wrn-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="f2eb0-124">If any column retrieved is truncated due to an insufficient length buffer, then the API will return [BufferTruncated](./jet-wrn-enumeration.md).</span></span> <span data-ttu-id="f2eb0-125">Sin embargo, otros errores JET_wrnColumnNull se devuelven solo en el campo error del objeto [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f2eb0-125">However other errors JET_wrnColumnNull are returned only in the error field of the [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) object.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f2eb0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2eb0-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f2eb0-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="f2eb0-127">Reference</span></span>

[<span data-ttu-id="f2eb0-128">Clase de API</span><span class="sxs-lookup"><span data-stu-id="f2eb0-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f2eb0-129">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="f2eb0-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f2eb0-130">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f2eb0-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
