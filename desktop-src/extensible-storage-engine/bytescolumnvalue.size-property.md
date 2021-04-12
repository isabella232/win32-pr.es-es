---
description: 'Más información sobre: BytesColumnValue. Size (propiedad)'
title: BytesColumnValue. Size (propiedad)
TOCTitle: 'Size property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BytesColumnValue.Size
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.size(v=EXCHG.10)
ms:contentKeyID: 55101188
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Size
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.get_Size
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Size
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 36f6aee31c5fdb61ac124904d07ee59f39728be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277501"
---
# <a name="bytescolumnvaluesize-property"></a><span data-ttu-id="337b4-103">BytesColumnValue. Size (propiedad)</span><span class="sxs-lookup"><span data-stu-id="337b4-103">BytesColumnValue.Size property</span></span>

<span data-ttu-id="337b4-104">Obtiene el tamaño del valor de la columna.</span><span class="sxs-lookup"><span data-stu-id="337b4-104">Gets the size of the value in the column.</span></span> <span data-ttu-id="337b4-105">Esto devuelve 0 para las columnas de tamaño variable (es decir, binary y String).</span><span class="sxs-lookup"><span data-stu-id="337b4-105">This returns 0 for variable sized columns (i.e. binary and string).</span></span>

<span data-ttu-id="337b4-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="337b4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="337b4-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="337b4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="337b4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="337b4-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides ReadOnly Property Size As Integer
    Get
'Usage
Dim value As Integer

value = Me.Size
```

``` csharp
protected override int Size { get; }
```

#### <a name="property-value"></a><span data-ttu-id="337b4-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="337b4-109">Property value</span></span>

<span data-ttu-id="337b4-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="337b4-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="337b4-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="337b4-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="337b4-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="337b4-112">Reference</span></span>

[<span data-ttu-id="337b4-113">Clase BytesColumnValue</span><span class="sxs-lookup"><span data-stu-id="337b4-113">BytesColumnValue class</span></span>](./bytescolumnvalue-class.md)

[<span data-ttu-id="337b4-114">Miembros de BytesColumnValue</span><span class="sxs-lookup"><span data-stu-id="337b4-114">BytesColumnValue members</span></span>](./bytescolumnvalue-members.md)

[<span data-ttu-id="337b4-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="337b4-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
