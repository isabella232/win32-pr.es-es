---
description: 'Más información sobre: clase EsentLinkNotSupportedException'
title: Clase EsentLinkNotSupportedException
TOCTitle: EsentLinkNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlinknotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55102133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a72a8f516e3c3a9c3e2a78f0397442bad9236a6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545614"
---
# <a name="esentlinknotsupportedexception-class"></a><span data-ttu-id="2cdbc-103">Clase EsentLinkNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="2cdbc-103">EsentLinkNotSupportedException class</span></span>

<span data-ttu-id="2cdbc-104">Clase base para JET_err. Excepciones LinkNotSupported.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-104">Base class for JET_err.LinkNotSupported exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2cdbc-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="2cdbc-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2cdbc-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2cdbc-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2cdbc-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2cdbc-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2cdbc-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="2cdbc-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2cdbc-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2cdbc-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2cdbc-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="2cdbc-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2cdbc-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="2cdbc-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="2cdbc-112">Microsoft. ISAM. esent. Interop. EsentLinkNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="2cdbc-112">Microsoft.Isam.Esent.Interop.EsentLinkNotSupportedException</span></span>  

<span data-ttu-id="2cdbc-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2cdbc-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2cdbc-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2cdbc-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2cdbc-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cdbc-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLinkNotSupportedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentLinkNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLinkNotSupportedException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="2cdbc-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="2cdbc-116">Thread safety</span></span>

<span data-ttu-id="2cdbc-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2cdbc-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="2cdbc-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2cdbc-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cdbc-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2cdbc-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="2cdbc-120">Reference</span></span>

[<span data-ttu-id="2cdbc-121">Miembros de EsentLinkNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="2cdbc-121">EsentLinkNotSupportedException members</span></span>](./esentlinknotsupportedexception-members.md)

[<span data-ttu-id="2cdbc-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2cdbc-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
