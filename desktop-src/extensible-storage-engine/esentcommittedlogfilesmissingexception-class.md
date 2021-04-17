---
description: 'Más información sobre: clase EsentCommittedLogFilesMissingException'
title: Clase EsentCommittedLogFilesMissingException
TOCTitle: EsentCommittedLogFilesMissingException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcommittedlogfilesmissingexception(v=EXCHG.10)
ms:contentKeyID: 55101361
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 937534d550ff13fce4240411ce486e6d789ef957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697466"
---
# <a name="esentcommittedlogfilesmissingexception-class"></a><span data-ttu-id="d6c26-103">Clase EsentCommittedLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="d6c26-103">EsentCommittedLogFilesMissingException class</span></span>

<span data-ttu-id="d6c26-104">Clase base para las excepciones JET_err. CommittedLogFilesMissing.</span><span class="sxs-lookup"><span data-stu-id="d6c26-104">Base class for JET_err.CommittedLogFilesMissing exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d6c26-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="d6c26-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d6c26-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d6c26-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d6c26-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d6c26-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d6c26-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d6c26-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d6c26-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d6c26-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d6c26-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="d6c26-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="d6c26-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="d6c26-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="d6c26-112">Microsoft. ISAM. esent. Interop. EsentCommittedLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="d6c26-112">Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException</span></span>  

<span data-ttu-id="d6c26-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6c26-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d6c26-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d6c26-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6c26-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6c26-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCommittedLogFilesMissingException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentCommittedLogFilesMissingException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCommittedLogFilesMissingException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="d6c26-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="d6c26-116">Thread safety</span></span>

<span data-ttu-id="d6c26-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d6c26-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d6c26-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d6c26-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6c26-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6c26-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6c26-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="d6c26-120">Reference</span></span>

[<span data-ttu-id="d6c26-121">Miembros de EsentCommittedLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="d6c26-121">EsentCommittedLogFilesMissingException members</span></span>](./esentcommittedlogfilesmissingexception-members.md)

[<span data-ttu-id="d6c26-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d6c26-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
