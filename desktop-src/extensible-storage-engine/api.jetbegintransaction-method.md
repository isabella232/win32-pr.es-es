---
description: 'Más información sobre: API. JetBeginTransaction (método)'
title: Método API. JetBeginTransaction
TOCTitle: 'JetBeginTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction(v=EXCHG.10)
ms:contentKeyID: 55107225
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b8812df332734ee109ea52820346e433e747751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715057"
---
# <a name="apijetbegintransaction-method"></a><span data-ttu-id="9aba6-103">Método API. JetBeginTransaction</span><span class="sxs-lookup"><span data-stu-id="9aba6-103">Api.JetBeginTransaction method</span></span>

<span data-ttu-id="9aba6-104">Hace que una sesión escriba una transacción o cree un nuevo punto de retorno en una transacción existente.</span><span class="sxs-lookup"><span data-stu-id="9aba6-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="9aba6-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9aba6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9aba6-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9aba6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9aba6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9aba6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetBeginTransaction(sesid)
```

``` csharp
public static void JetBeginTransaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="9aba6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9aba6-108">Parameters</span></span>

  - <span data-ttu-id="9aba6-109">sesid</span><span class="sxs-lookup"><span data-stu-id="9aba6-109">sesid</span></span>  
    <span data-ttu-id="9aba6-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9aba6-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9aba6-111">Sesión para la que se va a iniciar la transacción.</span><span class="sxs-lookup"><span data-stu-id="9aba6-111">The session to begin the transaction for.</span></span>

## <a name="see-also"></a><span data-ttu-id="9aba6-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="9aba6-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9aba6-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="9aba6-113">Reference</span></span>

[<span data-ttu-id="9aba6-114">Clase de API</span><span class="sxs-lookup"><span data-stu-id="9aba6-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9aba6-115">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="9aba6-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9aba6-116">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9aba6-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
