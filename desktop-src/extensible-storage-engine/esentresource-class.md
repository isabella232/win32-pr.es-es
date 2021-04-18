---
description: 'Más información sobre: clase EsentResource'
title: Clase EsentResource
TOCTitle: EsentResource class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource(v=EXCHG.10)
ms:contentKeyID: 55102575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 607fb59d6f9f89c33e685ed411ae9dc95eaa6818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715327"
---
# <a name="esentresource-class"></a><span data-ttu-id="2e5b5-103">Clase EsentResource</span><span class="sxs-lookup"><span data-stu-id="2e5b5-103">EsentResource class</span></span>

<span data-ttu-id="2e5b5-104">Esta es la clase base para todos los objetos de recursos esent.</span><span class="sxs-lookup"><span data-stu-id="2e5b5-104">This is the base class for all esent resource objects.</span></span> <span data-ttu-id="2e5b5-105">Las subclases de esta clase pueden asignar y liberar recursos no administrados.</span><span class="sxs-lookup"><span data-stu-id="2e5b5-105">Subclasses of this class can allocate and release unmanaged resources.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2e5b5-106">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="2e5b5-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="2e5b5-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="2e5b5-107">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="2e5b5-108">Microsoft. ISAM. esent. Interop. EsentResource</span><span class="sxs-lookup"><span data-stu-id="2e5b5-108">Microsoft.Isam.Esent.Interop.EsentResource</span></span>  
    [<span data-ttu-id="2e5b5-109">Microsoft. ISAM. esent. Interop. Session</span><span class="sxs-lookup"><span data-stu-id="2e5b5-109">Microsoft.Isam.Esent.Interop.Session</span></span>](./session-class.md)  
    [<span data-ttu-id="2e5b5-110">Microsoft. ISAM. esent. Interop. Table</span><span class="sxs-lookup"><span data-stu-id="2e5b5-110">Microsoft.Isam.Esent.Interop.Table</span></span>](./table-class.md)  
    [<span data-ttu-id="2e5b5-111">Microsoft. ISAM. esent. Interop. Transaction</span><span class="sxs-lookup"><span data-stu-id="2e5b5-111">Microsoft.Isam.Esent.Interop.Transaction</span></span>](./transaction-class.md)  
    [<span data-ttu-id="2e5b5-112">Microsoft. ISAM. esent. Interop. Update</span><span class="sxs-lookup"><span data-stu-id="2e5b5-112">Microsoft.Isam.Esent.Interop.Update</span></span>](./update-class.md)  
    [<span data-ttu-id="2e5b5-113">Microsoft. ISAM. esent. Interop. Windows8. DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="2e5b5-113">Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback</span></span>](./durablecommitcallback-class.md)  

<span data-ttu-id="2e5b5-114">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2e5b5-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2e5b5-115">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2e5b5-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2e5b5-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e5b5-116">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class EsentResource _
    Implements IDisposable
'Usage
Dim instance As EsentResource
```

``` csharp
public abstract class EsentResource : IDisposable
```

## <a name="thread-safety"></a><span data-ttu-id="2e5b5-117">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="2e5b5-117">Thread safety</span></span>

<span data-ttu-id="2e5b5-118">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="2e5b5-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2e5b5-119">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="2e5b5-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e5b5-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e5b5-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2e5b5-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="2e5b5-121">Reference</span></span>

[<span data-ttu-id="2e5b5-122">Miembros de EsentResource</span><span class="sxs-lookup"><span data-stu-id="2e5b5-122">EsentResource members</span></span>](./esentresource-members.md)

[<span data-ttu-id="2e5b5-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2e5b5-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
