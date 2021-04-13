---
description: 'Más información sobre: ColumnStream. Seek (método)'
title: ColumnStream. Seek (método)
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5489bb0ee9a4a1550166e14a945a2a6d58c45af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543438"
---
# <a name="columnstreamseek-method"></a><span data-ttu-id="8967d-103">ColumnStream. Seek (método)</span><span class="sxs-lookup"><span data-stu-id="8967d-103">ColumnStream.Seek method</span></span>

<span data-ttu-id="8967d-104">Establece la posición en la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="8967d-104">Sets the position in the current stream.</span></span>

<span data-ttu-id="8967d-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8967d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8967d-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8967d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8967d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8967d-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a><span data-ttu-id="8967d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8967d-108">Parameters</span></span>

  - <span data-ttu-id="8967d-109">offset</span><span class="sxs-lookup"><span data-stu-id="8967d-109">offset</span></span>  
    <span data-ttu-id="8967d-110">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="8967d-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="8967d-111">Desplazamiento de bytes con respecto al parámetro de origen.</span><span class="sxs-lookup"><span data-stu-id="8967d-111">Byte offset relative to the origin parameter.</span></span>

<!-- end list -->

  - <span data-ttu-id="8967d-112">origen</span><span class="sxs-lookup"><span data-stu-id="8967d-112">origin</span></span>  
    <span data-ttu-id="8967d-113">Tipo: [System. IO. SeekOrigin](/dotnet/api/system.io.seekorigin)</span><span class="sxs-lookup"><span data-stu-id="8967d-113">Type: [System.IO.SeekOrigin](/dotnet/api/system.io.seekorigin)</span></span>  
    
    <span data-ttu-id="8967d-114">Un SeekOrigin que indica el punto de referencia para la nueva posición.</span><span class="sxs-lookup"><span data-stu-id="8967d-114">A SeekOrigin indicating the reference point for the new position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8967d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8967d-115">Return value</span></span>

<span data-ttu-id="8967d-116">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="8967d-116">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
<span data-ttu-id="8967d-117">Nueva posición en la secuencia actual.</span><span class="sxs-lookup"><span data-stu-id="8967d-117">The new position in the current stream.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8967d-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="8967d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8967d-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="8967d-119">Reference</span></span>

[<span data-ttu-id="8967d-120">Clase ColumnStream</span><span class="sxs-lookup"><span data-stu-id="8967d-120">ColumnStream class</span></span>](./columnstream-class.md)

[<span data-ttu-id="8967d-121">Miembros de ColumnStream</span><span class="sxs-lookup"><span data-stu-id="8967d-121">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="8967d-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8967d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
