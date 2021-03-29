---
description: 'Más información acerca de: propiedad JET_RECSIZE. cbDataCompressed'
title: Propiedad JET_RECSIZE. cbDataCompressed (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'cbDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cbdatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515358
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbDataCompressed
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 747c2f00077f6a9d13de059f742bacc9a7936d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808516"
---
# <a name="jet_recsizecbdatacompressed-property"></a><span data-ttu-id="8570c-103">Propiedad JET_RECSIZE. cbDataCompressed</span><span class="sxs-lookup"><span data-stu-id="8570c-103">JET_RECSIZE.cbDataCompressed property</span></span>

<span data-ttu-id="8570c-104">Obtiene el tamaño comprimido de los datos de usuario en el registro.</span><span class="sxs-lookup"><span data-stu-id="8570c-104">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="8570c-105">Es lo mismo que [cbData](./jet-recsize.cbdata-property.md) si no se comprimen valores largos intrínsecos).</span><span class="sxs-lookup"><span data-stu-id="8570c-105">This is the same as [cbData](./jet-recsize.cbdata-property.md) if no intrinsic long-values are compressed).</span></span>

<span data-ttu-id="8570c-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8570c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="8570c-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8570c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8570c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8570c-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbDataCompressed
```

``` csharp
public long cbDataCompressed { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="8570c-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8570c-109">Property value</span></span>

<span data-ttu-id="8570c-110">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="8570c-110">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8570c-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="8570c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8570c-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="8570c-112">Reference</span></span>

[<span data-ttu-id="8570c-113">Estructura de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="8570c-113">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="8570c-114">Miembros de JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="8570c-114">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="8570c-115">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="8570c-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
