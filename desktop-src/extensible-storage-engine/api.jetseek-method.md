---
description: 'Más información sobre: API. JetSeek (método)'
title: Método API. JetSeek
TOCTitle: 'JetSeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetseek(v=EXCHG.10)
ms:contentKeyID: 55100796
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85c8c61bd4e56b342b33d26f22ae3946967640e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003005"
---
# <a name="apijetseek-method"></a><span data-ttu-id="0b029-103">Método API. JetSeek</span><span class="sxs-lookup"><span data-stu-id="0b029-103">Api.JetSeek method</span></span>

<span data-ttu-id="0b029-104">Coloca de forma eficaz un cursor en una entrada de índice que coincide con los criterios de búsqueda especificados por la clave de búsqueda en ese cursor y la desigualdad especificada.</span><span class="sxs-lookup"><span data-stu-id="0b029-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="0b029-105">Una clave de búsqueda se debe haber construido previamente mediante [JetMakeKey (JET_SESID, JET_TABLEID, \[ \] , Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span><span class="sxs-lookup"><span data-stu-id="0b029-105">A search key must have been previously constructed using [JetMakeKey(JET_SESID, JET_TABLEID, \[\], Int32, MakeKeyGrbit)](./api.jetmakekey-method.md).</span></span> <span data-ttu-id="0b029-106">Vea también [TrySeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.tryseek-method.md).</span><span class="sxs-lookup"><span data-stu-id="0b029-106">Also see [TrySeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.tryseek-method.md).</span></span>

<span data-ttu-id="0b029-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b029-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0b029-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0b029-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b029-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b029-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetSeek(sesid, _
    tableid, grbit)
```

``` csharp
public static JET_wrn JetSeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0b029-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b029-110">Parameters</span></span>

  - <span data-ttu-id="0b029-111">sesid</span><span class="sxs-lookup"><span data-stu-id="0b029-111">sesid</span></span>  
    <span data-ttu-id="0b029-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0b029-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0b029-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="0b029-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0b029-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="0b029-114">tableid</span></span>  
    <span data-ttu-id="0b029-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0b029-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0b029-116">Cursor que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="0b029-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="0b029-117">grbit</span><span class="sxs-lookup"><span data-stu-id="0b029-117">grbit</span></span>  
    <span data-ttu-id="0b029-118">Tipo: [Microsoft. ISAM. esent. Interop. SeekGrbit](./seekgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0b029-118">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0b029-119">Opciones de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="0b029-119">Seek options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0b029-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b029-120">Return value</span></span>

<span data-ttu-id="0b029-121">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0b029-121">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="0b029-122">Una advertencia de ESENT.</span><span class="sxs-lookup"><span data-stu-id="0b029-122">An ESENT warning.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0b029-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b029-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b029-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="0b029-124">Reference</span></span>

[<span data-ttu-id="0b029-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="0b029-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0b029-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="0b029-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0b029-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0b029-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
