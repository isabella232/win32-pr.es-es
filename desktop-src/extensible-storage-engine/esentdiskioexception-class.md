---
description: 'Más información sobre: clase EsentDiskIOException'
title: Clase EsentDiskIOException
TOCTitle: EsentDiskIOException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskIOException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskioexception(v=EXCHG.10)
ms:contentKeyID: 55101660
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskIOException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskIOException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9810c7cd54afd9649530c1bea6db93161911efb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002939"
---
# <a name="esentdiskioexception-class"></a><span data-ttu-id="f0d66-103">Clase EsentDiskIOException</span><span class="sxs-lookup"><span data-stu-id="f0d66-103">EsentDiskIOException class</span></span>

<span data-ttu-id="f0d66-104">Clase base para JET_err. Excepciones desmontaje.</span><span class="sxs-lookup"><span data-stu-id="f0d66-104">Base class for JET_err.DiskIO exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f0d66-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="f0d66-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f0d66-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f0d66-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f0d66-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f0d66-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f0d66-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f0d66-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f0d66-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f0d66-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f0d66-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="f0d66-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="f0d66-111">Microsoft. ISAM. esent. Interop. EsentIOException</span><span class="sxs-lookup"><span data-stu-id="f0d66-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
            <span data-ttu-id="f0d66-112">Microsoft. ISAM. esent. Interop. EsentDiskIOException</span><span class="sxs-lookup"><span data-stu-id="f0d66-112">Microsoft.Isam.Esent.Interop.EsentDiskIOException</span></span>  

<span data-ttu-id="f0d66-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f0d66-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f0d66-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f0d66-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f0d66-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0d66-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDiskIOException _
    Inherits EsentIOException
'Usage
Dim instance As EsentDiskIOException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDiskIOException : EsentIOException
```

## <a name="thread-safety"></a><span data-ttu-id="f0d66-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="f0d66-116">Thread safety</span></span>

<span data-ttu-id="f0d66-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f0d66-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f0d66-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f0d66-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0d66-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0d66-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f0d66-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="f0d66-120">Reference</span></span>

[<span data-ttu-id="f0d66-121">Miembros de EsentDiskIOException</span><span class="sxs-lookup"><span data-stu-id="f0d66-121">EsentDiskIOException members</span></span>](./esentdiskioexception-members.md)

[<span data-ttu-id="f0d66-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f0d66-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
