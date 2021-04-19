---
description: 'Más información sobre: clase EsentRunningInMultiInstanceModeException'
title: Clase EsentRunningInMultiInstanceModeException
TOCTitle: EsentRunningInMultiInstanceModeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrunninginmultiinstancemodeexception(v=EXCHG.10)
ms:contentKeyID: 55102667
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55423c0559ce332dbf2759c54e283e006e2d03e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716364"
---
# <a name="esentrunninginmultiinstancemodeexception-class"></a><span data-ttu-id="96b2a-103">Clase EsentRunningInMultiInstanceModeException</span><span class="sxs-lookup"><span data-stu-id="96b2a-103">EsentRunningInMultiInstanceModeException class</span></span>

<span data-ttu-id="96b2a-104">Clase base para JET_err. Excepciones RunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="96b2a-104">Base class for JET_err.RunningInMultiInstanceMode exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="96b2a-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="96b2a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="96b2a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="96b2a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="96b2a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="96b2a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="96b2a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="96b2a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="96b2a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="96b2a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="96b2a-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="96b2a-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="96b2a-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="96b2a-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="96b2a-112">Microsoft. ISAM. esent. Interop. EsentRunningInMultiInstanceModeException</span><span class="sxs-lookup"><span data-stu-id="96b2a-112">Microsoft.Isam.Esent.Interop.EsentRunningInMultiInstanceModeException</span></span>  

<span data-ttu-id="96b2a-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="96b2a-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="96b2a-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="96b2a-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="96b2a-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96b2a-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRunningInMultiInstanceModeException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentRunningInMultiInstanceModeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRunningInMultiInstanceModeException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="96b2a-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="96b2a-116">Thread safety</span></span>

<span data-ttu-id="96b2a-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="96b2a-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="96b2a-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="96b2a-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="96b2a-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="96b2a-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="96b2a-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="96b2a-120">Reference</span></span>

[<span data-ttu-id="96b2a-121">Miembros de EsentRunningInMultiInstanceModeException</span><span class="sxs-lookup"><span data-stu-id="96b2a-121">EsentRunningInMultiInstanceModeException members</span></span>](./esentrunninginmultiinstancemodeexception-members.md)

[<span data-ttu-id="96b2a-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="96b2a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
