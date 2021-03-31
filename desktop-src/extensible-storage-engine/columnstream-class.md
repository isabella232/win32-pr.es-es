---
description: 'Más información sobre: clase ColumnStream'
title: Clase ColumnStream
TOCTitle: ColumnStream class
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumnStream
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream(v=EXCHG.10)
ms:contentKeyID: 55100939
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eea249347acd18ec71f03fcdc82b8a2baa1da9ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277500"
---
# <a name="columnstream-class"></a><span data-ttu-id="14902-103">Clase ColumnStream</span><span class="sxs-lookup"><span data-stu-id="14902-103">ColumnStream class</span></span>

<span data-ttu-id="14902-104">Esta clase proporciona una interfaz de streaming a una columna de valor largo (es decir, una columna de tipo [LongBinary](./jet-coltyp-enumeration.md) o [LongText](./jet-coltyp-enumeration.md)).</span><span class="sxs-lookup"><span data-stu-id="14902-104">This class provides a streaming interface to a long-value column (i.e. a column of type [LongBinary](./jet-coltyp-enumeration.md) or [LongText](./jet-coltyp-enumeration.md)).</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="14902-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="14902-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="14902-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="14902-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="14902-107">System.MarshalByRefObject</span><span class="sxs-lookup"><span data-stu-id="14902-107">System.MarshalByRefObject</span></span>](/dotnet/api/system.marshalbyrefobject)  
    [<span data-ttu-id="14902-108">System. IO. Stream</span><span class="sxs-lookup"><span data-stu-id="14902-108">System.IO.Stream</span></span>](/dotnet/api/system.io.stream)  
      <span data-ttu-id="14902-109">Microsoft. ISAM. esent. Interop. ColumnStream</span><span class="sxs-lookup"><span data-stu-id="14902-109">Microsoft.Isam.Esent.Interop.ColumnStream</span></span>  

<span data-ttu-id="14902-110">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="14902-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="14902-111">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="14902-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="14902-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14902-112">Syntax</span></span>

``` vb
'Declaration
Public Class ColumnStream _
    Inherits Stream
'Usage
Dim instance As ColumnStream
```

``` csharp
public class ColumnStream : Stream
```

## <a name="thread-safety"></a><span data-ttu-id="14902-113">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="14902-113">Thread safety</span></span>

<span data-ttu-id="14902-114">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="14902-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="14902-115">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="14902-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="14902-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="14902-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="14902-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="14902-117">Reference</span></span>

[<span data-ttu-id="14902-118">Miembros de ColumnStream</span><span class="sxs-lookup"><span data-stu-id="14902-118">ColumnStream members</span></span>](./columnstream-members.md)

[<span data-ttu-id="14902-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="14902-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
