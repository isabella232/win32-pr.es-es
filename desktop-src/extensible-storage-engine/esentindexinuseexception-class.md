---
description: 'Más información sobre: clase EsentIndexInUseException'
title: Clase EsentIndexInUseException
TOCTitle: EsentIndexInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindexinuseexception(v=EXCHG.10)
ms:contentKeyID: 55101815
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexInUseException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b9460bcc2d9ca0ce8676c358781c59d881a5ea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705767"
---
# <a name="esentindexinuseexception-class"></a><span data-ttu-id="862d5-103">Clase EsentIndexInUseException</span><span class="sxs-lookup"><span data-stu-id="862d5-103">EsentIndexInUseException class</span></span>

<span data-ttu-id="862d5-104">Clase base para JET_err. Excepciones IndexInUse.</span><span class="sxs-lookup"><span data-stu-id="862d5-104">Base class for JET_err.IndexInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="862d5-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="862d5-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="862d5-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="862d5-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="862d5-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="862d5-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="862d5-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="862d5-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="862d5-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="862d5-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="862d5-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="862d5-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="862d5-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="862d5-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="862d5-112">Microsoft. ISAM. esent. Interop. EsentIndexInUseException</span><span class="sxs-lookup"><span data-stu-id="862d5-112">Microsoft.Isam.Esent.Interop.EsentIndexInUseException</span></span>  

<span data-ttu-id="862d5-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="862d5-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="862d5-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="862d5-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="862d5-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="862d5-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexInUseException _
    Inherits EsentStateException
'Usage
Dim instance As EsentIndexInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexInUseException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="862d5-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="862d5-116">Thread safety</span></span>

<span data-ttu-id="862d5-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="862d5-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="862d5-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="862d5-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="862d5-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="862d5-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="862d5-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="862d5-120">Reference</span></span>

[<span data-ttu-id="862d5-121">Miembros de EsentIndexInUseException</span><span class="sxs-lookup"><span data-stu-id="862d5-121">EsentIndexInUseException members</span></span>](./esentindexinuseexception-members.md)

[<span data-ttu-id="862d5-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="862d5-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
