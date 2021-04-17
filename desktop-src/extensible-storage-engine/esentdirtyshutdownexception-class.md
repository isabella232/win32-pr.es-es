---
description: 'Más información sobre: clase EsentDirtyShutdownException'
title: Clase EsentDirtyShutdownException
TOCTitle: EsentDirtyShutdownException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdirtyshutdownexception(v=EXCHG.10)
ms:contentKeyID: 55101504
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72eb3984c034cbbb9c6163e183a5b8680fc49845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717092"
---
# <a name="esentdirtyshutdownexception-class"></a><span data-ttu-id="253c7-103">Clase EsentDirtyShutdownException</span><span class="sxs-lookup"><span data-stu-id="253c7-103">EsentDirtyShutdownException class</span></span>

<span data-ttu-id="253c7-104">Clase base para JET_err. Excepciones DirtyShutdown.</span><span class="sxs-lookup"><span data-stu-id="253c7-104">Base class for JET_err.DirtyShutdown exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="253c7-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="253c7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="253c7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="253c7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="253c7-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="253c7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="253c7-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="253c7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="253c7-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="253c7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="253c7-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="253c7-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="253c7-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="253c7-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="253c7-112">Microsoft. ISAM. esent. Interop. EsentDirtyShutdownException</span><span class="sxs-lookup"><span data-stu-id="253c7-112">Microsoft.Isam.Esent.Interop.EsentDirtyShutdownException</span></span>  

<span data-ttu-id="253c7-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="253c7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="253c7-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="253c7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="253c7-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="253c7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDirtyShutdownException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDirtyShutdownException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDirtyShutdownException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="253c7-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="253c7-116">Thread safety</span></span>

<span data-ttu-id="253c7-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="253c7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="253c7-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="253c7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="253c7-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="253c7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="253c7-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="253c7-120">Reference</span></span>

[<span data-ttu-id="253c7-121">Miembros de EsentDirtyShutdownException</span><span class="sxs-lookup"><span data-stu-id="253c7-121">EsentDirtyShutdownException members</span></span>](./esentdirtyshutdownexception-members.md)

[<span data-ttu-id="253c7-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="253c7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
