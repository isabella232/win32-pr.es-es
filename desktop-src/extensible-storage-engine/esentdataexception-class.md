---
description: 'Más información sobre: clase EsentDataException'
title: Clase EsentDataException
TOCTitle: EsentDataException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDataException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101456
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDataException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 996839740d1b008ffae12cf823b9664bf8ca4273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715691"
---
# <a name="esentdataexception-class"></a><span data-ttu-id="94b70-103">Clase EsentDataException</span><span class="sxs-lookup"><span data-stu-id="94b70-103">EsentDataException class</span></span>

<span data-ttu-id="94b70-104">Clase base para las excepciones de datos.</span><span class="sxs-lookup"><span data-stu-id="94b70-104">Base class for Data exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="94b70-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="94b70-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="94b70-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="94b70-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="94b70-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="94b70-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="94b70-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="94b70-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="94b70-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="94b70-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="94b70-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="94b70-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>  
          [<span data-ttu-id="94b70-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="94b70-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
          [<span data-ttu-id="94b70-112">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="94b70-112">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
          [<span data-ttu-id="94b70-113">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="94b70-113">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  

<span data-ttu-id="94b70-114">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="94b70-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="94b70-115">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="94b70-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="94b70-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94b70-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentDataException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentDataException
```

``` csharp
[SerializableAttribute]
public abstract class EsentDataException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="94b70-117">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="94b70-117">Thread safety</span></span>

<span data-ttu-id="94b70-118">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="94b70-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="94b70-119">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="94b70-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="94b70-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="94b70-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="94b70-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="94b70-121">Reference</span></span>

[<span data-ttu-id="94b70-122">Miembros de EsentDataException</span><span class="sxs-lookup"><span data-stu-id="94b70-122">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="94b70-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="94b70-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
