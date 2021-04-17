---
description: 'Más información sobre: InstanceParameters. PreferredVerPages (propiedad)'
title: Propiedad InstanceParameters. PreferredVerPages
TOCTitle: 'PreferredVerPages property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.preferredverpages(v=EXCHG.10)
ms:contentKeyID: 55103322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.PreferredVerPages
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_PreferredVerPages
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 067d41cd3fb945b2f18d3cd6154b1eef6793b1e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716256"
---
# <a name="instanceparameterspreferredverpages-property"></a><span data-ttu-id="f98e7-103">Propiedad InstanceParameters. PreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="f98e7-103">InstanceParameters.PreferredVerPages property</span></span>

<span data-ttu-id="f98e7-104">Obtiene o establece el número preferido de páginas del almacén de versiones reservadas para esta instancia.</span><span class="sxs-lookup"><span data-stu-id="f98e7-104">Gets or sets the preferred number of version store pages reserved for this instance.</span></span> <span data-ttu-id="f98e7-105">Si el tamaño del almacén de versiones supera este umbral, cualquier información que solo se use para tareas en segundo plano opcionales, como la recuperación del espacio eliminado en la base de datos, se sacrifica en su lugar para conservar el espacio para la información transaccional.</span><span class="sxs-lookup"><span data-stu-id="f98e7-105">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="f98e7-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f98e7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f98e7-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f98e7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f98e7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f98e7-108">Syntax</span></span>

``` vb
'Declaration
Public Property PreferredVerPages As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.PreferredVerPages

instance.PreferredVerPages = value
```

``` csharp
public int PreferredVerPages { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="f98e7-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f98e7-109">Property value</span></span>

<span data-ttu-id="f98e7-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f98e7-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f98e7-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="f98e7-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f98e7-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="f98e7-112">Reference</span></span>

[<span data-ttu-id="f98e7-113">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="f98e7-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="f98e7-114">Miembros de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="f98e7-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="f98e7-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f98e7-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
