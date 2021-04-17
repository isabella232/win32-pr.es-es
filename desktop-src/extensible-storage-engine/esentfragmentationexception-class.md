---
description: 'Más información sobre: clase EsentFragmentationException'
title: Clase EsentFragmentationException
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 081198a696be9982e1fd8a7e4f1468e6d63d1c97
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721255"
---
# <a name="esentfragmentationexception-class"></a><span data-ttu-id="8ccd2-103">Clase EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-103">EsentFragmentationException class</span></span>

<span data-ttu-id="8ccd2-104">Clase base para las excepciones de fragmentación.</span><span class="sxs-lookup"><span data-stu-id="8ccd2-104">Base class for Fragmentation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8ccd2-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="8ccd2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8ccd2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8ccd2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8ccd2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="8ccd2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8ccd2-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8ccd2-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8ccd2-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="8ccd2-111">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            

<span data-ttu-id="8ccd2-112">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8ccd2-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8ccd2-113">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8ccd2-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8ccd2-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ccd2-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a><span data-ttu-id="8ccd2-115">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="8ccd2-115">Thread safety</span></span>

<span data-ttu-id="8ccd2-116">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="8ccd2-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8ccd2-117">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="8ccd2-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ccd2-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ccd2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8ccd2-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="8ccd2-119">Reference</span></span>

[<span data-ttu-id="8ccd2-120">Miembros de EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-120">EsentFragmentationException members</span></span>](./esentfragmentationexception-members.md)

[<span data-ttu-id="8ccd2-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8ccd2-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="8ccd2-122">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="8ccd2-122">Derived types</span></span>

[<span data-ttu-id="8ccd2-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="8ccd2-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8ccd2-124">System.Exception</span><span class="sxs-lookup"><span data-stu-id="8ccd2-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8ccd2-125">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8ccd2-126">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8ccd2-127">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-127">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          <span data-ttu-id="8ccd2-128">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-128">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>  
            [<span data-ttu-id="8ccd2-129">Microsoft. ISAM. esent. Interop. EsentLogSectorSizeMismatchException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-129">Microsoft.Isam.Esent.Interop.EsentLogSectorSizeMismatchException</span></span>](./esentlogsectorsizemismatchexception-class.md)  
            [<span data-ttu-id="8ccd2-130">Microsoft. ISAM. esent. Interop. EsentLogSequenceEndDatabasesConsistentException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-130">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndDatabasesConsistentException</span></span>](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [<span data-ttu-id="8ccd2-131">Microsoft. ISAM. esent. Interop. EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-131">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException</span></span>](./esentlogsequenceendexception-class.md)  
            [<span data-ttu-id="8ccd2-132">Microsoft. ISAM. esent. Interop. EsentOutOfAutoincrementValuesException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-132">Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException</span></span>](./esentoutofautoincrementvaluesexception-class.md)  
            [<span data-ttu-id="8ccd2-133">Microsoft. ISAM. esent. Interop. EsentOutOfDbtimeValuesException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-133">Microsoft.Isam.Esent.Interop.EsentOutOfDbtimeValuesException</span></span>](./esentoutofdbtimevaluesexception-class.md)  
            [<span data-ttu-id="8ccd2-134">Microsoft. ISAM. esent. Interop. EsentOutOfLongValueIDsException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-134">Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException</span></span>](./esentoutoflongvalueidsexception-class.md)  
            [<span data-ttu-id="8ccd2-135">Microsoft. ISAM. esent. Interop. EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-135">Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException</span></span>](./esentoutofobjectidsexception-class.md)  
            [<span data-ttu-id="8ccd2-136">Microsoft. ISAM. esent. Interop. EsentOutOfSequentialIndexValuesException</span><span class="sxs-lookup"><span data-stu-id="8ccd2-136">Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException</span></span>](./esentoutofsequentialindexvaluesexception-class.md)