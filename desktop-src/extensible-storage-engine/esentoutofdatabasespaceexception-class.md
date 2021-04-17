---
description: 'Más información sobre: clase EsentOutOfDatabaseSpaceException'
title: Clase EsentOutOfDatabaseSpaceException
TOCTitle: EsentOutOfDatabaseSpaceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofdatabasespaceexception(v=EXCHG.10)
ms:contentKeyID: 55102410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ece3a81fa0687299edba0857b15f4c0abc50e403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666974"
---
# <a name="esentoutofdatabasespaceexception-class"></a><span data-ttu-id="0bec1-103">Clase EsentOutOfDatabaseSpaceException</span><span class="sxs-lookup"><span data-stu-id="0bec1-103">EsentOutOfDatabaseSpaceException class</span></span>

<span data-ttu-id="0bec1-104">Clase base para JET_err. Excepciones OutOfDatabaseSpace.</span><span class="sxs-lookup"><span data-stu-id="0bec1-104">Base class for JET_err.OutOfDatabaseSpace exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0bec1-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="0bec1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0bec1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0bec1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0bec1-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0bec1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0bec1-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0bec1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0bec1-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0bec1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0bec1-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="0bec1-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="0bec1-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="0bec1-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="0bec1-112">Microsoft. ISAM. esent. Interop. EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="0bec1-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="0bec1-113">Microsoft. ISAM. esent. Interop. EsentOutOfDatabaseSpaceException</span><span class="sxs-lookup"><span data-stu-id="0bec1-113">Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException</span></span>  

<span data-ttu-id="0bec1-114">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0bec1-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0bec1-115">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0bec1-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0bec1-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bec1-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfDatabaseSpaceException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentOutOfDatabaseSpaceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfDatabaseSpaceException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="0bec1-117">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="0bec1-117">Thread safety</span></span>

<span data-ttu-id="0bec1-118">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0bec1-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0bec1-119">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0bec1-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0bec1-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bec1-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0bec1-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="0bec1-121">Reference</span></span>

[<span data-ttu-id="0bec1-122">Miembros de EsentOutOfDatabaseSpaceException</span><span class="sxs-lookup"><span data-stu-id="0bec1-122">EsentOutOfDatabaseSpaceException members</span></span>](./esentoutofdatabasespaceexception-members.md)

[<span data-ttu-id="0bec1-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0bec1-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
