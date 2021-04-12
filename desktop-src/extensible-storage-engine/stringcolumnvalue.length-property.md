---
description: 'Más información sobre: StringColumnValue. length (propiedad)'
title: StringColumnValue. length (propiedad)
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.StringColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55104090
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.StringColumnValue.get_Length
- Microsoft.Isam.Esent.Interop.StringColumnValue.Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed7313f66bd25653a66ebd8567a21c0ad5431ec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278040"
---
# <a name="stringcolumnvaluelength-property"></a><span data-ttu-id="2097f-103">StringColumnValue. length (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2097f-103">StringColumnValue.Length property</span></span>

<span data-ttu-id="2097f-104">Obtiene la longitud de bytes de un valor de columna, que es cero si la columna es null; de lo contrario, coincide con la longitud de bytes del valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="2097f-104">Gets the byte length of a column value, which is zero if column is null, otherwise it matches the byte length of the string value.</span></span> <span data-ttu-id="2097f-105">La longitud de bytes se determina en suposición de dos bytes por carácter.</span><span class="sxs-lookup"><span data-stu-id="2097f-105">The byte length is determined in assumption of two bytes per character.</span></span>

<span data-ttu-id="2097f-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2097f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2097f-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2097f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2097f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2097f-108">Syntax</span></span>

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As StringColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a><span data-ttu-id="2097f-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2097f-109">Property value</span></span>

<span data-ttu-id="2097f-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="2097f-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="2097f-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="2097f-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2097f-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="2097f-112">Reference</span></span>

[<span data-ttu-id="2097f-113">Clase StringColumnValue</span><span class="sxs-lookup"><span data-stu-id="2097f-113">StringColumnValue class</span></span>](./stringcolumnvalue-class.md)

[<span data-ttu-id="2097f-114">Miembros de StringColumnValue</span><span class="sxs-lookup"><span data-stu-id="2097f-114">StringColumnValue members</span></span>](./stringcolumnvalue-members.md)

[<span data-ttu-id="2097f-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2097f-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
