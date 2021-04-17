---
description: 'Más información sobre: clase EsentPageSizeMismatchException'
title: Clase EsentPageSizeMismatchException
TOCTitle: EsentPageSizeMismatchException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpagesizemismatchexception(v=EXCHG.10)
ms:contentKeyID: 55102466
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c0573603fae445e1e5ae9d9768c3a0ffcf38f283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678045"
---
# <a name="esentpagesizemismatchexception-class"></a><span data-ttu-id="5c13e-103">Clase EsentPageSizeMismatchException</span><span class="sxs-lookup"><span data-stu-id="5c13e-103">EsentPageSizeMismatchException class</span></span>

<span data-ttu-id="5c13e-104">Clase base para JET_err. Excepciones PageSizeMismatch.</span><span class="sxs-lookup"><span data-stu-id="5c13e-104">Base class for JET_err.PageSizeMismatch exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5c13e-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="5c13e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5c13e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5c13e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5c13e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="5c13e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5c13e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="5c13e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5c13e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="5c13e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5c13e-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="5c13e-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="5c13e-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="5c13e-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="5c13e-112">Microsoft. ISAM. esent. Interop. EsentPageSizeMismatchException</span><span class="sxs-lookup"><span data-stu-id="5c13e-112">Microsoft.Isam.Esent.Interop.EsentPageSizeMismatchException</span></span>  

<span data-ttu-id="5c13e-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5c13e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5c13e-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5c13e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5c13e-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c13e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPageSizeMismatchException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentPageSizeMismatchException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPageSizeMismatchException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="5c13e-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="5c13e-116">Thread safety</span></span>

<span data-ttu-id="5c13e-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="5c13e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5c13e-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="5c13e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c13e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c13e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5c13e-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="5c13e-120">Reference</span></span>

[<span data-ttu-id="5c13e-121">Miembros de EsentPageSizeMismatchException</span><span class="sxs-lookup"><span data-stu-id="5c13e-121">EsentPageSizeMismatchException members</span></span>](./esentpagesizemismatchexception-members.md)

[<span data-ttu-id="5c13e-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5c13e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
