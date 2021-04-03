---
description: 'Más información acerca de: propiedad JET_RETRIEVECOLUMN. cbData'
title: Propiedad JET_RETRIEVECOLUMN. cbData
TOCTitle: 'cbData property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.cbData
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn.cbdata(v=EXCHG.10)
ms:contentKeyID: 55103810
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.cbData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.set_cbData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.get_cbData
- Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN.cbData
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b91e78d31e2c82b0825da5e320fef558f790caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810508"
---
# <a name="jet_retrievecolumncbdata-property"></a><span data-ttu-id="8c039-103">Propiedad JET_RETRIEVECOLUMN. cbData</span><span class="sxs-lookup"><span data-stu-id="8c039-103">JET_RETRIEVECOLUMN.cbData property</span></span>

<span data-ttu-id="8c039-104">Obtiene o establece el tamaño del búfer de [pvData](./jet-retrievecolumn.pvdata-property.md) , en bytes.</span><span class="sxs-lookup"><span data-stu-id="8c039-104">Gets or sets the size of the [pvData](./jet-retrievecolumn.pvdata-property.md) buffer, in bytes.</span></span> <span data-ttu-id="8c039-105">La operación de recuperación de columna no almacenará más datos en pvData que cbData.</span><span class="sxs-lookup"><span data-stu-id="8c039-105">The retrieve column operation will not store more data in pvData than cbData.</span></span>

<span data-ttu-id="8c039-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8c039-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8c039-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8c039-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8c039-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c039-108">Syntax</span></span>

``` vb
'Declaration
Public Property cbData As Integer
    Get
    Set
'Usage
Dim instance As JET_RETRIEVECOLUMN
Dim value As Integer

value = instance.cbData

instance.cbData = value
```

``` csharp
public int cbData { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="8c039-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8c039-109">Property value</span></span>

<span data-ttu-id="8c039-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="8c039-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8c039-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c039-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8c039-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="8c039-112">Reference</span></span>

[<span data-ttu-id="8c039-113">JET_RETRIEVECOLUMN (clase)</span><span class="sxs-lookup"><span data-stu-id="8c039-113">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="8c039-114">Miembros de JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="8c039-114">JET_RETRIEVECOLUMN members</span></span>](./jet-retrievecolumn-members.md)

[<span data-ttu-id="8c039-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8c039-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
