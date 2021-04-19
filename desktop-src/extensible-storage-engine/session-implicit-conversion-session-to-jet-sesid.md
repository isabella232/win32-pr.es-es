---
description: Más información acerca de la conversión implícita de sesión (sesión a JET_SESID)
title: Conversión implícita de sesión (sesión a JET_SESID)
TOCTitle: Implicit conversion (Session to JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.op_Implicit(Microsoft.Isam.Esent.Interop.Session)~Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104121
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session.op_Implicit
- Microsoft.Isam.Esent.Interop.Session.Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 512bc457a84ad1d1b170ac9d31cb04e36d8a05d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720420"
---
# <a name="session-implicit-conversion-session-to-jet_sesid"></a><span data-ttu-id="d5ed8-103">Conversión implícita de sesión (sesión a JET_SESID)</span><span class="sxs-lookup"><span data-stu-id="d5ed8-103">Session Implicit conversion (Session to JET_SESID)</span></span>

<span data-ttu-id="d5ed8-104">Operador de conversión implícita de una sesión a un JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="d5ed8-104">Implicit conversion operator from a Session to a JET_SESID.</span></span> <span data-ttu-id="d5ed8-105">Esto permite usar una sesión con las API que esperan un JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="d5ed8-105">This allows a Session to be used with APIs which expect a JET_SESID.</span></span>

<span data-ttu-id="d5ed8-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d5ed8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d5ed8-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d5ed8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ed8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5ed8-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    session As Session _
) As JET_SESID
'Usage
Dim input As Session
Dim output As JET_SESID

output = CType(input, JET_SESID)
```

``` csharp
public static implicit operator JET_SESID (
    Session session
)
```

#### <a name="parameters"></a><span data-ttu-id="d5ed8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5ed8-109">Parameters</span></span>

  - <span data-ttu-id="d5ed8-110">hora de sesión</span><span class="sxs-lookup"><span data-stu-id="d5ed8-110">session</span></span>  
    <span data-ttu-id="d5ed8-111">Tipo: [Microsoft. ISAM. esent. Interop. Session](./session-class.md)</span><span class="sxs-lookup"><span data-stu-id="d5ed8-111">Type: [Microsoft.Isam.Esent.Interop.Session](./session-class.md)</span></span>  
    
    <span data-ttu-id="d5ed8-112">La sesión que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="d5ed8-112">The session to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d5ed8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5ed8-113">Return value</span></span>

<span data-ttu-id="d5ed8-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d5ed8-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
<span data-ttu-id="d5ed8-115">JET_SESID de la sesión.</span><span class="sxs-lookup"><span data-stu-id="d5ed8-115">The JET_SESID of the session.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d5ed8-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5ed8-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d5ed8-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="d5ed8-117">Reference</span></span>

[<span data-ttu-id="d5ed8-118">Clase de sesión</span><span class="sxs-lookup"><span data-stu-id="d5ed8-118">Session class</span></span>](./session-class.md)

[<span data-ttu-id="d5ed8-119">Miembros de sesión</span><span class="sxs-lookup"><span data-stu-id="d5ed8-119">Session members</span></span>](./session-members.md)

[<span data-ttu-id="d5ed8-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d5ed8-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
