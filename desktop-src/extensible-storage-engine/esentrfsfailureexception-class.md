---
description: 'Más información sobre: clase EsentRfsFailureException'
title: Clase EsentRfsFailureException
TOCTitle: EsentRfsFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRfsFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrfsfailureexception(v=EXCHG.10)
ms:contentKeyID: 55102636
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRfsFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRfsFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 47c9a6ec3f782d53f0ff7c338bfbd84a6cf1ba91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715678"
---
# <a name="esentrfsfailureexception-class"></a><span data-ttu-id="8fd27-103">Clase EsentRfsFailureException</span><span class="sxs-lookup"><span data-stu-id="8fd27-103">EsentRfsFailureException class</span></span>

<span data-ttu-id="8fd27-104">Clase base para JET_err. Excepciones RfsFailure.</span><span class="sxs-lookup"><span data-stu-id="8fd27-104">Base class for JET_err.RfsFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8fd27-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="8fd27-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8fd27-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8fd27-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8fd27-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="8fd27-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8fd27-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="8fd27-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8fd27-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8fd27-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8fd27-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="8fd27-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="8fd27-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="8fd27-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="8fd27-112">Microsoft. ISAM. esent. Interop. EsentRfsFailureException</span><span class="sxs-lookup"><span data-stu-id="8fd27-112">Microsoft.Isam.Esent.Interop.EsentRfsFailureException</span></span>  

<span data-ttu-id="8fd27-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8fd27-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8fd27-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8fd27-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd27-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fd27-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRfsFailureException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentRfsFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRfsFailureException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="8fd27-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="8fd27-116">Thread safety</span></span>

<span data-ttu-id="8fd27-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="8fd27-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8fd27-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="8fd27-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8fd27-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fd27-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8fd27-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="8fd27-120">Reference</span></span>

[<span data-ttu-id="8fd27-121">Miembros de EsentRfsFailureException</span><span class="sxs-lookup"><span data-stu-id="8fd27-121">EsentRfsFailureException members</span></span>](./esentrfsfailureexception-members.md)

[<span data-ttu-id="8fd27-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8fd27-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
