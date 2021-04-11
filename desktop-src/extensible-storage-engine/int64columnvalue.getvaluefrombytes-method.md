---
description: 'Más información sobre: Int64ColumnValue. GetValueFromBytes (método)'
title: Int64ColumnValue. GetValueFromBytes, método
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.int64columnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55103365
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Int64ColumnValue.GetValueFromBytes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a33d85fb929f61d67d814ad47eb64406b77e7c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361487"
---
# <a name="int64columnvaluegetvaluefrombytes-method"></a><span data-ttu-id="b7503-103">Int64ColumnValue. GetValueFromBytes, método</span><span class="sxs-lookup"><span data-stu-id="b7503-103">Int64ColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="b7503-104">Dados los datos recuperados de ESENT, descodifique los datos y establezca el valor en el objeto ColumnValue.</span><span class="sxs-lookup"><span data-stu-id="b7503-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="b7503-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7503-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7503-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b7503-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7503-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7503-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub GetValueFromBytes ( _
    value As Byte(), _
    startIndex As Integer, _
    count As Integer, _
    err As Integer _
)
'Usage
Dim value As Byte()
Dim startIndex As Integer
Dim count As Integer
Dim err As Integer

Me.GetValueFromBytes(value, startIndex, _
    count, err)
```

``` csharp
protected override void GetValueFromBytes(
    byte[] value,
    int startIndex,
    int count,
    int err
)
```

#### <a name="parameters"></a><span data-ttu-id="b7503-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b7503-108">Parameters</span></span>

  - <span data-ttu-id="b7503-109">value</span><span class="sxs-lookup"><span data-stu-id="b7503-109">value</span></span>  
    <span data-ttu-id="b7503-110">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="b7503-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="b7503-111">Matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="b7503-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7503-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="b7503-112">startIndex</span></span>  
    <span data-ttu-id="b7503-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b7503-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b7503-114">Posición inicial dentro de los bytes.</span><span class="sxs-lookup"><span data-stu-id="b7503-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7503-115">count</span><span class="sxs-lookup"><span data-stu-id="b7503-115">count</span></span>  
    <span data-ttu-id="b7503-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b7503-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b7503-117">Número de bytes que se van a descodificar.</span><span class="sxs-lookup"><span data-stu-id="b7503-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7503-118">err</span><span class="sxs-lookup"><span data-stu-id="b7503-118">err</span></span>  
    <span data-ttu-id="b7503-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b7503-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b7503-120">Error devuelto desde ESENT.</span><span class="sxs-lookup"><span data-stu-id="b7503-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7503-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7503-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7503-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="b7503-122">Reference</span></span>

[<span data-ttu-id="b7503-123">Clase Int64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="b7503-123">Int64ColumnValue class</span></span>](./int64columnvalue-class.md)

[<span data-ttu-id="b7503-124">Miembros de Int64ColumnValue</span><span class="sxs-lookup"><span data-stu-id="b7503-124">Int64ColumnValue members</span></span>](./int64columnvalue-members.md)

[<span data-ttu-id="b7503-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b7503-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
