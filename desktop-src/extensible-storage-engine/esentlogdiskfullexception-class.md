---
description: 'Más información sobre: clase EsentLogDiskFullException'
title: Clase EsentLogDiskFullException
TOCTitle: EsentLogDiskFullException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogdiskfullexception(v=EXCHG.10)
ms:contentKeyID: 55102101
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a237a8d21aab32114708a5cb59545ed827e05bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360797"
---
# <a name="esentlogdiskfullexception-class"></a><span data-ttu-id="4ad14-103">Clase EsentLogDiskFullException</span><span class="sxs-lookup"><span data-stu-id="4ad14-103">EsentLogDiskFullException class</span></span>

<span data-ttu-id="4ad14-104">Clase base para JET_err. Excepciones LogDiskFull.</span><span class="sxs-lookup"><span data-stu-id="4ad14-104">Base class for JET_err.LogDiskFull exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4ad14-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="4ad14-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4ad14-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4ad14-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4ad14-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4ad14-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4ad14-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="4ad14-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4ad14-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="4ad14-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4ad14-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="4ad14-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="4ad14-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="4ad14-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="4ad14-112">Microsoft. ISAM. esent. Interop. EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="4ad14-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
              <span data-ttu-id="4ad14-113">Microsoft. ISAM. esent. Interop. EsentLogDiskFullException</span><span class="sxs-lookup"><span data-stu-id="4ad14-113">Microsoft.Isam.Esent.Interop.EsentLogDiskFullException</span></span>  

<span data-ttu-id="4ad14-114">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ad14-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ad14-115">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4ad14-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad14-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ad14-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogDiskFullException _
    Inherits EsentDiskException
'Usage
Dim instance As EsentLogDiskFullException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogDiskFullException : EsentDiskException
```

## <a name="thread-safety"></a><span data-ttu-id="4ad14-117">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="4ad14-117">Thread safety</span></span>

<span data-ttu-id="4ad14-118">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4ad14-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4ad14-119">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4ad14-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ad14-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ad14-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ad14-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="4ad14-121">Reference</span></span>

[<span data-ttu-id="4ad14-122">Miembros de EsentLogDiskFullException</span><span class="sxs-lookup"><span data-stu-id="4ad14-122">EsentLogDiskFullException members</span></span>](./esentlogdiskfullexception-members.md)

[<span data-ttu-id="4ad14-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4ad14-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
