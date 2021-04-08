---
description: 'Más información sobre: clase EsentTaggedNotNULLException'
title: Clase EsentTaggedNotNULLException
TOCTitle: EsentTaggedNotNULLException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTaggedNotNULLException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttaggednotnullexception(v=EXCHG.10)
ms:contentKeyID: 55103018
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTaggedNotNULLException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTaggedNotNULLException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf1d64e769bc2b1c9d26300c92d25a5df06ccf4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002423"
---
# <a name="esenttaggednotnullexception-class"></a><span data-ttu-id="4670a-103">Clase EsentTaggedNotNULLException</span><span class="sxs-lookup"><span data-stu-id="4670a-103">EsentTaggedNotNULLException class</span></span>

<span data-ttu-id="4670a-104">Clase base para JET_err. Excepciones TaggedNotNULL.</span><span class="sxs-lookup"><span data-stu-id="4670a-104">Base class for JET_err.TaggedNotNULL exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4670a-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="4670a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4670a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4670a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4670a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4670a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4670a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="4670a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4670a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="4670a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4670a-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="4670a-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4670a-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="4670a-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="4670a-112">Microsoft. ISAM. esent. Interop. EsentTaggedNotNULLException</span><span class="sxs-lookup"><span data-stu-id="4670a-112">Microsoft.Isam.Esent.Interop.EsentTaggedNotNULLException</span></span>  

<span data-ttu-id="4670a-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4670a-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4670a-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4670a-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4670a-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4670a-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTaggedNotNULLException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentTaggedNotNULLException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTaggedNotNULLException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="4670a-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="4670a-116">Thread safety</span></span>

<span data-ttu-id="4670a-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4670a-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4670a-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4670a-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4670a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4670a-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4670a-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="4670a-120">Reference</span></span>

[<span data-ttu-id="4670a-121">Miembros de EsentTaggedNotNULLException</span><span class="sxs-lookup"><span data-stu-id="4670a-121">EsentTaggedNotNULLException members</span></span>](./esenttaggednotnullexception-members.md)

[<span data-ttu-id="4670a-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4670a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
