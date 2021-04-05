---
description: 'Más información acerca de: propiedad JET_OPENTEMPORARYTABLE. prgcolumnid'
title: Propiedad JET_OPENTEMPORARYTABLE. prgcolumnid (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'prgcolumnid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.prgcolumnid(v=EXCHG.10)
ms:contentKeyID: 55104133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_prgcolumnid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumnid
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd6516e01d08de32f7962a48d2caca69ddbf0427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002898"
---
# <a name="jet_opentemporarytableprgcolumnid-property"></a><span data-ttu-id="b3716-103">Propiedad JET_OPENTEMPORARYTABLE. prgcolumnid</span><span class="sxs-lookup"><span data-stu-id="b3716-103">JET_OPENTEMPORARYTABLE.prgcolumnid property</span></span>

<span data-ttu-id="b3716-104">Obtiene o establece el búfer de salida que recibe la matriz de identificadores de columna generados durante la creación de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="b3716-104">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="b3716-105">Los identificadores de columna de esta matriz se corresponden exactamente con la matriz de entrada de definiciones de columna.</span><span class="sxs-lookup"><span data-stu-id="b3716-105">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="b3716-106">Como resultado, el tamaño de este búfer debe corresponder al tamaño de [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md).</span><span class="sxs-lookup"><span data-stu-id="b3716-106">As a result, the size of this buffer must correspond to the size of [prgcolumndef](./jet-opentemporarytable.prgcolumndef-property.md).</span></span>

<span data-ttu-id="b3716-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b3716-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="b3716-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b3716-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b3716-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3716-109">Syntax</span></span>

``` vb
'Declaration
Public Property prgcolumnid As JET_COLUMNID()
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_COLUMNID()

value = instance.prgcolumnid

instance.prgcolumnid = value
```

``` csharp
public JET_COLUMNID[] prgcolumnid { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="b3716-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b3716-110">Property value</span></span>

<span data-ttu-id="b3716-111">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="b3716-111">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="b3716-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3716-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b3716-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="b3716-113">Reference</span></span>

[<span data-ttu-id="b3716-114">JET_OPENTEMPORARYTABLE (clase)</span><span class="sxs-lookup"><span data-stu-id="b3716-114">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="b3716-115">Miembros de JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="b3716-115">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="b3716-116">Espacio de nombres Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="b3716-116">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
