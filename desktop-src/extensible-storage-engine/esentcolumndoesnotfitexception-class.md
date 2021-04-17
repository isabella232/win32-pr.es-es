---
description: 'Más información sobre: clase EsentColumnDoesNotFitException'
title: Clase EsentColumnDoesNotFitException
TOCTitle: EsentColumnDoesNotFitException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnDoesNotFitException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumndoesnotfitexception(v=EXCHG.10)
ms:contentKeyID: 55107263
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnDoesNotFitException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnDoesNotFitException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 337601b7ded2288497897bdaff8665b8f8722321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714941"
---
# <a name="esentcolumndoesnotfitexception-class"></a><span data-ttu-id="0823b-103">Clase EsentColumnDoesNotFitException</span><span class="sxs-lookup"><span data-stu-id="0823b-103">EsentColumnDoesNotFitException class</span></span>

<span data-ttu-id="0823b-104">Clase base para JET_err. Excepciones ColumnDoesNotFit.</span><span class="sxs-lookup"><span data-stu-id="0823b-104">Base class for JET_err.ColumnDoesNotFit exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0823b-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="0823b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0823b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0823b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0823b-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0823b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0823b-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0823b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0823b-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0823b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0823b-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="0823b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="0823b-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="0823b-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="0823b-112">Microsoft. ISAM. esent. Interop. EsentColumnDoesNotFitException</span><span class="sxs-lookup"><span data-stu-id="0823b-112">Microsoft.Isam.Esent.Interop.EsentColumnDoesNotFitException</span></span>  

<span data-ttu-id="0823b-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0823b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0823b-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0823b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0823b-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0823b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnDoesNotFitException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnDoesNotFitException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnDoesNotFitException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="0823b-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="0823b-116">Thread safety</span></span>

<span data-ttu-id="0823b-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0823b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0823b-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0823b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0823b-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0823b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0823b-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="0823b-120">Reference</span></span>

[<span data-ttu-id="0823b-121">Miembros de EsentColumnDoesNotFitException</span><span class="sxs-lookup"><span data-stu-id="0823b-121">EsentColumnDoesNotFitException members</span></span>](./esentcolumndoesnotfitexception-members.md)

[<span data-ttu-id="0823b-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0823b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
