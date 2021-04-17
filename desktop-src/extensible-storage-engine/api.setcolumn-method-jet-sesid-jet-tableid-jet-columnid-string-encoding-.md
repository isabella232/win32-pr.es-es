---
description: 'Más información sobre: método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, cadena, codificación)'
title: Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, cadena, codificación)
TOCTitle: SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.SetColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.String,System.Text.Encoding)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.setcolumn(v=EXCHG.10)
ms:contentKeyID: 55100935
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.SetColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7237bd6ba02e15ade70ee03330332242977822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697340"
---
# <a name="apisetcolumn-method-jet_sesid-jet_tableid-jet_columnid-string-encoding"></a><span data-ttu-id="8aceb-103">Método API. SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, cadena, codificación)</span><span class="sxs-lookup"><span data-stu-id="8aceb-103">Api.SetColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, String, Encoding)</span></span>

<span data-ttu-id="8aceb-104">Modifica un valor de columna única en un registro modificado que se va a insertar o actualizar el registro actual.</span><span class="sxs-lookup"><span data-stu-id="8aceb-104">Modifies a single column value in a modified record to be inserted or to update the current record.</span></span>

<span data-ttu-id="8aceb-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8aceb-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8aceb-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8aceb-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8aceb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8aceb-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub SetColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As String, _
    encoding As Encoding _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As String
Dim encoding As EncodingApi.SetColumn(sesid, tableid, columnid, _
    data, encoding)
```

``` csharp
public static void SetColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    string data,
    Encoding encoding
)
```

#### <a name="parameters"></a><span data-ttu-id="8aceb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8aceb-108">Parameters</span></span>

  - <span data-ttu-id="8aceb-109">sesid</span><span class="sxs-lookup"><span data-stu-id="8aceb-109">sesid</span></span>  
    <span data-ttu-id="8aceb-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8aceb-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8aceb-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="8aceb-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8aceb-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="8aceb-112">tableid</span></span>  
    <span data-ttu-id="8aceb-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8aceb-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8aceb-114">Cursor que se va a actualizar.</span><span class="sxs-lookup"><span data-stu-id="8aceb-114">The cursor to update.</span></span> <span data-ttu-id="8aceb-115">Se debe preparar una actualización.</span><span class="sxs-lookup"><span data-stu-id="8aceb-115">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="8aceb-116">columnid</span><span class="sxs-lookup"><span data-stu-id="8aceb-116">columnid</span></span>  
    <span data-ttu-id="8aceb-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8aceb-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="8aceb-118">Columnid que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="8aceb-118">The columnid to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="8aceb-119">datos</span><span class="sxs-lookup"><span data-stu-id="8aceb-119">data</span></span>  
    <span data-ttu-id="8aceb-120">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8aceb-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8aceb-121">Datos que se van a establecer.</span><span class="sxs-lookup"><span data-stu-id="8aceb-121">The data to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="8aceb-122">encoding</span><span class="sxs-lookup"><span data-stu-id="8aceb-122">encoding</span></span>  
    <span data-ttu-id="8aceb-123">Tipo: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="8aceb-123">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="8aceb-124">Codificación que se usa para convertir la cadena.</span><span class="sxs-lookup"><span data-stu-id="8aceb-124">The encoding used to convert the string.</span></span>

## <a name="see-also"></a><span data-ttu-id="8aceb-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8aceb-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8aceb-126">Referencia</span><span class="sxs-lookup"><span data-stu-id="8aceb-126">Reference</span></span>

[<span data-ttu-id="8aceb-127">Clase de API</span><span class="sxs-lookup"><span data-stu-id="8aceb-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8aceb-128">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="8aceb-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8aceb-129">Sobrecarga SetColumn</span><span class="sxs-lookup"><span data-stu-id="8aceb-129">SetColumn overload</span></span>](./api.setcolumn-method.md)

[<span data-ttu-id="8aceb-130">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8aceb-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
