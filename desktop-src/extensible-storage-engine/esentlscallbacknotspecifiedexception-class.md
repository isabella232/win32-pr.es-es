---
description: 'Más información sobre: clase EsentLSCallbackNotSpecifiedException'
title: Clase EsentLSCallbackNotSpecifiedException
TOCTitle: EsentLSCallbackNotSpecifiedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLSCallbackNotSpecifiedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlscallbacknotspecifiedexception(v=EXCHG.10)
ms:contentKeyID: 55102179
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLSCallbackNotSpecifiedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLSCallbackNotSpecifiedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6096410a8e0ca15539bac4a52412d2f61611ddbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156265"
---
# <a name="esentlscallbacknotspecifiedexception-class"></a><span data-ttu-id="eef06-103">Clase EsentLSCallbackNotSpecifiedException</span><span class="sxs-lookup"><span data-stu-id="eef06-103">EsentLSCallbackNotSpecifiedException class</span></span>

<span data-ttu-id="eef06-104">Clase base para JET_err. Excepciones LSCallbackNotSpecified.</span><span class="sxs-lookup"><span data-stu-id="eef06-104">Base class for JET_err.LSCallbackNotSpecified exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="eef06-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="eef06-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="eef06-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="eef06-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="eef06-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="eef06-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="eef06-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="eef06-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="eef06-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="eef06-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="eef06-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="eef06-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="eef06-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="eef06-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="eef06-112">Microsoft. ISAM. esent. Interop. EsentLSCallbackNotSpecifiedException</span><span class="sxs-lookup"><span data-stu-id="eef06-112">Microsoft.Isam.Esent.Interop.EsentLSCallbackNotSpecifiedException</span></span>  

<span data-ttu-id="eef06-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eef06-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eef06-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eef06-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eef06-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eef06-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLSCallbackNotSpecifiedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentLSCallbackNotSpecifiedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLSCallbackNotSpecifiedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="eef06-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="eef06-116">Thread safety</span></span>

<span data-ttu-id="eef06-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="eef06-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="eef06-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="eef06-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="eef06-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="eef06-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eef06-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="eef06-120">Reference</span></span>

[<span data-ttu-id="eef06-121">Miembros de EsentLSCallbackNotSpecifiedException</span><span class="sxs-lookup"><span data-stu-id="eef06-121">EsentLSCallbackNotSpecifiedException members</span></span>](./esentlscallbacknotspecifiedexception-members.md)

[<span data-ttu-id="eef06-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="eef06-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
