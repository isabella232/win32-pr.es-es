---
description: 'Más información sobre: API. JetEndSession (método)'
title: Método API. JetEndSession
TOCTitle: 'JetEndSession method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndSession(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.EndSessionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendsession(v=EXCHG.10)
ms:contentKeyID: 55100690
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndSession
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10412f6b01b14d63557bf024d65975c271bbe31b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540859"
---
# <a name="apijetendsession-method"></a><span data-ttu-id="1a08d-103">Método API. JetEndSession</span><span class="sxs-lookup"><span data-stu-id="1a08d-103">Api.JetEndSession method</span></span>

<span data-ttu-id="1a08d-104">Finaliza una sesión.</span><span class="sxs-lookup"><span data-stu-id="1a08d-104">Ends a session.</span></span>

<span data-ttu-id="1a08d-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1a08d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1a08d-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1a08d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1a08d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a08d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndSession ( _
    sesid As JET_SESID, _
    grbit As EndSessionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As EndSessionGrbitApi.JetEndSession(sesid, grbit)
```

``` csharp
public static void JetEndSession(
    JET_SESID sesid,
    EndSessionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1a08d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a08d-108">Parameters</span></span>

  - <span data-ttu-id="1a08d-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1a08d-109">sesid</span></span>  
    <span data-ttu-id="1a08d-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1a08d-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1a08d-111">La sesión que se va a finalizar.</span><span class="sxs-lookup"><span data-stu-id="1a08d-111">The session to end.</span></span>

<!-- end list -->

  - <span data-ttu-id="1a08d-112">grbit</span><span class="sxs-lookup"><span data-stu-id="1a08d-112">grbit</span></span>  
    <span data-ttu-id="1a08d-113">Tipo: [Microsoft. ISAM. esent. Interop. EndSessionGrbit](./endsessiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1a08d-113">Type: [Microsoft.Isam.Esent.Interop.EndSessionGrbit](./endsessiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1a08d-114">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1a08d-114">This parameter is not used.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a08d-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a08d-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1a08d-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="1a08d-116">Reference</span></span>

[<span data-ttu-id="1a08d-117">Clase de API</span><span class="sxs-lookup"><span data-stu-id="1a08d-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1a08d-118">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="1a08d-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1a08d-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1a08d-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
