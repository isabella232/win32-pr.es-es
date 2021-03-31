---
description: 'Más información sobre: clase EsentRecordTooBigForBackwardCompatibilityException'
title: Clase EsentRecordTooBigForBackwardCompatibilityException
TOCTitle: EsentRecordTooBigForBackwardCompatibilityException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordtoobigforbackwardcompatibilityexception(v=EXCHG.10)
ms:contentKeyID: 55102602
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3d56e87678daf465f3f303d649e8c554fbb0c21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809175"
---
# <a name="esentrecordtoobigforbackwardcompatibilityexception-class"></a><span data-ttu-id="07aff-103">Clase EsentRecordTooBigForBackwardCompatibilityException</span><span class="sxs-lookup"><span data-stu-id="07aff-103">EsentRecordTooBigForBackwardCompatibilityException class</span></span>

<span data-ttu-id="07aff-104">Clase base para JET_err. Excepciones RecordTooBigForBackwardCompatibility.</span><span class="sxs-lookup"><span data-stu-id="07aff-104">Base class for JET_err.RecordTooBigForBackwardCompatibility exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="07aff-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="07aff-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="07aff-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="07aff-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="07aff-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="07aff-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="07aff-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="07aff-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="07aff-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="07aff-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="07aff-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="07aff-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="07aff-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="07aff-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="07aff-112">Microsoft. ISAM. esent. Interop. EsentRecordTooBigForBackwardCompatibilityException</span><span class="sxs-lookup"><span data-stu-id="07aff-112">Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException</span></span>  

<span data-ttu-id="07aff-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="07aff-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="07aff-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="07aff-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="07aff-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07aff-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordTooBigForBackwardCompatibilityException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecordTooBigForBackwardCompatibilityException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordTooBigForBackwardCompatibilityException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="07aff-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="07aff-116">Thread safety</span></span>

<span data-ttu-id="07aff-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="07aff-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="07aff-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="07aff-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="07aff-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="07aff-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="07aff-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="07aff-120">Reference</span></span>

[<span data-ttu-id="07aff-121">Miembros de EsentRecordTooBigForBackwardCompatibilityException</span><span class="sxs-lookup"><span data-stu-id="07aff-121">EsentRecordTooBigForBackwardCompatibilityException members</span></span>](./esentrecordtoobigforbackwardcompatibilityexception-members.md)

[<span data-ttu-id="07aff-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="07aff-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
