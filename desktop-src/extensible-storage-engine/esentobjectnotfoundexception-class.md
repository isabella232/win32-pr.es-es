---
description: 'Más información sobre: clase EsentObjectNotFoundException'
title: Clase EsentObjectNotFoundException
TOCTitle: EsentObjectNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobjectnotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55102350
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d30eb09898142b25549ff4318059b4a373c31d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275651"
---
# <a name="esentobjectnotfoundexception-class"></a><span data-ttu-id="c49a2-103">Clase EsentObjectNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c49a2-103">EsentObjectNotFoundException class</span></span>

<span data-ttu-id="c49a2-104">Clase base para JET_err. Excepciones ObjectNotFound.</span><span class="sxs-lookup"><span data-stu-id="c49a2-104">Base class for JET_err.ObjectNotFound exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c49a2-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="c49a2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c49a2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c49a2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c49a2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c49a2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c49a2-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c49a2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c49a2-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c49a2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c49a2-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="c49a2-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="c49a2-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="c49a2-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="c49a2-112">Microsoft. ISAM. esent. Interop. EsentObjectNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c49a2-112">Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException</span></span>  

<span data-ttu-id="c49a2-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c49a2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c49a2-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c49a2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c49a2-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c49a2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentObjectNotFoundException _
    Inherits EsentStateException
'Usage
Dim instance As EsentObjectNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentObjectNotFoundException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="c49a2-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="c49a2-116">Thread safety</span></span>

<span data-ttu-id="c49a2-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c49a2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c49a2-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c49a2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c49a2-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c49a2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c49a2-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="c49a2-120">Reference</span></span>

[<span data-ttu-id="c49a2-121">Miembros de EsentObjectNotFoundException</span><span class="sxs-lookup"><span data-stu-id="c49a2-121">EsentObjectNotFoundException members</span></span>](./esentobjectnotfoundexception-members.md)

[<span data-ttu-id="c49a2-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c49a2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
