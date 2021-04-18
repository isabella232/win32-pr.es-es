---
description: 'Más información sobre: clase EsentTableInUseException'
title: Clase EsentTableInUseException
TOCTitle: EsentTableInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTableInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttableinuseexception(v=EXCHG.10)
ms:contentKeyID: 55102969
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTableInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTableInUseException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f3a0ee3576ec0981e1251a8248a252967065a99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706358"
---
# <a name="esenttableinuseexception-class"></a><span data-ttu-id="07a09-103">Clase EsentTableInUseException</span><span class="sxs-lookup"><span data-stu-id="07a09-103">EsentTableInUseException class</span></span>

<span data-ttu-id="07a09-104">Clase base para JET_err. Excepciones TableInUse.</span><span class="sxs-lookup"><span data-stu-id="07a09-104">Base class for JET_err.TableInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="07a09-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="07a09-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="07a09-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="07a09-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="07a09-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="07a09-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="07a09-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="07a09-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="07a09-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="07a09-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="07a09-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="07a09-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="07a09-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="07a09-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="07a09-112">Microsoft. ISAM. esent. Interop. EsentTableInUseException</span><span class="sxs-lookup"><span data-stu-id="07a09-112">Microsoft.Isam.Esent.Interop.EsentTableInUseException</span></span>  

<span data-ttu-id="07a09-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="07a09-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="07a09-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="07a09-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="07a09-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07a09-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTableInUseException _
    Inherits EsentStateException
'Usage
Dim instance As EsentTableInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTableInUseException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="07a09-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="07a09-116">Thread safety</span></span>

<span data-ttu-id="07a09-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="07a09-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="07a09-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="07a09-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="07a09-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="07a09-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="07a09-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="07a09-120">Reference</span></span>

[<span data-ttu-id="07a09-121">Miembros de EsentTableInUseException</span><span class="sxs-lookup"><span data-stu-id="07a09-121">EsentTableInUseException members</span></span>](./esenttableinuseexception-members.md)

[<span data-ttu-id="07a09-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="07a09-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
