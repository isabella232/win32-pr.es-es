---
description: 'Más información sobre: clase de instancia'
title: Clase de instancia
TOCTitle: Instance class
ms:assetid: T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance(v=EXCHG.10)
ms:contentKeyID: 55103260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b717286a9d07b7eb17b87354cbe0896cf182f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811137"
---
# <a name="instance-class"></a><span data-ttu-id="5c822-103">Clase de instancia</span><span class="sxs-lookup"><span data-stu-id="5c822-103">Instance class</span></span>

<span data-ttu-id="5c822-104">Una clase que encapsula una [JET_INSTANCE](./jet-instance-structure.md) en un objeto descartable.</span><span class="sxs-lookup"><span data-stu-id="5c822-104">A class that encapsulates a [JET_INSTANCE](./jet-instance-structure.md) in a disposable object.</span></span> <span data-ttu-id="5c822-105">La instancia debe cerrarse en último lugar y el cierre de la instancia libera todos los demás recursos de la instancia.</span><span class="sxs-lookup"><span data-stu-id="5c822-105">The instance must be closed last and closing the instance releases all other resources for the instance.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5c822-106">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="5c822-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="5c822-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="5c822-107">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5c822-108">System. Runtime. ConstrainedExecution. CriticalFinalizerObject</span><span class="sxs-lookup"><span data-stu-id="5c822-108">System.Runtime.ConstrainedExecution.CriticalFinalizerObject</span></span>](/dotnet/api/system.runtime.constrainedexecution.criticalfinalizerobject)  
    [<span data-ttu-id="5c822-109">System.Runtime.InteropServices.SafeHandle</span><span class="sxs-lookup"><span data-stu-id="5c822-109">System.Runtime.InteropServices.SafeHandle</span></span>](/dotnet/api/system.runtime.interopservices.safehandle)  
      [<span data-ttu-id="5c822-110">Microsoft. Win32. SafeHandle. SafeHandleZeroOrMinusOneIsInvalid</span><span class="sxs-lookup"><span data-stu-id="5c822-110">Microsoft.Win32.SafeHandles.SafeHandleZeroOrMinusOneIsInvalid</span></span>](/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid)  
        <span data-ttu-id="5c822-111">Microsoft. ISAM. esent. Interop. Instance</span><span class="sxs-lookup"><span data-stu-id="5c822-111">Microsoft.Isam.Esent.Interop.Instance</span></span>  

<span data-ttu-id="5c822-112">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5c822-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5c822-113">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5c822-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5c822-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c822-114">Syntax</span></span>

``` vb
'Declaration
Public Class Instance _
    Inherits SafeHandleZeroOrMinusOneIsInvalid
'Usage
Dim instance As Instance
```

``` csharp
public class Instance : SafeHandleZeroOrMinusOneIsInvalid
```

## <a name="thread-safety"></a><span data-ttu-id="5c822-115">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="5c822-115">Thread safety</span></span>

<span data-ttu-id="5c822-116">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="5c822-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5c822-117">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="5c822-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c822-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c822-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5c822-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="5c822-119">Reference</span></span>

[<span data-ttu-id="5c822-120">Miembros de instancia</span><span class="sxs-lookup"><span data-stu-id="5c822-120">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="5c822-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5c822-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
