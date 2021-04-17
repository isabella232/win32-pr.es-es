---
description: 'Más información sobre: clase EsentOutOfFileHandlesException'
title: Clase EsentOutOfFileHandlesException
TOCTitle: EsentOutOfFileHandlesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutoffilehandlesexception(v=EXCHG.10)
ms:contentKeyID: 55102419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24d8dec9de0cb4149835766222348dc037f54c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716845"
---
# <a name="esentoutoffilehandlesexception-class"></a><span data-ttu-id="169d7-103">Clase EsentOutOfFileHandlesException</span><span class="sxs-lookup"><span data-stu-id="169d7-103">EsentOutOfFileHandlesException class</span></span>

<span data-ttu-id="169d7-104">Clase base para JET_err. Excepciones OutOfFileHandles.</span><span class="sxs-lookup"><span data-stu-id="169d7-104">Base class for JET_err.OutOfFileHandles exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="169d7-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="169d7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="169d7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="169d7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="169d7-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="169d7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="169d7-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="169d7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="169d7-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="169d7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="169d7-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="169d7-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="169d7-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="169d7-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="169d7-112">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="169d7-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="169d7-113">Microsoft. ISAM. esent. Interop. EsentOutOfFileHandlesException</span><span class="sxs-lookup"><span data-stu-id="169d7-113">Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException</span></span>  

<span data-ttu-id="169d7-114">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="169d7-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="169d7-115">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="169d7-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="169d7-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="169d7-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfFileHandlesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfFileHandlesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfFileHandlesException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="169d7-117">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="169d7-117">Thread safety</span></span>

<span data-ttu-id="169d7-118">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="169d7-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="169d7-119">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="169d7-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="169d7-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="169d7-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="169d7-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="169d7-121">Reference</span></span>

[<span data-ttu-id="169d7-122">Miembros de EsentOutOfFileHandlesException</span><span class="sxs-lookup"><span data-stu-id="169d7-122">EsentOutOfFileHandlesException members</span></span>](./esentoutoffilehandlesexception-members.md)

[<span data-ttu-id="169d7-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="169d7-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
