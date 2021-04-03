---
description: 'Más información sobre: ColumnStream. Write (método)'
title: ColumnStream. Write (método)
TOCTitle: 'Write method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Write(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.write(v=EXCHG.10)
ms:contentKeyID: 55100987
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77b62e7dd028da3452082c973690ce0c0210b438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083290"
---
# <a name="columnstreamwrite-method"></a><span data-ttu-id="a02b1-103">ColumnStream. Write (método)</span><span class="sxs-lookup"><span data-stu-id="a02b1-103">ColumnStream.Write method</span></span>

<span data-ttu-id="a02b1-104">Escribe una secuencia de bytes en la secuencia actual y avanza la posición actual en esta secuencia según el número de bytes escritos.</span><span class="sxs-lookup"><span data-stu-id="a02b1-104">Writes a sequence of bytes to the current stream and advances the current position within this stream by the number of bytes written.</span></span>

<span data-ttu-id="a02b1-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a02b1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a02b1-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a02b1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a02b1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a02b1-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Sub Write ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
)
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer

instance.Write(buffer, offset, count)
```

``` csharp
public override void Write(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="a02b1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a02b1-108">Parameters</span></span>

  - <span data-ttu-id="a02b1-109">buffer</span><span class="sxs-lookup"><span data-stu-id="a02b1-109">buffer</span></span>  
    <span data-ttu-id="a02b1-110">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="a02b1-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="a02b1-111">Búfer del que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="a02b1-111">The buffer to write from.</span></span>

<!-- end list -->

  - <span data-ttu-id="a02b1-112">offset</span><span class="sxs-lookup"><span data-stu-id="a02b1-112">offset</span></span>  
    <span data-ttu-id="a02b1-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a02b1-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a02b1-114">Desplazamiento en el búfer que se va a escribir.</span><span class="sxs-lookup"><span data-stu-id="a02b1-114">The offset in the buffer to write.</span></span>

<!-- end list -->

  - <span data-ttu-id="a02b1-115">count</span><span class="sxs-lookup"><span data-stu-id="a02b1-115">count</span></span>  
    <span data-ttu-id="a02b1-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a02b1-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a02b1-117">Número de bytes que se van a escribir.</span><span class="sxs-lookup"><span data-stu-id="a02b1-117">The number of bytes to write.</span></span>

## <a name="see-also"></a><span data-ttu-id="a02b1-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a02b1-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a02b1-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="a02b1-119">Reference</span></span>

[<span data-ttu-id="a02b1-120">Clase ColumnStream</span><span class="sxs-lookup"><span data-stu-id="a02b1-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="a02b1-121">Miembros de ColumnStream</span><span class="sxs-lookup"><span data-stu-id="a02b1-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="a02b1-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a02b1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
