---
description: 'Más información sobre: clase EsentRecoveryVerifyFailureException'
title: Clase EsentRecoveryVerifyFailureException
TOCTitle: EsentRecoveryVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecoveryverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102574
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad3a052a4d2891a25e5b3ecce11d8f45f89a2292
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677309"
---
# <a name="esentrecoveryverifyfailureexception-class"></a><span data-ttu-id="70db1-103">Clase EsentRecoveryVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="70db1-103">EsentRecoveryVerifyFailureException class</span></span>

<span data-ttu-id="70db1-104">Clase base para JET_err. Excepciones RecoveryVerifyFailure.</span><span class="sxs-lookup"><span data-stu-id="70db1-104">Base class for JET_err.RecoveryVerifyFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="70db1-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="70db1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="70db1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="70db1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="70db1-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="70db1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="70db1-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="70db1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="70db1-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="70db1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="70db1-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="70db1-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="70db1-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="70db1-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="70db1-112">Microsoft. ISAM. esent. Interop. EsentRecoveryVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="70db1-112">Microsoft.Isam.Esent.Interop.EsentRecoveryVerifyFailureException</span></span>  

<span data-ttu-id="70db1-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="70db1-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="70db1-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="70db1-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="70db1-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70db1-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecoveryVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentRecoveryVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecoveryVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="70db1-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="70db1-116">Thread safety</span></span>

<span data-ttu-id="70db1-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="70db1-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="70db1-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="70db1-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="70db1-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="70db1-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="70db1-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="70db1-120">Reference</span></span>

[<span data-ttu-id="70db1-121">Miembros de EsentRecoveryVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="70db1-121">EsentRecoveryVerifyFailureException members</span></span>](./esentrecoveryverifyfailureexception-members.md)

[<span data-ttu-id="70db1-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="70db1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
