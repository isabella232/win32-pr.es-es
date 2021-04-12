---
description: 'Más información sobre: <T> clase ColumnValueOfStruct'
title: Clase ColumnValueOfStruct(T)
TOCTitle: ColumnValueOfStruct(T) class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334171(v=EXCHG.10)
ms:contentKeyID: 55100962
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82083adcaaf0d9f5b4f2a720da83e95cd4b39401
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104361817"
---
# <a name="columnvalueofstructt-class"></a><span data-ttu-id="21b7f-103">\<T\>Clase ColumnValueOfStruct</span><span class="sxs-lookup"><span data-stu-id="21b7f-103">ColumnValueOfStruct\<T\> class</span></span>

<span data-ttu-id="21b7f-104">Establezca una columna de un tipo de estructura (por ejemplo, Int32/GUID).</span><span class="sxs-lookup"><span data-stu-id="21b7f-104">Set a column of a struct type (e.g. Int32/Guid).</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="21b7f-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="21b7f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="21b7f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="21b7f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="21b7f-107">Microsoft. ISAM. esent. Interop. ColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-107">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="21b7f-108">Microsoft. ISAM. esent. Interop. ColumnValueOfStruct\<T\></span><span class="sxs-lookup"><span data-stu-id="21b7f-108">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      

<span data-ttu-id="21b7f-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="21b7f-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="21b7f-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="21b7f-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="21b7f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21b7f-111">Syntax</span></span>

``` vb
'Declaration
Public MustInherit Class ColumnValueOfStruct(Of T As {Structure, New, IEquatable(Of T)}) _
    Inherits ColumnValue
'Usage
Dim instance As ColumnValueOfStruct(Of T)
```

``` csharp
public abstract class ColumnValueOfStruct<T> : ColumnValue
where T : struct, new(), IEquatable<T>
```

#### <a name="type-parameters"></a><span data-ttu-id="21b7f-112">Parámetros de tipo</span><span class="sxs-lookup"><span data-stu-id="21b7f-112">Type parameters</span></span>

  - <span data-ttu-id="21b7f-113">T</span><span class="sxs-lookup"><span data-stu-id="21b7f-113">T</span></span>  
    <span data-ttu-id="21b7f-114">Tipo que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="21b7f-114">Type to set.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="21b7f-115">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="21b7f-115">Thread safety</span></span>

<span data-ttu-id="21b7f-116">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="21b7f-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="21b7f-117">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="21b7f-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="21b7f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="21b7f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="21b7f-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="21b7f-119">Reference</span></span>

[<span data-ttu-id="21b7f-120">Miembros de ColumnValueOfStruct \<T\></span><span class="sxs-lookup"><span data-stu-id="21b7f-120">ColumnValueOfStruct\<T\> members</span></span>](./columnvalueofstruct-t-members.md)

[<span data-ttu-id="21b7f-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="21b7f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="21b7f-122">Tipos derivados</span><span class="sxs-lookup"><span data-stu-id="21b7f-122">Derived types</span></span>

[<span data-ttu-id="21b7f-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="21b7f-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="21b7f-124">Microsoft. ISAM. esent. Interop. ColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-124">Microsoft.Isam.Esent.Interop.ColumnValue</span></span>](./columnvalue-class.md)  
    <span data-ttu-id="21b7f-125">Microsoft. ISAM. esent. Interop. ColumnValueOfStruct\<T\></span><span class="sxs-lookup"><span data-stu-id="21b7f-125">Microsoft.Isam.Esent.Interop.ColumnValueOfStruct\<T\></span></span>  
      [<span data-ttu-id="21b7f-126">Microsoft. ISAM. esent. Interop. BoolColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-126">Microsoft.Isam.Esent.Interop.BoolColumnValue</span></span>](./boolcolumnvalue-class.md)  
      [<span data-ttu-id="21b7f-127">Microsoft. ISAM. esent. Interop. ByteColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-127">Microsoft.Isam.Esent.Interop.ByteColumnValue</span></span>](./bytecolumnvalue-class.md)  
      [<span data-ttu-id="21b7f-128">Microsoft. ISAM. esent. Interop. DateTimeColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-128">Microsoft.Isam.Esent.Interop.DateTimeColumnValue</span></span>](./datetimecolumnvalue-class.md)  
      [<span data-ttu-id="21b7f-129">Microsoft. ISAM. esent. Interop. DoubleColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-129">Microsoft.Isam.Esent.Interop.DoubleColumnValue</span></span>](./doublecolumnvalue-class.md)  
      [<span data-ttu-id="21b7f-130">Microsoft. ISAM. esent. Interop. FloatColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-130">Microsoft.Isam.Esent.Interop.FloatColumnValue</span></span>](./floatcolumnvalue-class.md)  
      [<span data-ttu-id="21b7f-131">Microsoft. ISAM. esent. Interop. GuidColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-131">Microsoft.Isam.Esent.Interop.GuidColumnValue</span></span>](./guidcolumnvalue-class.md)  
      [<span data-ttu-id="21b7f-132">Microsoft. ISAM. esent. Interop. Int16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-132">Microsoft.Isam.Esent.Interop.Int16ColumnValue</span></span>](./int16columnvalue-class.md)  
      [<span data-ttu-id="21b7f-133">Microsoft. ISAM. esent. Interop. Int32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-133">Microsoft.Isam.Esent.Interop.Int32ColumnValue</span></span>](./int32columnvalue-class.md)  
      [<span data-ttu-id="21b7f-134">Microsoft. ISAM. esent. Interop. Int64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-134">Microsoft.Isam.Esent.Interop.Int64ColumnValue</span></span>](./int64columnvalue-class.md)  
      [<span data-ttu-id="21b7f-135">Microsoft. ISAM. esent. Interop. UInt16ColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-135">Microsoft.Isam.Esent.Interop.UInt16ColumnValue</span></span>](./uint16columnvalue-class.md)  
      [<span data-ttu-id="21b7f-136">Microsoft. ISAM. esent. Interop. UInt32ColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-136">Microsoft.Isam.Esent.Interop.UInt32ColumnValue</span></span>](./uint32columnvalue-class.md)  
      [<span data-ttu-id="21b7f-137">Microsoft. ISAM. esent. Interop. UInt64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="21b7f-137">Microsoft.Isam.Esent.Interop.UInt64ColumnValue</span></span>](./uint64columnvalue-class.md)