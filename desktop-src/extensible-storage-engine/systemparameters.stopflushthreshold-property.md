---
description: 'Más información sobre: SystemParameters. StopFlushThreshold (propiedad)'
title: Propiedad SystemParameters. StopFlushThreshold
TOCTitle: 'StopFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.stopflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b79a9e5894de6539e8ab7dc0db4218b5f6cb3bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361192"
---
# <a name="systemparametersstopflushthreshold-property"></a><span data-ttu-id="f7179-103">Propiedad SystemParameters. StopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="f7179-103">SystemParameters.StopFlushThreshold property</span></span>

<span data-ttu-id="f7179-104">Obtiene o establece el umbral en el que la caché de páginas de base de datos termina la expulsión de las páginas de la memoria caché para dejar espacio a las páginas que no están almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="f7179-104">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="f7179-105">Cuando el número de búferes de página de la memoria caché supera este umbral, se detiene el proceso en segundo plano que se inició para reponer el grupo de búferes disponibles.</span><span class="sxs-lookup"><span data-stu-id="f7179-105">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="f7179-106">Este umbral siempre es relativo al tamaño máximo de la memoria caché establecido por JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="f7179-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="f7179-107">Este umbral también debe ser siempre mayor que el umbral de inicio establecido por JET_paramStartFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="f7179-107">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="f7179-108">La distancia entre el umbral de inicio y el umbral de detención afecta a la eficacia con la que el proceso en segundo plano vacía las páginas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f7179-108">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="f7179-109">Una brecha más grande hará que sea más probable que se combinen las escrituras en páginas vecinas.</span><span class="sxs-lookup"><span data-stu-id="f7179-109">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="f7179-110">Sin embargo, un umbral de detención alta reducirá el tamaño efectivo de la caché de páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="f7179-110">However, a high stop threshold will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="f7179-111">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f7179-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f7179-112">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f7179-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f7179-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7179-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StopFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StopFlushThreshold

SystemParameters.StopFlushThreshold = value
```

``` csharp
public static int StopFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="f7179-114">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f7179-114">Property value</span></span>

<span data-ttu-id="f7179-115">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f7179-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f7179-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7179-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f7179-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="f7179-117">Reference</span></span>

[<span data-ttu-id="f7179-118">SystemParameters (clase)</span><span class="sxs-lookup"><span data-stu-id="f7179-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="f7179-119">Miembros de SystemParameters</span><span class="sxs-lookup"><span data-stu-id="f7179-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="f7179-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f7179-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
