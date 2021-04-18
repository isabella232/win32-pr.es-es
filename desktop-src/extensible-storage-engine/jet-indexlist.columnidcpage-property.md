---
description: 'Más información acerca de: propiedad JET_INDEXLIST. columnidcPage'
title: Propiedad JET_INDEXLIST. columnidcPage
TOCTitle: 'columnidcPage property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcPage
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist.columnidcpage(v=EXCHG.10)
ms:contentKeyID: 55103616
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcPage
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.set_columnidcPage
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.get_columnidcPage
- Microsoft.Isam.Esent.Interop.JET_INDEXLIST.columnidcPage
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 474ed77a5309da4b48107bcb5477ad9914563709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716611"
---
# <a name="jet_indexlistcolumnidcpage-property"></a><span data-ttu-id="73cc9-103">Propiedad JET_INDEXLIST. columnidcPage</span><span class="sxs-lookup"><span data-stu-id="73cc9-103">JET_INDEXLIST.columnidcPage property</span></span>

<span data-ttu-id="73cc9-104">Obtiene el columnid de la columna de la tabla temporal que almacena el número de páginas del índice.</span><span class="sxs-lookup"><span data-stu-id="73cc9-104">Gets the columnid of the column in the temporary table which stores the number of pages in the index.</span></span> <span data-ttu-id="73cc9-105">Este valor no es actual y solo se actualiza mediante "API. JetComputeStats".</span><span class="sxs-lookup"><span data-stu-id="73cc9-105">This value is not current and is only is updated by "Api.JetComputeStats".</span></span> <span data-ttu-id="73cc9-106">La columna es de tipo [Long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="73cc9-106">The column is of type [Long](./jet-coltyp-enumeration.md).</span></span>

<span data-ttu-id="73cc9-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="73cc9-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="73cc9-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="73cc9-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="73cc9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73cc9-109">Syntax</span></span>

``` vb
'Declaration
Public Property columnidcPage As JET_COLUMNID
    Get
    Friend Set
'Usage
Dim instance As JET_INDEXLIST
Dim value As JET_COLUMNID

value = instance.columnidcPage
```

``` csharp
public JET_COLUMNID columnidcPage { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="73cc9-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="73cc9-110">Property value</span></span>

<span data-ttu-id="73cc9-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="73cc9-111">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="73cc9-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="73cc9-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="73cc9-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="73cc9-113">Reference</span></span>

[<span data-ttu-id="73cc9-114">JET_INDEXLIST (clase)</span><span class="sxs-lookup"><span data-stu-id="73cc9-114">JET_INDEXLIST class</span></span>](./jet-indexlist-class.md)

[<span data-ttu-id="73cc9-115">Miembros de JET_INDEXLIST</span><span class="sxs-lookup"><span data-stu-id="73cc9-115">JET_INDEXLIST members</span></span>](./jet-indexlist-members.md)

[<span data-ttu-id="73cc9-116">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="73cc9-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
