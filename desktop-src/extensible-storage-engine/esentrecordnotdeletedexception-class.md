---
description: 'Más información sobre: clase EsentRecordNotDeletedException'
title: Clase EsentRecordNotDeletedException
TOCTitle: EsentRecordNotDeletedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordnotdeletedexception(v=EXCHG.10)
ms:contentKeyID: 55102578
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70eb38e960b127474415c9b7291e4765719fb7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715331"
---
# <a name="esentrecordnotdeletedexception-class"></a><span data-ttu-id="5d679-103">Clase EsentRecordNotDeletedException</span><span class="sxs-lookup"><span data-stu-id="5d679-103">EsentRecordNotDeletedException class</span></span>

<span data-ttu-id="5d679-104">Clase base para JET_err. Excepciones RecordNotDeleted.</span><span class="sxs-lookup"><span data-stu-id="5d679-104">Base class for JET_err.RecordNotDeleted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5d679-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="5d679-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5d679-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5d679-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5d679-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="5d679-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5d679-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="5d679-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5d679-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="5d679-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5d679-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="5d679-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="5d679-111">Microsoft. ISAM. esent. Interop. EsentRecordNotDeletedException</span><span class="sxs-lookup"><span data-stu-id="5d679-111">Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException</span></span>  

<span data-ttu-id="5d679-112">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5d679-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5d679-113">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5d679-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5d679-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d679-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordNotDeletedException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentRecordNotDeletedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordNotDeletedException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="5d679-115">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="5d679-115">Thread safety</span></span>

<span data-ttu-id="5d679-116">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="5d679-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5d679-117">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="5d679-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d679-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d679-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5d679-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="5d679-119">Reference</span></span>

[<span data-ttu-id="5d679-120">Miembros de EsentRecordNotDeletedException</span><span class="sxs-lookup"><span data-stu-id="5d679-120">EsentRecordNotDeletedException members</span></span>](./esentrecordnotdeletedexception-members.md)

[<span data-ttu-id="5d679-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5d679-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
