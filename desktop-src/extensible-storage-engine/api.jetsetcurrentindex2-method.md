---
description: 'Más información sobre: API. JetSetCurrentIndex2 (método)'
title: Método API. JetSetCurrentIndex2
TOCTitle: 'JetSetCurrentIndex2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex2(v=EXCHG.10)
ms:contentKeyID: 55100798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e08e1fe5027641348259381d74b34ce16b034e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423752"
---
# <a name="apijetsetcurrentindex2-method"></a><span data-ttu-id="f8464-103">Método API. JetSetCurrentIndex2</span><span class="sxs-lookup"><span data-stu-id="f8464-103">Api.JetSetCurrentIndex2 method</span></span>

<span data-ttu-id="f8464-104">Establece el índice actual de un cursor.</span><span class="sxs-lookup"><span data-stu-id="f8464-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="f8464-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8464-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8464-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8464-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8464-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8464-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    grbit As SetCurrentIndexGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim grbit As SetCurrentIndexGrbitApi.JetSetCurrentIndex2(sesid, _
    tableid, index, grbit)
```

``` csharp
public static void JetSetCurrentIndex2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    SetCurrentIndexGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f8464-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8464-108">Parameters</span></span>

  - <span data-ttu-id="f8464-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f8464-109">sesid</span></span>  
    <span data-ttu-id="f8464-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8464-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f8464-111">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="f8464-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8464-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="f8464-112">tableid</span></span>  
    <span data-ttu-id="f8464-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8464-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f8464-114">Cursor en el que se va a establecer el índice.</span><span class="sxs-lookup"><span data-stu-id="f8464-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8464-115">índice</span><span class="sxs-lookup"><span data-stu-id="f8464-115">index</span></span>  
    <span data-ttu-id="f8464-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f8464-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="f8464-117">Nombre del índice que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="f8464-117">The name of the index to be selected.</span></span> <span data-ttu-id="f8464-118">Si es null o está vacío, se seleccionará el índice principal.</span><span class="sxs-lookup"><span data-stu-id="f8464-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8464-119">grbit</span><span class="sxs-lookup"><span data-stu-id="f8464-119">grbit</span></span>  
    <span data-ttu-id="f8464-120">Tipo: [Microsoft. ISAM. esent. Interop. SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f8464-120">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f8464-121">Establecer opciones de índice.</span><span class="sxs-lookup"><span data-stu-id="f8464-121">Set index options.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8464-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8464-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8464-123">Referencia</span><span class="sxs-lookup"><span data-stu-id="f8464-123">Reference</span></span>

[<span data-ttu-id="f8464-124">Clase de API</span><span class="sxs-lookup"><span data-stu-id="f8464-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f8464-125">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="f8464-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f8464-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f8464-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
