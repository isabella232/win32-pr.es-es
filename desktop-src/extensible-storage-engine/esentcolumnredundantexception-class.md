---
description: 'Más información sobre: clase EsentColumnRedundantException'
title: Clase EsentColumnRedundantException
TOCTitle: EsentColumnRedundantException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnRedundantException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumnredundantexception(v=EXCHG.10)
ms:contentKeyID: 55101247
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnRedundantException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnRedundantException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18b2fdd850e26c5a435841110a4e1ac5c0c7c640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714985"
---
# <a name="esentcolumnredundantexception-class"></a><span data-ttu-id="d9491-103">Clase EsentColumnRedundantException</span><span class="sxs-lookup"><span data-stu-id="d9491-103">EsentColumnRedundantException class</span></span>

<span data-ttu-id="d9491-104">Clase base para JET_err. Excepciones ColumnRedundant.</span><span class="sxs-lookup"><span data-stu-id="d9491-104">Base class for JET_err.ColumnRedundant exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d9491-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="d9491-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d9491-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d9491-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d9491-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d9491-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d9491-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d9491-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d9491-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d9491-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d9491-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="d9491-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="d9491-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="d9491-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="d9491-112">Microsoft. ISAM. esent. Interop. EsentColumnRedundantException</span><span class="sxs-lookup"><span data-stu-id="d9491-112">Microsoft.Isam.Esent.Interop.EsentColumnRedundantException</span></span>  

<span data-ttu-id="d9491-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d9491-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d9491-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d9491-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d9491-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9491-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnRedundantException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnRedundantException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnRedundantException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="d9491-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="d9491-116">Thread safety</span></span>

<span data-ttu-id="d9491-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d9491-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d9491-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d9491-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9491-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9491-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d9491-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="d9491-120">Reference</span></span>

[<span data-ttu-id="d9491-121">Miembros de EsentColumnRedundantException</span><span class="sxs-lookup"><span data-stu-id="d9491-121">EsentColumnRedundantException members</span></span>](./esentcolumnredundantexception-members.md)

[<span data-ttu-id="d9491-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d9491-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
