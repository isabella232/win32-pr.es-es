---
description: 'Más información sobre: clase EsentDatabasesNotFromSameSnapshotException'
title: Clase EsentDatabasesNotFromSameSnapshotException
TOCTitle: EsentDatabasesNotFromSameSnapshotException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasesnotfromsamesnapshotexception(v=EXCHG.10)
ms:contentKeyID: 55101443
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6d26ecdab73517d1634bc6beb79dfc1249a2756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648267"
---
# <a name="esentdatabasesnotfromsamesnapshotexception-class"></a><span data-ttu-id="f3b21-103">Clase EsentDatabasesNotFromSameSnapshotException</span><span class="sxs-lookup"><span data-stu-id="f3b21-103">EsentDatabasesNotFromSameSnapshotException class</span></span>

<span data-ttu-id="f3b21-104">Clase base para JET_err. Excepciones DatabasesNotFromSameSnapshot.</span><span class="sxs-lookup"><span data-stu-id="f3b21-104">Base class for JET_err.DatabasesNotFromSameSnapshot exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f3b21-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="f3b21-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f3b21-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f3b21-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f3b21-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f3b21-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f3b21-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f3b21-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f3b21-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f3b21-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f3b21-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="f3b21-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f3b21-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="f3b21-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="f3b21-112">Microsoft. ISAM. esent. Interop. EsentDatabasesNotFromSameSnapshotException</span><span class="sxs-lookup"><span data-stu-id="f3b21-112">Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException</span></span>  

<span data-ttu-id="f3b21-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f3b21-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f3b21-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f3b21-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b21-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3b21-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabasesNotFromSameSnapshotException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabasesNotFromSameSnapshotException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabasesNotFromSameSnapshotException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="f3b21-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="f3b21-116">Thread safety</span></span>

<span data-ttu-id="f3b21-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f3b21-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f3b21-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f3b21-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3b21-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3b21-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f3b21-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="f3b21-120">Reference</span></span>

[<span data-ttu-id="f3b21-121">Miembros de EsentDatabasesNotFromSameSnapshotException</span><span class="sxs-lookup"><span data-stu-id="f3b21-121">EsentDatabasesNotFromSameSnapshotException members</span></span>](./esentdatabasesnotfromsamesnapshotexception-members.md)

[<span data-ttu-id="f3b21-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f3b21-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
