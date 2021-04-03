---
description: 'Más información sobre: clase EsentColumnCannotBeCompressedException'
title: Clase EsentColumnCannotBeCompressedException
TOCTitle: EsentColumnCannotBeCompressedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumncannotbecompressedexception(v=EXCHG.10)
ms:contentKeyID: 55101403
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1159125aaa9f1c522e3e3d1374bda772ce6c5db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083378"
---
# <a name="esentcolumncannotbecompressedexception-class"></a><span data-ttu-id="e63ea-103">Clase EsentColumnCannotBeCompressedException</span><span class="sxs-lookup"><span data-stu-id="e63ea-103">EsentColumnCannotBeCompressedException class</span></span>

<span data-ttu-id="e63ea-104">Clase base para JET_err. Excepciones ColumnCannotBeCompressed.</span><span class="sxs-lookup"><span data-stu-id="e63ea-104">Base class for JET_err.ColumnCannotBeCompressed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e63ea-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="e63ea-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e63ea-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e63ea-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e63ea-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="e63ea-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e63ea-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="e63ea-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e63ea-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e63ea-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e63ea-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="e63ea-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e63ea-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="e63ea-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="e63ea-112">Microsoft. ISAM. esent. Interop. EsentColumnCannotBeCompressedException</span><span class="sxs-lookup"><span data-stu-id="e63ea-112">Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException</span></span>  

<span data-ttu-id="e63ea-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e63ea-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e63ea-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e63ea-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e63ea-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e63ea-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnCannotBeCompressedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnCannotBeCompressedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnCannotBeCompressedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="e63ea-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="e63ea-116">Thread safety</span></span>

<span data-ttu-id="e63ea-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="e63ea-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e63ea-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="e63ea-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e63ea-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="e63ea-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e63ea-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="e63ea-120">Reference</span></span>

[<span data-ttu-id="e63ea-121">Miembros de EsentColumnCannotBeCompressedException</span><span class="sxs-lookup"><span data-stu-id="e63ea-121">EsentColumnCannotBeCompressedException members</span></span>](./esentcolumncannotbecompressedexception-members.md)

[<span data-ttu-id="e63ea-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e63ea-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
