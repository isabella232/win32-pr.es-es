---
description: 'Más información sobre: clase EsentBadColumnIdException'
title: Clase EsentBadColumnIdException
TOCTitle: EsentBadColumnIdException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadColumnIdException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadcolumnidexception(v=EXCHG.10)
ms:contentKeyID: 55101061
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadColumnIdException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadColumnIdException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94b7e898b95130df4a1f7e3a88fa2e450d3b6776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083126"
---
# <a name="esentbadcolumnidexception-class"></a><span data-ttu-id="636ac-103">Clase EsentBadColumnIdException</span><span class="sxs-lookup"><span data-stu-id="636ac-103">EsentBadColumnIdException class</span></span>

<span data-ttu-id="636ac-104">Clase base para JET_err. Excepciones BadColumnId.</span><span class="sxs-lookup"><span data-stu-id="636ac-104">Base class for JET_err.BadColumnId exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="636ac-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="636ac-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="636ac-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="636ac-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="636ac-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="636ac-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="636ac-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="636ac-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="636ac-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="636ac-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="636ac-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="636ac-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="636ac-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="636ac-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="636ac-112">Microsoft. ISAM. esent. Interop. EsentBadColumnIdException</span><span class="sxs-lookup"><span data-stu-id="636ac-112">Microsoft.Isam.Esent.Interop.EsentBadColumnIdException</span></span>  

<span data-ttu-id="636ac-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="636ac-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="636ac-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="636ac-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="636ac-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="636ac-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadColumnIdException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentBadColumnIdException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadColumnIdException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="636ac-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="636ac-116">Thread safety</span></span>

<span data-ttu-id="636ac-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="636ac-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="636ac-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="636ac-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="636ac-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="636ac-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="636ac-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="636ac-120">Reference</span></span>

[<span data-ttu-id="636ac-121">Miembros de EsentBadColumnIdException</span><span class="sxs-lookup"><span data-stu-id="636ac-121">EsentBadColumnIdException members</span></span>](./esentbadcolumnidexception-members.md)

[<span data-ttu-id="636ac-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="636ac-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
