---
description: 'Más información sobre: API. JetPrepareUpdate (método)'
title: Método API. JetPrepareUpdate
TOCTitle: 'JetPrepareUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_prep)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetprepareupdate(v=EXCHG.10)
ms:contentKeyID: 55100782
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetPrepareUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e8094fef5fcf008dd5f6eb6f2bfd05a0be1bf077
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279083"
---
# <a name="apijetprepareupdate-method"></a><span data-ttu-id="85d82-103">Método API. JetPrepareUpdate</span><span class="sxs-lookup"><span data-stu-id="85d82-103">Api.JetPrepareUpdate method</span></span>

<span data-ttu-id="85d82-104">Preparar un cursor para la actualización.</span><span class="sxs-lookup"><span data-stu-id="85d82-104">Prepare a cursor for update.</span></span>

<span data-ttu-id="85d82-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="85d82-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="85d82-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="85d82-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="85d82-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85d82-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrepareUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    prep As JET_prep _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim prep As JET_prepApi.JetPrepareUpdate(sesid, tableid, _
    prep)
```

``` csharp
public static void JetPrepareUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_prep prep
)
```

#### <a name="parameters"></a><span data-ttu-id="85d82-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85d82-108">Parameters</span></span>

  - <span data-ttu-id="85d82-109">sesid</span><span class="sxs-lookup"><span data-stu-id="85d82-109">sesid</span></span>  
    <span data-ttu-id="85d82-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="85d82-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="85d82-111">La sesión que está iniciando la actualización.</span><span class="sxs-lookup"><span data-stu-id="85d82-111">The session which is starting the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="85d82-112">TABLEID</span><span class="sxs-lookup"><span data-stu-id="85d82-112">tableid</span></span>  
    <span data-ttu-id="85d82-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="85d82-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="85d82-114">Cursor para el que se va a iniciar la actualización.</span><span class="sxs-lookup"><span data-stu-id="85d82-114">The cursor to start the update for.</span></span>

<!-- end list -->

  - <span data-ttu-id="85d82-115">porcentaje</span><span class="sxs-lookup"><span data-stu-id="85d82-115">prep</span></span>  
    <span data-ttu-id="85d82-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_prep](./jet-prep-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="85d82-116">Type: [Microsoft.Isam.Esent.Interop.JET_prep](./jet-prep-enumeration.md)</span></span>  
    
    <span data-ttu-id="85d82-117">El tipo de actualización que se va a preparar.</span><span class="sxs-lookup"><span data-stu-id="85d82-117">The type of update to prepare.</span></span>

## <a name="see-also"></a><span data-ttu-id="85d82-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="85d82-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="85d82-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="85d82-119">Reference</span></span>

[<span data-ttu-id="85d82-120">Clase de API</span><span class="sxs-lookup"><span data-stu-id="85d82-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="85d82-121">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="85d82-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="85d82-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="85d82-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
