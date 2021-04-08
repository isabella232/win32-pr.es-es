---
description: 'Más información sobre: clase EsentDisabledFunctionalityException'
title: Clase EsentDisabledFunctionalityException
TOCTitle: EsentDisabledFunctionalityException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDisabledFunctionalityException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdisabledfunctionalityexception(v=EXCHG.10)
ms:contentKeyID: 55101615
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDisabledFunctionalityException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDisabledFunctionalityException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ec4458b1306f11240f2090403dcc6ae4c7db07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002993"
---
# <a name="esentdisabledfunctionalityexception-class"></a><span data-ttu-id="0ca5a-103">Clase EsentDisabledFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="0ca5a-103">EsentDisabledFunctionalityException class</span></span>

<span data-ttu-id="0ca5a-104">Clase base para JET_err. Excepciones DisabledFunctionality.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-104">Base class for JET_err.DisabledFunctionality exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0ca5a-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="0ca5a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0ca5a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0ca5a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0ca5a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0ca5a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0ca5a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0ca5a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0ca5a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0ca5a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0ca5a-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="0ca5a-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="0ca5a-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="0ca5a-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="0ca5a-112">Microsoft. ISAM. esent. Interop. EsentDisabledFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="0ca5a-112">Microsoft.Isam.Esent.Interop.EsentDisabledFunctionalityException</span></span>  

<span data-ttu-id="0ca5a-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0ca5a-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0ca5a-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0ca5a-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0ca5a-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ca5a-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDisabledFunctionalityException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDisabledFunctionalityException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDisabledFunctionalityException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="0ca5a-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="0ca5a-116">Thread safety</span></span>

<span data-ttu-id="0ca5a-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0ca5a-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0ca5a-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ca5a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ca5a-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0ca5a-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="0ca5a-120">Reference</span></span>

[<span data-ttu-id="0ca5a-121">Miembros de EsentDisabledFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="0ca5a-121">EsentDisabledFunctionalityException members</span></span>](./esentdisabledfunctionalityexception-members.md)

[<span data-ttu-id="0ca5a-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0ca5a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
