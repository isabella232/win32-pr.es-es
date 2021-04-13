---
description: 'Más información sobre: clase EsentTooManySortsException'
title: Clase EsentTooManySortsException
TOCTitle: EsentTooManySortsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManySortsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanysortsexception(v=EXCHG.10)
ms:contentKeyID: 55103099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManySortsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManySortsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9048d2c7c65906ba6f093f21c604f25adfcf16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360487"
---
# <a name="esenttoomanysortsexception-class"></a><span data-ttu-id="51bac-103">Clase EsentTooManySortsException</span><span class="sxs-lookup"><span data-stu-id="51bac-103">EsentTooManySortsException class</span></span>

<span data-ttu-id="51bac-104">Clase base para JET_err. Excepciones TooManySorts.</span><span class="sxs-lookup"><span data-stu-id="51bac-104">Base class for JET_err.TooManySorts exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="51bac-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="51bac-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="51bac-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="51bac-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="51bac-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="51bac-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="51bac-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="51bac-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="51bac-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="51bac-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="51bac-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="51bac-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="51bac-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="51bac-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="51bac-112">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="51bac-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="51bac-113">Microsoft. ISAM. esent. Interop. EsentTooManySortsException</span><span class="sxs-lookup"><span data-stu-id="51bac-113">Microsoft.Isam.Esent.Interop.EsentTooManySortsException</span></span>  

<span data-ttu-id="51bac-114">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="51bac-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="51bac-115">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="51bac-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="51bac-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51bac-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManySortsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManySortsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManySortsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="51bac-117">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="51bac-117">Thread safety</span></span>

<span data-ttu-id="51bac-118">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="51bac-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="51bac-119">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="51bac-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="51bac-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="51bac-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="51bac-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="51bac-121">Reference</span></span>

[<span data-ttu-id="51bac-122">Miembros de EsentTooManySortsException</span><span class="sxs-lookup"><span data-stu-id="51bac-122">EsentTooManySortsException members</span></span>](./esenttoomanysortsexception-members.md)

[<span data-ttu-id="51bac-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="51bac-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
