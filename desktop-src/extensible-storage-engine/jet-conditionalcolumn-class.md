---
description: 'Más información sobre: JET_CONDITIONALCOLUMN (clase)'
title: JET_CONDITIONALCOLUMN (clase)
TOCTitle: JET_CONDITIONALCOLUMN class
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_conditionalcolumn(v=EXCHG.10)
ms:contentKeyID: 55107506
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23b116ce88b24702711d74f610c208a72c44addf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002421"
---
# <a name="jet_conditionalcolumn-class"></a><span data-ttu-id="59c48-103">JET_CONDITIONALCOLUMN (clase)</span><span class="sxs-lookup"><span data-stu-id="59c48-103">JET_CONDITIONALCOLUMN class</span></span>

<span data-ttu-id="59c48-104">Define cómo se realiza la indización condicional para un índice determinado.</span><span class="sxs-lookup"><span data-stu-id="59c48-104">Defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="59c48-105">Un índice condicional solo contiene una entrada de índice para las filas que coincidan con la condición especificada.</span><span class="sxs-lookup"><span data-stu-id="59c48-105">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="59c48-106">Sin embargo, la columna condicional no forma parte de la clave del índice, sino que solo controla la presencia de la entrada de índice.</span><span class="sxs-lookup"><span data-stu-id="59c48-106">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="59c48-107">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="59c48-107">Inheritance hierarchy</span></span>

[<span data-ttu-id="59c48-108">System.Object</span><span class="sxs-lookup"><span data-stu-id="59c48-108">System.Object</span></span>](/dotnet/api/system.object)  
  <span data-ttu-id="59c48-109">Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="59c48-109">Microsoft.Isam.Esent.Interop.JET_CONDITIONALCOLUMN</span></span>  

<span data-ttu-id="59c48-110">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="59c48-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="59c48-111">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="59c48-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="59c48-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59c48-112">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class JET_CONDITIONALCOLUMN _
    Implements IContentEquatable(Of JET_CONDITIONALCOLUMN), IDeepCloneable(Of JET_CONDITIONALCOLUMN)
'Usage
Dim instance As JET_CONDITIONALCOLUMN
```

``` csharp
[SerializableAttribute]
public sealed class JET_CONDITIONALCOLUMN : IContentEquatable<JET_CONDITIONALCOLUMN>, 
    IDeepCloneable<JET_CONDITIONALCOLUMN>
```

## <a name="thread-safety"></a><span data-ttu-id="59c48-113">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="59c48-113">Thread safety</span></span>

<span data-ttu-id="59c48-114">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="59c48-114">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="59c48-115">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="59c48-115">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="59c48-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="59c48-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="59c48-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="59c48-117">Reference</span></span>

[<span data-ttu-id="59c48-118">Miembros de JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="59c48-118">JET_CONDITIONALCOLUMN members</span></span>](./jet-conditionalcolumn-members.md)

[<span data-ttu-id="59c48-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="59c48-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
