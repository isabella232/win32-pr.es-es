---
description: 'Más información sobre: API. TryMovePrevious (método)'
title: Método API. TryMovePrevious
TOCTitle: 'TryMovePrevious method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMovePrevious(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymoveprevious(v=EXCHG.10)
ms:contentKeyID: 55100940
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMovePrevious
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMovePrevious
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe512ac4443f670ac73964a422bd9606d903055a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648325"
---
# <a name="apitrymoveprevious-method"></a><span data-ttu-id="69083-103">Método API. TryMovePrevious</span><span class="sxs-lookup"><span data-stu-id="69083-103">Api.TryMovePrevious method</span></span>

<span data-ttu-id="69083-104">Intente moverse al registro anterior de la tabla.</span><span class="sxs-lookup"><span data-stu-id="69083-104">Try to move to the previous record in the table.</span></span> <span data-ttu-id="69083-105">Si no hay un registro anterior, devolverá FALSE si se produce un error diferente al producirse una excepción.</span><span class="sxs-lookup"><span data-stu-id="69083-105">If there is not a previous record this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="69083-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69083-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69083-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69083-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69083-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69083-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMovePrevious ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMovePrevious(sesid, _
    tableid)
```

``` csharp
public static bool TryMovePrevious(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="69083-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69083-109">Parameters</span></span>

  - <span data-ttu-id="69083-110">sesid</span><span class="sxs-lookup"><span data-stu-id="69083-110">sesid</span></span>  
    <span data-ttu-id="69083-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69083-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="69083-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="69083-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="69083-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="69083-113">tableid</span></span>  
    <span data-ttu-id="69083-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69083-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="69083-115">Cursor que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="69083-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="69083-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69083-116">Return value</span></span>

<span data-ttu-id="69083-117">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="69083-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="69083-118">True si el movimiento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="69083-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="69083-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="69083-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69083-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="69083-120">Reference</span></span>

[<span data-ttu-id="69083-121">Clase de API</span><span class="sxs-lookup"><span data-stu-id="69083-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="69083-122">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="69083-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="69083-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="69083-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
