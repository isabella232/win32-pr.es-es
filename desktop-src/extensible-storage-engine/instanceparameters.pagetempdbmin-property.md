---
description: 'Más información sobre: InstanceParameters. PageTempDBMin (propiedad)'
title: Propiedad InstanceParameters. PageTempDBMin
TOCTitle: 'PageTempDBMin property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.pagetempdbmin(v=EXCHG.10)
ms:contentKeyID: 55103558
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PageTempDBMin
- Microsoft.Isam.Esent.Interop.InstanceParameters.PageTempDBMin
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06825762485ad52743d585ce0fed86bd1739cd21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716258"
---
# <a name="instanceparameterspagetempdbmin-property"></a><span data-ttu-id="d1349-103">Propiedad InstanceParameters. PageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="d1349-103">InstanceParameters.PageTempDBMin property</span></span>

<span data-ttu-id="d1349-104">Obtiene o establece el tamaño inicial de la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="d1349-104">Gets or sets the initial size of the temporary database.</span></span> <span data-ttu-id="d1349-105">El tamaño está en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="d1349-105">The size is in database pages.</span></span> <span data-ttu-id="d1349-106">Un tamaño de cero indica que se debe usar el tamaño predeterminado de una base de datos normal.</span><span class="sxs-lookup"><span data-stu-id="d1349-106">A size of zero indicates that the default size of an ordinary database should be used.</span></span> <span data-ttu-id="d1349-107">A menudo, es deseable que las aplicaciones pequeñas configuren la base de datos temporal para que sea lo más pequeña posible.</span><span class="sxs-lookup"><span data-stu-id="d1349-107">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="d1349-108">Si se establece este parámetro en [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) , se logrará la base de datos temporal más pequeña posible.</span><span class="sxs-lookup"><span data-stu-id="d1349-108">Setting this parameter to [PageTempDBSmallest](./systemparameters.pagetempdbsmallest-field.md) will achieve the smallest temporary database possible.</span></span>

<span data-ttu-id="d1349-109">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d1349-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d1349-110">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d1349-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d1349-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1349-111">Syntax</span></span>

``` vb
'Declaration
Public Property PageTempDBMin As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PageTempDBMin

instance.PageTempDBMin = value
```

``` csharp
public int PageTempDBMin { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="d1349-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d1349-112">Property value</span></span>

<span data-ttu-id="d1349-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d1349-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="d1349-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1349-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d1349-115">Referencia</span><span class="sxs-lookup"><span data-stu-id="d1349-115">Reference</span></span>

[<span data-ttu-id="d1349-116">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="d1349-116">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="d1349-117">Miembros de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="d1349-117">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="d1349-118">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d1349-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
