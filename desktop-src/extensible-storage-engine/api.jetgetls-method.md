---
description: 'Más información sobre: API. JetGetLS (método)'
title: Método API. JetGetLS
TOCTitle: 'JetGetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS@,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetls(v=EXCHG.10)
ms:contentKeyID: 55100734
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 611f92e21dad83121b4e4a6226838ac9ebce2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275303"
---
# <a name="apijetgetls-method"></a><span data-ttu-id="217d5-103">Método API. JetGetLS</span><span class="sxs-lookup"><span data-stu-id="217d5-103">Api.JetGetLS method</span></span>

<span data-ttu-id="217d5-104">Permite que la aplicación recupere el identificador de contexto conocido como almacenamiento local que está asociado a un cursor o la tabla asociada a ese cursor.</span><span class="sxs-lookup"><span data-stu-id="217d5-104">Enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="217d5-105">Este identificador de contexto se debe haber establecido previamente mediante [JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span><span class="sxs-lookup"><span data-stu-id="217d5-105">This context handle must have been previously set using [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span></span> <span data-ttu-id="217d5-106">JetGetLS también se puede usar para capturar simultáneamente el identificador de contexto actual para un cursor o una tabla y restablecer ese identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="217d5-106">JetGetLS can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="217d5-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="217d5-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="217d5-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="217d5-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="217d5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="217d5-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetGetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetGetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="217d5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="217d5-110">Parameters</span></span>

  - <span data-ttu-id="217d5-111">sesid</span><span class="sxs-lookup"><span data-stu-id="217d5-111">sesid</span></span>  
    <span data-ttu-id="217d5-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="217d5-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="217d5-113">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="217d5-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="217d5-114">TABLEID</span><span class="sxs-lookup"><span data-stu-id="217d5-114">tableid</span></span>  
    <span data-ttu-id="217d5-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="217d5-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="217d5-116">Cursor que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="217d5-116">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="217d5-117">ls</span><span class="sxs-lookup"><span data-stu-id="217d5-117">ls</span></span>  
    <span data-ttu-id="217d5-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="217d5-118">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="217d5-119">Devuelve el identificador de contexto recuperado.</span><span class="sxs-lookup"><span data-stu-id="217d5-119">Returns the retrieved context handle.</span></span>

<!-- end list -->

  - <span data-ttu-id="217d5-120">grbit</span><span class="sxs-lookup"><span data-stu-id="217d5-120">grbit</span></span>  
    <span data-ttu-id="217d5-121">Tipo: [Microsoft. ISAM. esent. Interop. LsGrbit](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="217d5-121">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="217d5-122">Opciones de recuperación.</span><span class="sxs-lookup"><span data-stu-id="217d5-122">Retrieve options.</span></span>

## <a name="see-also"></a><span data-ttu-id="217d5-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="217d5-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="217d5-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="217d5-124">Reference</span></span>

[<span data-ttu-id="217d5-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="217d5-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="217d5-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="217d5-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="217d5-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="217d5-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
