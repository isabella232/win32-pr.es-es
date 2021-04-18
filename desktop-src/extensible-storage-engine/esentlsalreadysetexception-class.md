---
description: 'Más información sobre: clase EsentLSAlreadySetException'
title: Clase EsentLSAlreadySetException
TOCTitle: EsentLSAlreadySetException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlsalreadysetexception(v=EXCHG.10)
ms:contentKeyID: 55102175
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7757740a6c07d6fedaa8b17c7a84755ade4de59b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716694"
---
# <a name="esentlsalreadysetexception-class"></a><span data-ttu-id="1f57e-103">Clase EsentLSAlreadySetException</span><span class="sxs-lookup"><span data-stu-id="1f57e-103">EsentLSAlreadySetException class</span></span>

<span data-ttu-id="1f57e-104">Clase base para JET_err. Excepciones LSAlreadySet.</span><span class="sxs-lookup"><span data-stu-id="1f57e-104">Base class for JET_err.LSAlreadySet exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1f57e-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="1f57e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1f57e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1f57e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1f57e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1f57e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1f57e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="1f57e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1f57e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1f57e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1f57e-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="1f57e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="1f57e-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="1f57e-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="1f57e-112">Microsoft. ISAM. esent. Interop. EsentLSAlreadySetException</span><span class="sxs-lookup"><span data-stu-id="1f57e-112">Microsoft.Isam.Esent.Interop.EsentLSAlreadySetException</span></span>  

<span data-ttu-id="1f57e-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1f57e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1f57e-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1f57e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1f57e-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f57e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLSAlreadySetException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentLSAlreadySetException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLSAlreadySetException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="1f57e-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="1f57e-116">Thread safety</span></span>

<span data-ttu-id="1f57e-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1f57e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1f57e-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1f57e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f57e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f57e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f57e-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="1f57e-120">Reference</span></span>

[<span data-ttu-id="1f57e-121">Miembros de EsentLSAlreadySetException</span><span class="sxs-lookup"><span data-stu-id="1f57e-121">EsentLSAlreadySetException members</span></span>](./esentlsalreadysetexception-members.md)

[<span data-ttu-id="1f57e-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1f57e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
