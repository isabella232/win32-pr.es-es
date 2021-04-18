---
description: 'Más información sobre: clase EsentBufferTooSmallException'
title: Clase EsentBufferTooSmallException
TOCTitle: EsentBufferTooSmallException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbuffertoosmallexception(v=EXCHG.10)
ms:contentKeyID: 55101109
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbe7f021bc29895db6678b171027a8b46972c6aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697837"
---
# <a name="esentbuffertoosmallexception-class"></a><span data-ttu-id="13b39-103">Clase EsentBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="13b39-103">EsentBufferTooSmallException class</span></span>

<span data-ttu-id="13b39-104">Clase base para JET_err. Excepciones BufferTooSmall.</span><span class="sxs-lookup"><span data-stu-id="13b39-104">Base class for JET_err.BufferTooSmall exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="13b39-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="13b39-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="13b39-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="13b39-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="13b39-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="13b39-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="13b39-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="13b39-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="13b39-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="13b39-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="13b39-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="13b39-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="13b39-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="13b39-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="13b39-112">Microsoft. ISAM. esent. Interop. EsentBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="13b39-112">Microsoft.Isam.Esent.Interop.EsentBufferTooSmallException</span></span>  

<span data-ttu-id="13b39-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="13b39-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="13b39-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="13b39-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="13b39-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13b39-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBufferTooSmallException _
    Inherits EsentStateException
'Usage
Dim instance As EsentBufferTooSmallException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBufferTooSmallException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="13b39-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="13b39-116">Thread safety</span></span>

<span data-ttu-id="13b39-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="13b39-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="13b39-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="13b39-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="13b39-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="13b39-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="13b39-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="13b39-120">Reference</span></span>

[<span data-ttu-id="13b39-121">Miembros de EsentBufferTooSmallException</span><span class="sxs-lookup"><span data-stu-id="13b39-121">EsentBufferTooSmallException members</span></span>](./esentbuffertoosmallexception-members.md)

[<span data-ttu-id="13b39-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="13b39-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
