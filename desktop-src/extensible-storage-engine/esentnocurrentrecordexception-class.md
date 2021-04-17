---
description: 'Más información sobre: clase EsentNoCurrentRecordException'
title: Clase EsentNoCurrentRecordException
TOCTitle: EsentNoCurrentRecordException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnocurrentrecordexception(v=EXCHG.10)
ms:contentKeyID: 55102290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed58890ccd410101ecc6e6f38fafa0d254f4c2d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717185"
---
# <a name="esentnocurrentrecordexception-class"></a><span data-ttu-id="57410-103">Clase EsentNoCurrentRecordException</span><span class="sxs-lookup"><span data-stu-id="57410-103">EsentNoCurrentRecordException class</span></span>

<span data-ttu-id="57410-104">Clase base para JET_err. Excepciones NoCurrentRecord.</span><span class="sxs-lookup"><span data-stu-id="57410-104">Base class for JET_err.NoCurrentRecord exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="57410-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="57410-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="57410-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="57410-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="57410-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="57410-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="57410-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="57410-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="57410-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="57410-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="57410-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="57410-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="57410-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="57410-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="57410-112">Microsoft. ISAM. esent. Interop. EsentNoCurrentRecordException</span><span class="sxs-lookup"><span data-stu-id="57410-112">Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException</span></span>  

<span data-ttu-id="57410-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="57410-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="57410-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="57410-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="57410-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57410-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNoCurrentRecordException _
    Inherits EsentStateException
'Usage
Dim instance As EsentNoCurrentRecordException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNoCurrentRecordException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="57410-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="57410-116">Thread safety</span></span>

<span data-ttu-id="57410-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="57410-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="57410-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="57410-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="57410-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="57410-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="57410-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="57410-120">Reference</span></span>

[<span data-ttu-id="57410-121">Miembros de EsentNoCurrentRecordException</span><span class="sxs-lookup"><span data-stu-id="57410-121">EsentNoCurrentRecordException members</span></span>](./esentnocurrentrecordexception-members.md)

[<span data-ttu-id="57410-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="57410-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
