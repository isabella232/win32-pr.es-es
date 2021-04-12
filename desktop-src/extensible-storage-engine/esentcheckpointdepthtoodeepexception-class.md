---
description: 'Más información sobre: clase EsentCheckpointDepthTooDeepException'
title: Clase EsentCheckpointDepthTooDeepException
TOCTitle: EsentCheckpointDepthTooDeepException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcheckpointdepthtoodeepexception(v=EXCHG.10)
ms:contentKeyID: 55101222
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5cb3bf934336ba4990456966582f20c4ab50c392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278527"
---
# <a name="esentcheckpointdepthtoodeepexception-class"></a><span data-ttu-id="7a2d6-103">Clase EsentCheckpointDepthTooDeepException</span><span class="sxs-lookup"><span data-stu-id="7a2d6-103">EsentCheckpointDepthTooDeepException class</span></span>

<span data-ttu-id="7a2d6-104">Clase base para JET_err. Excepciones CheckpointDepthTooDeep.</span><span class="sxs-lookup"><span data-stu-id="7a2d6-104">Base class for JET_err.CheckpointDepthTooDeep exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7a2d6-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="7a2d6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7a2d6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7a2d6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7a2d6-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="7a2d6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7a2d6-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="7a2d6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7a2d6-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="7a2d6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7a2d6-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="7a2d6-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="7a2d6-111">Microsoft. ISAM. esent. Interop. EsentCheckpointDepthTooDeepException</span><span class="sxs-lookup"><span data-stu-id="7a2d6-111">Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException</span></span>  

<span data-ttu-id="7a2d6-112">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7a2d6-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7a2d6-113">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7a2d6-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7a2d6-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a2d6-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCheckpointDepthTooDeepException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentCheckpointDepthTooDeepException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCheckpointDepthTooDeepException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="7a2d6-115">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="7a2d6-115">Thread safety</span></span>

<span data-ttu-id="7a2d6-116">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="7a2d6-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7a2d6-117">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="7a2d6-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a2d6-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a2d6-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7a2d6-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="7a2d6-119">Reference</span></span>

[<span data-ttu-id="7a2d6-120">Miembros de EsentCheckpointDepthTooDeepException</span><span class="sxs-lookup"><span data-stu-id="7a2d6-120">EsentCheckpointDepthTooDeepException members</span></span>](./esentcheckpointdepthtoodeepexception-members.md)

[<span data-ttu-id="7a2d6-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7a2d6-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
