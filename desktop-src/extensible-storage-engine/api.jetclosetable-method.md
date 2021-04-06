---
description: 'Más información sobre: API. JetCloseTable (método)'
title: Método API. JetCloseTable
TOCTitle: 'JetCloseTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosetable(v=EXCHG.10)
ms:contentKeyID: 55100664
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fee4ad7d7accf71bd4c3439f954ee36badd2ea20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001025"
---
# <a name="apijetclosetable-method"></a><span data-ttu-id="f9cf1-103">Método API. JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="f9cf1-103">Api.JetCloseTable method</span></span>

<span data-ttu-id="f9cf1-104">Cierre una tabla abierta.</span><span class="sxs-lookup"><span data-stu-id="f9cf1-104">Close an open table.</span></span>

<span data-ttu-id="f9cf1-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f9cf1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f9cf1-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f9cf1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f9cf1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9cf1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseTable ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetCloseTable(sesid, tableid)
```

``` csharp
public static void JetCloseTable(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="f9cf1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9cf1-108">Parameters</span></span>

  - <span data-ttu-id="f9cf1-109">sesid</span><span class="sxs-lookup"><span data-stu-id="f9cf1-109">sesid</span></span>  
    <span data-ttu-id="f9cf1-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f9cf1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f9cf1-111">La sesión que abrió la tabla.</span><span class="sxs-lookup"><span data-stu-id="f9cf1-111">The session which opened the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="f9cf1-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="f9cf1-112">tableid</span></span>  
    <span data-ttu-id="f9cf1-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f9cf1-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f9cf1-114">Tabla que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="f9cf1-114">The table to close.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9cf1-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9cf1-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f9cf1-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="f9cf1-116">Reference</span></span>

[<span data-ttu-id="f9cf1-117">Clase de API</span><span class="sxs-lookup"><span data-stu-id="f9cf1-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f9cf1-118">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="f9cf1-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f9cf1-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f9cf1-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
