---
description: 'Más información sobre: clase EsentTooManyMempoolEntriesException'
title: Clase EsentTooManyMempoolEntriesException
TOCTitle: EsentTooManyMempoolEntriesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanymempoolentriesexception(v=EXCHG.10)
ms:contentKeyID: 55103097
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 454abe6d19fedb2f318696b80d166f181e19fb0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688398"
---
# <a name="esenttoomanymempoolentriesexception-class"></a><span data-ttu-id="8cf8e-103">Clase EsentTooManyMempoolEntriesException</span><span class="sxs-lookup"><span data-stu-id="8cf8e-103">EsentTooManyMempoolEntriesException class</span></span>

<span data-ttu-id="8cf8e-104">Clase base para JET_err. Excepciones TooManyMempoolEntries.</span><span class="sxs-lookup"><span data-stu-id="8cf8e-104">Base class for JET_err.TooManyMempoolEntries exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8cf8e-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="8cf8e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8cf8e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8cf8e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8cf8e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="8cf8e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8cf8e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="8cf8e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8cf8e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8cf8e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8cf8e-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="8cf8e-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="8cf8e-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="8cf8e-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="8cf8e-112">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="8cf8e-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="8cf8e-113">Microsoft. ISAM. esent. Interop. EsentTooManyMempoolEntriesException</span><span class="sxs-lookup"><span data-stu-id="8cf8e-113">Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException</span></span>  

<span data-ttu-id="8cf8e-114">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8cf8e-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8cf8e-115">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8cf8e-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf8e-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cf8e-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyMempoolEntriesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManyMempoolEntriesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyMempoolEntriesException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="8cf8e-117">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="8cf8e-117">Thread safety</span></span>

<span data-ttu-id="8cf8e-118">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="8cf8e-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8cf8e-119">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="8cf8e-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cf8e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cf8e-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8cf8e-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="8cf8e-121">Reference</span></span>

[<span data-ttu-id="8cf8e-122">Miembros de EsentTooManyMempoolEntriesException</span><span class="sxs-lookup"><span data-stu-id="8cf8e-122">EsentTooManyMempoolEntriesException members</span></span>](./esenttoomanymempoolentriesexception-members.md)

[<span data-ttu-id="8cf8e-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8cf8e-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
