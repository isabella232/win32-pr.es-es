---
description: 'Más información sobre: InstanceParameters. WaypointLatency (propiedad)'
title: Propiedad InstanceParameters. WaypointLatency
TOCTitle: 'WaypointLatency property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.waypointlatency(v=EXCHG.10)
ms:contentKeyID: 55103325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_WaypointLatency
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d7d837d7fff804926529ec67780e319d85031f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707380"
---
# <a name="instanceparameterswaypointlatency-property"></a><span data-ttu-id="3a1c3-103">Propiedad InstanceParameters. WaypointLatency</span><span class="sxs-lookup"><span data-stu-id="3a1c3-103">InstanceParameters.WaypointLatency property</span></span>

<span data-ttu-id="3a1c3-104">Obtiene o establece el número de registros que esent aplazará los vaciados de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-104">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="3a1c3-105">Se puede usar para aumentar la capacidad de recuperación de la base de datos si los errores provocan la pérdida de los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-105">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="3a1c3-106">Compatible con Windows 7 y up.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-106">Supported on Windows 7 and up.</span></span> <span data-ttu-id="3a1c3-107">Se omite en Windows XP, Windows Server 2003, Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3a1c3-107">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="3a1c3-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3a1c3-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3a1c3-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3a1c3-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1c3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a1c3-110">Syntax</span></span>

``` vb
'Declaration
Public Property WaypointLatency As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.WaypointLatency

instance.WaypointLatency = value
```

``` csharp
public int WaypointLatency { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="3a1c3-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3a1c3-111">Property value</span></span>

<span data-ttu-id="3a1c3-112">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3a1c3-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="3a1c3-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a1c3-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3a1c3-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="3a1c3-114">Reference</span></span>

[<span data-ttu-id="3a1c3-115">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="3a1c3-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="3a1c3-116">Miembros de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="3a1c3-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="3a1c3-117">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3a1c3-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
