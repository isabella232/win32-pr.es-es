---
description: 'Más información sobre: BoolColumnValue. GetValueFromBytes (método)'
title: BoolColumnValue. GetValueFromBytes, método
TOCTitle: 'GetValueFromBytes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.BoolColumnValue.GetValueFromBytes(System.Byte[],System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.boolcolumnvalue.getvaluefrombytes(v=EXCHG.10)
ms:contentKeyID: 55100913
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.GetValueFromBytes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BoolColumnValue.GetValueFromBytes
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a0d4f41995525632f582cf89709076f60cdd6181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278751"
---
# <a name="boolcolumnvaluegetvaluefrombytes-method"></a><span data-ttu-id="10d50-103">BoolColumnValue. GetValueFromBytes, método</span><span class="sxs-lookup"><span data-stu-id="10d50-103">BoolColumnValue.GetValueFromBytes method</span></span>

<span data-ttu-id="10d50-104">Dados los datos recuperados de ESENT, descodifique los datos y establezca el valor en el objeto ColumnValue.</span><span class="sxs-lookup"><span data-stu-id="10d50-104">Given data retrieved from ESENT, decode the data and set the value in the ColumnValue object.</span></span>

<span data-ttu-id="10d50-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="10d50-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="10d50-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="10d50-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10d50-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10d50-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="10d50-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10d50-108">Parameters</span></span>

  - <span data-ttu-id="10d50-109">value</span><span class="sxs-lookup"><span data-stu-id="10d50-109">value</span></span>  
    <span data-ttu-id="10d50-110">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="10d50-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="10d50-111">Matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="10d50-111">An array of bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="10d50-112">startIndex</span><span class="sxs-lookup"><span data-stu-id="10d50-112">startIndex</span></span>  
    <span data-ttu-id="10d50-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="10d50-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="10d50-114">Posición inicial dentro de los bytes.</span><span class="sxs-lookup"><span data-stu-id="10d50-114">The starting position within the bytes.</span></span>

<!-- end list -->

  - <span data-ttu-id="10d50-115">count</span><span class="sxs-lookup"><span data-stu-id="10d50-115">count</span></span>  
    <span data-ttu-id="10d50-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="10d50-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="10d50-117">Número de bytes que se van a descodificar.</span><span class="sxs-lookup"><span data-stu-id="10d50-117">The number of bytes to decode.</span></span>

<!-- end list -->

  - <span data-ttu-id="10d50-118">err</span><span class="sxs-lookup"><span data-stu-id="10d50-118">err</span></span>  
    <span data-ttu-id="10d50-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="10d50-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="10d50-120">Error devuelto desde ESENT.</span><span class="sxs-lookup"><span data-stu-id="10d50-120">The error returned from ESENT.</span></span>

## <a name="see-also"></a><span data-ttu-id="10d50-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="10d50-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10d50-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="10d50-122">Reference</span></span>

[<span data-ttu-id="10d50-123">Clase BoolColumnValue</span><span class="sxs-lookup"><span data-stu-id="10d50-123">BoolColumnValue class</span></span>](./boolcolumnvalue-class.md)

[<span data-ttu-id="10d50-124">Miembros de BoolColumnValue</span><span class="sxs-lookup"><span data-stu-id="10d50-124">BoolColumnValue members</span></span>](./boolcolumnvalue-members.md)

[<span data-ttu-id="10d50-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="10d50-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
