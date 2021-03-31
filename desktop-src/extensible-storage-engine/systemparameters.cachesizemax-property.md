---
description: 'Más información sobre: SystemParameters. CacheSizeMax (propiedad)'
title: Propiedad SystemParameters. CacheSizeMax
TOCTitle: 'CacheSizeMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.cachesizemax(v=EXCHG.10)
ms:contentKeyID: 55104037
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.get_CacheSizeMax
- Microsoft.Isam.Esent.Interop.SystemParameters.CacheSizeMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7b03df288a0263cf6b79281f5ed79330dfd641d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278933"
---
# <a name="systemparameterscachesizemax-property"></a><span data-ttu-id="81f2c-103">Propiedad SystemParameters. CacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="81f2c-103">SystemParameters.CacheSizeMax property</span></span>

<span data-ttu-id="81f2c-104">Obtiene o establece el tamaño máximo de la memoria caché de páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="81f2c-104">Gets or sets the maximum size of the database page cache.</span></span> <span data-ttu-id="81f2c-105">El tamaño está en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="81f2c-105">The size is in database pages.</span></span> <span data-ttu-id="81f2c-106">Si este parámetro se deja en su valor predeterminado, el tamaño máximo de la memoria caché se establecerá en el tamaño de la memoria física cuando se llame a JetInit.</span><span class="sxs-lookup"><span data-stu-id="81f2c-106">If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when JetInit is called.</span></span>

<span data-ttu-id="81f2c-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="81f2c-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="81f2c-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="81f2c-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="81f2c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81f2c-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Property CacheSizeMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.CacheSizeMax

SystemParameters.CacheSizeMax = value
```

``` csharp
public static int CacheSizeMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="81f2c-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="81f2c-110">Property value</span></span>

<span data-ttu-id="81f2c-111">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="81f2c-111">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="81f2c-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="81f2c-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="81f2c-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="81f2c-113">Reference</span></span>

[<span data-ttu-id="81f2c-114">SystemParameters (clase)</span><span class="sxs-lookup"><span data-stu-id="81f2c-114">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="81f2c-115">Miembros de SystemParameters</span><span class="sxs-lookup"><span data-stu-id="81f2c-115">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="81f2c-116">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="81f2c-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
