---
description: 'Más información sobre: ColumnStream. Read (método)'
title: ColumnStream. Read (método)
TOCTitle: 'Read method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Read(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.read(v=EXCHG.10)
ms:contentKeyID: 55100988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Read
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e407a9069807d10eaabf4f7ac3fce3919576bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678339"
---
# <a name="columnstreamread-method"></a><span data-ttu-id="4b16e-103">ColumnStream. Read (método)</span><span class="sxs-lookup"><span data-stu-id="4b16e-103">ColumnStream.Read method</span></span>

<span data-ttu-id="4b16e-104">Lee una secuencia de bytes en el flujo actual y avanza la posición en el flujo según el número de bytes leídos.</span><span class="sxs-lookup"><span data-stu-id="4b16e-104">Reads a sequence of bytes from the current stream and advances the position within the stream by the number of bytes read.</span></span>

<span data-ttu-id="4b16e-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4b16e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4b16e-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4b16e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4b16e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b16e-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Read ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
) As Integer
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer
Dim returnValue As Integer

returnValue = instance.Read(buffer, offset, _
    count)
```

``` csharp
public override int Read(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a><span data-ttu-id="4b16e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b16e-108">Parameters</span></span>

  - <span data-ttu-id="4b16e-109">buffer</span><span class="sxs-lookup"><span data-stu-id="4b16e-109">buffer</span></span>  
    <span data-ttu-id="4b16e-110">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="4b16e-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="4b16e-111">Búfer en el que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="4b16e-111">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="4b16e-112">offset</span><span class="sxs-lookup"><span data-stu-id="4b16e-112">offset</span></span>  
    <span data-ttu-id="4b16e-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4b16e-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4b16e-114">Desplazamiento en el búfer en el que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="4b16e-114">The offset in the buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="4b16e-115">count</span><span class="sxs-lookup"><span data-stu-id="4b16e-115">count</span></span>  
    <span data-ttu-id="4b16e-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4b16e-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4b16e-117">Número de bytes que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="4b16e-117">The number of bytes to read.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4b16e-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b16e-118">Return value</span></span>

<span data-ttu-id="4b16e-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4b16e-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="4b16e-120">Número de bytes leídos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="4b16e-120">The number of bytes read into the buffer.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4b16e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b16e-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4b16e-122">Referencia</span><span class="sxs-lookup"><span data-stu-id="4b16e-122">Reference</span></span>

[<span data-ttu-id="4b16e-123">Clase ColumnStream</span><span class="sxs-lookup"><span data-stu-id="4b16e-123">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="4b16e-124">Miembros de ColumnStream</span><span class="sxs-lookup"><span data-stu-id="4b16e-124">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="4b16e-125">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4b16e-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
