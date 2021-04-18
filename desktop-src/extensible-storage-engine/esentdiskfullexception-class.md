---
description: 'Más información sobre: clase EsentDiskFullException'
title: Clase EsentDiskFullException
TOCTitle: EsentDiskFullException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskFullException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskfullexception(v=EXCHG.10)
ms:contentKeyID: 55101513
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskFullException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskFullException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28c3fb4fa06a6526cf06d0f4822ce3dcb835bad6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361505"
---
# <a name="esentdiskfullexception-class"></a><span data-ttu-id="c54c1-103">Clase EsentDiskFullException</span><span class="sxs-lookup"><span data-stu-id="c54c1-103">EsentDiskFullException class</span></span>

<span data-ttu-id="c54c1-104">Clase base para JET_err. Excepciones DiskFull.</span><span class="sxs-lookup"><span data-stu-id="c54c1-104">Base class for JET_err.DiskFull exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c54c1-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="c54c1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c54c1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c54c1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c54c1-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c54c1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c54c1-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c54c1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c54c1-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c54c1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c54c1-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c54c1-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="c54c1-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="c54c1-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="c54c1-112">Microsoft. ISAM. esent. Interop. EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="c54c1-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
              <span data-ttu-id="c54c1-113">Microsoft. ISAM. esent. Interop. EsentDiskFullException</span><span class="sxs-lookup"><span data-stu-id="c54c1-113">Microsoft.Isam.Esent.Interop.EsentDiskFullException</span></span>  

<span data-ttu-id="c54c1-114">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c54c1-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c54c1-115">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c54c1-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c54c1-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c54c1-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDiskFullException _
    Inherits EsentDiskException
'Usage
Dim instance As EsentDiskFullException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDiskFullException : EsentDiskException
```

## <a name="thread-safety"></a><span data-ttu-id="c54c1-117">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="c54c1-117">Thread safety</span></span>

<span data-ttu-id="c54c1-118">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c54c1-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c54c1-119">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c54c1-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c54c1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c54c1-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c54c1-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="c54c1-121">Reference</span></span>

[<span data-ttu-id="c54c1-122">Miembros de EsentDiskFullException</span><span class="sxs-lookup"><span data-stu-id="c54c1-122">EsentDiskFullException members</span></span>](./esentdiskfullexception-members.md)

[<span data-ttu-id="c54c1-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c54c1-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
