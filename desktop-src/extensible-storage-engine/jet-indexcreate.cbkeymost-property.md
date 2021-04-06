---
description: 'Más información acerca de: propiedad JET_INDEXCREATE. cbKeyMost'
title: Propiedad JET_INDEXCREATE. cbKeyMost
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 321704f88da59af33f4dab99d7d681fbcbd96e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911465"
---
# <a name="jet_indexcreatecbkeymost-property"></a><span data-ttu-id="b04f4-103">Propiedad JET_INDEXCREATE. cbKeyMost</span><span class="sxs-lookup"><span data-stu-id="b04f4-103">JET_INDEXCREATE.cbKeyMost property</span></span>

<span data-ttu-id="b04f4-104">Obtiene o establece el tamaño máximo permitido, en bytes, para las claves del índice.</span><span class="sxs-lookup"><span data-stu-id="b04f4-104">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="b04f4-105">El tamaño máximo de clave compatible mínimo es JET_cbKeyMostMin (255), que es el tamaño de clave máximo heredado.</span><span class="sxs-lookup"><span data-stu-id="b04f4-105">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="b04f4-106">El tamaño máximo de la clave depende del tamaño de página de la base de datos [DatabasePageSize](./jet-param-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="b04f4-106">The maximum key size is dependent on the database page size [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="b04f4-107">El tamaño máximo de la clave se puede recuperar con [KeyMost](./systemparameters.keymost-property.md).</span><span class="sxs-lookup"><span data-stu-id="b04f4-107">The maximum key size can be retrieved with [KeyMost](./systemparameters.keymost-property.md).</span></span> <span data-ttu-id="b04f4-108">Este parámetro se omite en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b04f4-108">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b04f4-109">A diferencia de la API no administrada, **IndexKeyMost ()** (JET_bitIndexKeyMost) no es necesario, sino que se agregará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="b04f4-109">Unlike the unmanaged API, **IndexKeyMost()** (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span>

<span data-ttu-id="b04f4-110">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b04f4-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b04f4-111">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b04f4-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b04f4-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b04f4-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="b04f4-113">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b04f4-113">Property value</span></span>

<span data-ttu-id="b04f4-114">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b04f4-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b04f4-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="b04f4-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b04f4-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="b04f4-116">Reference</span></span>

[<span data-ttu-id="b04f4-117">JET_INDEXCREATE (clase)</span><span class="sxs-lookup"><span data-stu-id="b04f4-117">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="b04f4-118">Miembros de JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="b04f4-118">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="b04f4-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b04f4-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
