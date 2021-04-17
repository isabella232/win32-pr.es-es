---
description: 'Más información sobre: clase EsentAccessDeniedException'
title: Clase EsentAccessDeniedException
TOCTitle: EsentAccessDeniedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentaccessdeniedexception(v=EXCHG.10)
ms:contentKeyID: 55101035
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7d81979a93bfa2ad3801047e5ec5cac9796bcda8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688306"
---
# <a name="esentaccessdeniedexception-class"></a><span data-ttu-id="d29b8-103">Clase EsentAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="d29b8-103">EsentAccessDeniedException class</span></span>

<span data-ttu-id="d29b8-104">Clase base para JET_err. Excepciones AccessDenied.</span><span class="sxs-lookup"><span data-stu-id="d29b8-104">Base class for JET_err.AccessDenied exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d29b8-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="d29b8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d29b8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d29b8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d29b8-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d29b8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d29b8-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d29b8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d29b8-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d29b8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d29b8-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="d29b8-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="d29b8-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="d29b8-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="d29b8-112">Microsoft. ISAM. esent. Interop. EsentAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="d29b8-112">Microsoft.Isam.Esent.Interop.EsentAccessDeniedException</span></span>  

<span data-ttu-id="d29b8-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d29b8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d29b8-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d29b8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d29b8-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d29b8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAccessDeniedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentAccessDeniedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAccessDeniedException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="d29b8-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="d29b8-116">Thread safety</span></span>

<span data-ttu-id="d29b8-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d29b8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d29b8-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d29b8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d29b8-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d29b8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d29b8-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="d29b8-120">Reference</span></span>

[<span data-ttu-id="d29b8-121">Miembros de EsentAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="d29b8-121">EsentAccessDeniedException members</span></span>](./esentaccessdeniedexception-members.md)

[<span data-ttu-id="d29b8-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d29b8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
