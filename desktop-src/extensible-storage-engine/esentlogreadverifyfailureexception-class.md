---
description: 'Más información sobre: clase EsentLogReadVerifyFailureException'
title: Clase EsentLogReadVerifyFailureException
TOCTitle: EsentLogReadVerifyFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogreadverifyfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102142
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 937d3fa0b721b66d072817ba12c2cf8ba97d5cdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717264"
---
# <a name="esentlogreadverifyfailureexception-class"></a><span data-ttu-id="be9ee-103">Clase EsentLogReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="be9ee-103">EsentLogReadVerifyFailureException class</span></span>

<span data-ttu-id="be9ee-104">Clase base para JET_err. Excepciones LogReadVerifyFailure.</span><span class="sxs-lookup"><span data-stu-id="be9ee-104">Base class for JET_err.LogReadVerifyFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="be9ee-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="be9ee-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="be9ee-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="be9ee-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="be9ee-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="be9ee-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="be9ee-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="be9ee-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="be9ee-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="be9ee-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="be9ee-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="be9ee-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="be9ee-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="be9ee-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="be9ee-112">Microsoft. ISAM. esent. Interop. EsentLogReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="be9ee-112">Microsoft.Isam.Esent.Interop.EsentLogReadVerifyFailureException</span></span>  

<span data-ttu-id="be9ee-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="be9ee-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="be9ee-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="be9ee-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="be9ee-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be9ee-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogReadVerifyFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogReadVerifyFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogReadVerifyFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="be9ee-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="be9ee-116">Thread safety</span></span>

<span data-ttu-id="be9ee-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="be9ee-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="be9ee-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="be9ee-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="be9ee-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="be9ee-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="be9ee-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="be9ee-120">Reference</span></span>

[<span data-ttu-id="be9ee-121">Miembros de EsentLogReadVerifyFailureException</span><span class="sxs-lookup"><span data-stu-id="be9ee-121">EsentLogReadVerifyFailureException members</span></span>](./esentlogreadverifyfailureexception-members.md)

[<span data-ttu-id="be9ee-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="be9ee-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
