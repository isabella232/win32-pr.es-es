---
description: 'Más información sobre: clase EsentTooManyOpenTablesAndCleanupTimedOutException'
title: Clase EsentTooManyOpenTablesAndCleanupTimedOutException
TOCTitle: EsentTooManyOpenTablesAndCleanupTimedOutException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopentablesandcleanuptimedoutexception(v=EXCHG.10)
ms:contentKeyID: 55103109
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ddfcf7f09a98e62b44265c263fd835cace699e8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649267"
---
# <a name="esenttoomanyopentablesandcleanuptimedoutexception-class"></a><span data-ttu-id="bfe32-103">Clase EsentTooManyOpenTablesAndCleanupTimedOutException</span><span class="sxs-lookup"><span data-stu-id="bfe32-103">EsentTooManyOpenTablesAndCleanupTimedOutException class</span></span>

<span data-ttu-id="bfe32-104">Clase base para JET_err. Excepciones TooManyOpenTablesAndCleanupTimedOut.</span><span class="sxs-lookup"><span data-stu-id="bfe32-104">Base class for JET_err.TooManyOpenTablesAndCleanupTimedOut exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="bfe32-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="bfe32-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="bfe32-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="bfe32-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="bfe32-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="bfe32-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="bfe32-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="bfe32-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="bfe32-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="bfe32-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="bfe32-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="bfe32-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="bfe32-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="bfe32-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="bfe32-112">Microsoft. ISAM. esent. Interop. EsentTooManyOpenTablesAndCleanupTimedOutException</span><span class="sxs-lookup"><span data-stu-id="bfe32-112">Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesAndCleanupTimedOutException</span></span>  

<span data-ttu-id="bfe32-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bfe32-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bfe32-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bfe32-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bfe32-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfe32-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenTablesAndCleanupTimedOutException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyOpenTablesAndCleanupTimedOutException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenTablesAndCleanupTimedOutException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="bfe32-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="bfe32-116">Thread safety</span></span>

<span data-ttu-id="bfe32-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="bfe32-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="bfe32-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="bfe32-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="bfe32-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfe32-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bfe32-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="bfe32-120">Reference</span></span>

[<span data-ttu-id="bfe32-121">Miembros de EsentTooManyOpenTablesAndCleanupTimedOutException</span><span class="sxs-lookup"><span data-stu-id="bfe32-121">EsentTooManyOpenTablesAndCleanupTimedOutException members</span></span>](./esenttoomanyopentablesandcleanuptimedoutexception-members.md)

[<span data-ttu-id="bfe32-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="bfe32-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
