---
description: 'Más información sobre: API. JetSetLS (método)'
title: Método API. JetSetLS
TOCTitle: 'JetSetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetls(v=EXCHG.10)
ms:contentKeyID: 55100808
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetLS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d11d0790bb1d9340c427fd1b836d927527c6ca63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278544"
---
# <a name="apijetsetls-method"></a><span data-ttu-id="92014-103">Método API. JetSetLS</span><span class="sxs-lookup"><span data-stu-id="92014-103">Api.JetSetLS method</span></span>

<span data-ttu-id="92014-104">Permite a la aplicación asociar un identificador de contexto conocido como almacenamiento local con un cursor o la tabla asociada a ese cursor.</span><span class="sxs-lookup"><span data-stu-id="92014-104">Enables the application to associate a context handle known as Local Storage with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="92014-105">La aplicación puede usar este identificador de contexto para almacenar datos auxiliares que están asociados a un cursor o una tabla.</span><span class="sxs-lookup"><span data-stu-id="92014-105">This context handle can be used by the application to store auxiliary data that is associated with a cursor or table.</span></span> <span data-ttu-id="92014-106">Posteriormente, la aplicación recibe una notificación mediante una devolución de llamada en tiempo de ejecución cuando se debe liberar el identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="92014-106">The application is later notified using a runtime callback when the context handle must be released.</span></span> <span data-ttu-id="92014-107">Esto hace posible asociar el estado asignado dinámicamente a un cursor o una tabla.</span><span class="sxs-lookup"><span data-stu-id="92014-107">This makes it possible to associate dynamically allocated state with a cursor or table.</span></span>

<span data-ttu-id="92014-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="92014-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="92014-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="92014-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="92014-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92014-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetSetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetSetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="92014-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92014-111">Parameters</span></span>

  - <span data-ttu-id="92014-112">sesid</span><span class="sxs-lookup"><span data-stu-id="92014-112">sesid</span></span>  
    <span data-ttu-id="92014-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="92014-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="92014-114">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="92014-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="92014-115">TABLEID</span><span class="sxs-lookup"><span data-stu-id="92014-115">tableid</span></span>  
    <span data-ttu-id="92014-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="92014-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="92014-117">Cursor que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="92014-117">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="92014-118">ls</span><span class="sxs-lookup"><span data-stu-id="92014-118">ls</span></span>  
    <span data-ttu-id="92014-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="92014-119">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="92014-120">Identificador de contexto que se va a asociar a la sesión o al cursor.</span><span class="sxs-lookup"><span data-stu-id="92014-120">The context handle to be associated with the session or cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="92014-121">grbit</span><span class="sxs-lookup"><span data-stu-id="92014-121">grbit</span></span>  
    <span data-ttu-id="92014-122">Tipo: [Microsoft. ISAM. esent. Interop. LsGrbit](./lsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="92014-122">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="92014-123">Opciones set.</span><span class="sxs-lookup"><span data-stu-id="92014-123">Set options.</span></span>

## <a name="see-also"></a><span data-ttu-id="92014-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="92014-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="92014-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="92014-125">Reference</span></span>

[<span data-ttu-id="92014-126">Clase de API</span><span class="sxs-lookup"><span data-stu-id="92014-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="92014-127">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="92014-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="92014-128">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="92014-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
