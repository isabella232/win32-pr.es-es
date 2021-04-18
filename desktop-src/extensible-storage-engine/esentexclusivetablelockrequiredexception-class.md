---
description: 'Más información sobre: clase EsentExclusiveTableLockRequiredException'
title: Clase EsentExclusiveTableLockRequiredException
TOCTitle: EsentExclusiveTableLockRequiredException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentexclusivetablelockrequiredexception(v=EXCHG.10)
ms:contentKeyID: 55101593
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c167ab3910b3ba3ce69bc4f946ba7d315256b17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706600"
---
# <a name="esentexclusivetablelockrequiredexception-class"></a><span data-ttu-id="0f092-103">Clase EsentExclusiveTableLockRequiredException</span><span class="sxs-lookup"><span data-stu-id="0f092-103">EsentExclusiveTableLockRequiredException class</span></span>

<span data-ttu-id="0f092-104">Clase base para JET_err. Excepciones ExclusiveTableLockRequired.</span><span class="sxs-lookup"><span data-stu-id="0f092-104">Base class for JET_err.ExclusiveTableLockRequired exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0f092-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="0f092-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0f092-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0f092-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0f092-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0f092-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0f092-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0f092-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0f092-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0f092-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0f092-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="0f092-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="0f092-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="0f092-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="0f092-112">Microsoft. ISAM. esent. Interop. EsentExclusiveTableLockRequiredException</span><span class="sxs-lookup"><span data-stu-id="0f092-112">Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException</span></span>  

<span data-ttu-id="0f092-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0f092-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0f092-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0f092-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0f092-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f092-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentExclusiveTableLockRequiredException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentExclusiveTableLockRequiredException
```

``` csharp
[SerializableAttribute]
public sealed class EsentExclusiveTableLockRequiredException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="0f092-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="0f092-116">Thread safety</span></span>

<span data-ttu-id="0f092-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0f092-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0f092-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0f092-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f092-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f092-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0f092-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="0f092-120">Reference</span></span>

[<span data-ttu-id="0f092-121">Miembros de EsentExclusiveTableLockRequiredException</span><span class="sxs-lookup"><span data-stu-id="0f092-121">EsentExclusiveTableLockRequiredException members</span></span>](./esentexclusivetablelockrequiredexception-members.md)

[<span data-ttu-id="0f092-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0f092-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
