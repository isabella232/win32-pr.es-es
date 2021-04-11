---
description: 'Más información sobre: API. TryMoveNext (método)'
title: Método API. TryMoveNext
TOCTitle: 'TryMoveNext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveNext(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovenext(v=EXCHG.10)
ms:contentKeyID: 55100887
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveNext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveNext
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b4b4e1f296e5549ba3823f698cdcb5cc9f9f42a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154032"
---
# <a name="apitrymovenext-method"></a><span data-ttu-id="b6114-103">Método API. TryMoveNext</span><span class="sxs-lookup"><span data-stu-id="b6114-103">Api.TryMoveNext method</span></span>

<span data-ttu-id="b6114-104">Intente moverse al siguiente registro de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b6114-104">Try to move to the next record in the table.</span></span> <span data-ttu-id="b6114-105">Si no hay un registro siguiente, devuelve false, si se produce un error diferente, se produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="b6114-105">If there is not a next record this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="b6114-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b6114-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b6114-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b6114-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b6114-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6114-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMoveNext ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveNext(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveNext(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="b6114-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6114-109">Parameters</span></span>

  - <span data-ttu-id="b6114-110">sesid</span><span class="sxs-lookup"><span data-stu-id="b6114-110">sesid</span></span>  
    <span data-ttu-id="b6114-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6114-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b6114-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b6114-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6114-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="b6114-113">tableid</span></span>  
    <span data-ttu-id="b6114-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6114-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b6114-115">Cursor que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="b6114-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b6114-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6114-116">Return value</span></span>

<span data-ttu-id="b6114-117">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b6114-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b6114-118">True si el movimiento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b6114-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b6114-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6114-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b6114-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="b6114-120">Reference</span></span>

[<span data-ttu-id="b6114-121">Clase de API</span><span class="sxs-lookup"><span data-stu-id="b6114-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b6114-122">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="b6114-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b6114-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b6114-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
