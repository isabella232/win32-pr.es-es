---
description: 'Más información sobre: API. TryMoveLast (método)'
title: Método API. TryMoveLast
TOCTitle: 'TryMoveLast method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryMoveLast(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trymovelast(v=EXCHG.10)
ms:contentKeyID: 55100933
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryMoveLast
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryMoveLast
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ab1e0495d3fbea490f7b1be6cc67e45d97bc89d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155977"
---
# <a name="apitrymovelast-method"></a><span data-ttu-id="f6890-103">Método API. TryMoveLast</span><span class="sxs-lookup"><span data-stu-id="f6890-103">Api.TryMoveLast method</span></span>

<span data-ttu-id="f6890-104">Intente moverse al último registro de la tabla.</span><span class="sxs-lookup"><span data-stu-id="f6890-104">Try to move to the last record in the table.</span></span> <span data-ttu-id="f6890-105">Si la tabla está vacía, devuelve false, si se produce un error diferente, se inicia una excepción.</span><span class="sxs-lookup"><span data-stu-id="f6890-105">If the table is empty this returns false, if a different error is encountered an exception is thrown.</span></span>

<span data-ttu-id="f6890-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6890-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f6890-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6890-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6890-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6890-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryMoveLast ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryMoveLast(sesid, _
    tableid)
```

``` csharp
public static bool TryMoveLast(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="f6890-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6890-109">Parameters</span></span>

  - <span data-ttu-id="f6890-110">sesid</span><span class="sxs-lookup"><span data-stu-id="f6890-110">sesid</span></span>  
    <span data-ttu-id="f6890-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f6890-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f6890-112">La sesión que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="f6890-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f6890-113">TABLEID</span><span class="sxs-lookup"><span data-stu-id="f6890-113">tableid</span></span>  
    <span data-ttu-id="f6890-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f6890-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f6890-115">Cursor que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="f6890-115">The cursor to position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f6890-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6890-116">Return value</span></span>

<span data-ttu-id="f6890-117">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f6890-117">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f6890-118">True si el movimiento se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="f6890-118">True if the move was successful.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6890-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6890-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6890-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="f6890-120">Reference</span></span>

[<span data-ttu-id="f6890-121">Clase de API</span><span class="sxs-lookup"><span data-stu-id="f6890-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f6890-122">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="f6890-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f6890-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f6890-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
