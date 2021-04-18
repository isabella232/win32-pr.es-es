---
description: 'Más información sobre: clase EsentQuotaException'
title: Clase EsentQuotaException
TOCTitle: EsentQuotaException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentQuotaException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102495
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53b108a4d55553788a6c2d316f93f4f8efc76035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707059"
---
# <a name="esentquotaexception-class"></a><span data-ttu-id="c3eee-103">Clase EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="c3eee-103">EsentQuotaException class</span></span>

<span data-ttu-id="c3eee-104">Clase base para las excepciones de cuota.</span><span class="sxs-lookup"><span data-stu-id="c3eee-104">Base class for Quota exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c3eee-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="c3eee-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c3eee-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c3eee-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c3eee-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="c3eee-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c3eee-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c3eee-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c3eee-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c3eee-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c3eee-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c3eee-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="c3eee-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="c3eee-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="c3eee-112">Microsoft. ISAM. esent. Interop. EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="c3eee-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>  
              [<span data-ttu-id="c3eee-113">Microsoft. ISAM. esent. Interop. EsentOutOfDatabaseSpaceException</span><span class="sxs-lookup"><span data-stu-id="c3eee-113">Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException</span></span>](./esentoutofdatabasespaceexception-class.md)  
              [<span data-ttu-id="c3eee-114">Microsoft. ISAM. esent. Interop. EsentTooManyInstancesException</span><span class="sxs-lookup"><span data-stu-id="c3eee-114">Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException</span></span>](./esenttoomanyinstancesexception-class.md)  
              [<span data-ttu-id="c3eee-115">Microsoft. ISAM. esent. Interop. EsentTooManyOpenTablesException</span><span class="sxs-lookup"><span data-stu-id="c3eee-115">Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException</span></span>](./esenttoomanyopentablesexception-class.md)  
              [<span data-ttu-id="c3eee-116">Microsoft. ISAM. esent. Interop. EsentVersionStoreOutOfMemoryException</span><span class="sxs-lookup"><span data-stu-id="c3eee-116">Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException</span></span>](./esentversionstoreoutofmemoryexception-class.md)  

<span data-ttu-id="c3eee-117">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3eee-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c3eee-118">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c3eee-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3eee-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3eee-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentQuotaException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentQuotaException
```

``` csharp
[SerializableAttribute]
public abstract class EsentQuotaException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="c3eee-120">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="c3eee-120">Thread safety</span></span>

<span data-ttu-id="c3eee-121">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c3eee-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c3eee-122">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="c3eee-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3eee-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3eee-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3eee-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="c3eee-124">Reference</span></span>

[<span data-ttu-id="c3eee-125">Miembros de EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="c3eee-125">EsentQuotaException members</span></span>](./esentquotaexception-members.md)

[<span data-ttu-id="c3eee-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c3eee-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
