---
description: 'Más información sobre: clase EsentDataHasChangedException'
title: Clase EsentDataHasChangedException
TOCTitle: EsentDataHasChangedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDataHasChangedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatahaschangedexception(v=EXCHG.10)
ms:contentKeyID: 55101459
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDataHasChangedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataHasChangedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 003045a1aec3cf299fc24f45491424e167a18e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812278"
---
# <a name="esentdatahaschangedexception-class"></a><span data-ttu-id="454fa-103">Clase EsentDataHasChangedException</span><span class="sxs-lookup"><span data-stu-id="454fa-103">EsentDataHasChangedException class</span></span>

<span data-ttu-id="454fa-104">Clase base para JET_err. Excepciones DataHasChanged.</span><span class="sxs-lookup"><span data-stu-id="454fa-104">Base class for JET_err.DataHasChanged exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="454fa-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="454fa-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="454fa-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="454fa-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="454fa-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="454fa-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="454fa-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="454fa-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="454fa-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="454fa-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="454fa-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="454fa-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="454fa-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="454fa-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="454fa-112">Microsoft. ISAM. esent. Interop. EsentDataHasChangedException</span><span class="sxs-lookup"><span data-stu-id="454fa-112">Microsoft.Isam.Esent.Interop.EsentDataHasChangedException</span></span>  

<span data-ttu-id="454fa-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="454fa-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="454fa-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="454fa-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="454fa-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="454fa-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDataHasChangedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDataHasChangedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDataHasChangedException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="454fa-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="454fa-116">Thread safety</span></span>

<span data-ttu-id="454fa-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="454fa-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="454fa-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="454fa-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="454fa-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="454fa-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="454fa-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="454fa-120">Reference</span></span>

[<span data-ttu-id="454fa-121">Miembros de EsentDataHasChangedException</span><span class="sxs-lookup"><span data-stu-id="454fa-121">EsentDataHasChangedException members</span></span>](./esentdatahaschangedexception-members.md)

[<span data-ttu-id="454fa-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="454fa-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
