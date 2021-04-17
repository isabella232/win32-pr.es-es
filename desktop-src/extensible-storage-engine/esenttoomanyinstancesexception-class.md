---
description: 'Más información sobre: clase EsentTooManyInstancesException'
title: Clase EsentTooManyInstancesException
TOCTitle: EsentTooManyInstancesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyinstancesexception(v=EXCHG.10)
ms:contentKeyID: 55103084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ecd20f6a05a17d4bd21623732a4e716e82c9b1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716691"
---
# <a name="esenttoomanyinstancesexception-class"></a><span data-ttu-id="e6c11-103">Clase EsentTooManyInstancesException</span><span class="sxs-lookup"><span data-stu-id="e6c11-103">EsentTooManyInstancesException class</span></span>

<span data-ttu-id="e6c11-104">Clase base para JET_err. Excepciones TooManyInstances.</span><span class="sxs-lookup"><span data-stu-id="e6c11-104">Base class for JET_err.TooManyInstances exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e6c11-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="e6c11-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e6c11-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e6c11-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e6c11-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="e6c11-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e6c11-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="e6c11-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e6c11-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e6c11-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e6c11-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="e6c11-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="e6c11-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="e6c11-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="e6c11-112">Microsoft. ISAM. esent. Interop. EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="e6c11-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="e6c11-113">Microsoft. ISAM. esent. Interop. EsentTooManyInstancesException</span><span class="sxs-lookup"><span data-stu-id="e6c11-113">Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException</span></span>  

<span data-ttu-id="e6c11-114">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6c11-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e6c11-115">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6c11-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6c11-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6c11-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyInstancesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyInstancesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyInstancesException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="e6c11-117">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="e6c11-117">Thread safety</span></span>

<span data-ttu-id="e6c11-118">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="e6c11-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e6c11-119">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="e6c11-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6c11-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6c11-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6c11-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="e6c11-121">Reference</span></span>

[<span data-ttu-id="e6c11-122">Miembros de EsentTooManyInstancesException</span><span class="sxs-lookup"><span data-stu-id="e6c11-122">EsentTooManyInstancesException members</span></span>](./esenttoomanyinstancesexception-members.md)

[<span data-ttu-id="e6c11-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e6c11-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
