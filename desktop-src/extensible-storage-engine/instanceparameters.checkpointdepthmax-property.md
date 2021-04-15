---
description: 'Más información sobre: InstanceParameters. CheckpointDepthMax (propiedad)'
title: Propiedad InstanceParameters. CheckpointDepthMax
TOCTitle: 'CheckpointDepthMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.checkpointdepthmax(v=EXCHG.10)
ms:contentKeyID: 55103294
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3addab0356206577eda22119ddce81721e9c2bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715542"
---
# <a name="instanceparameterscheckpointdepthmax-property"></a><span data-ttu-id="572a5-103">Propiedad InstanceParameters. CheckpointDepthMax</span><span class="sxs-lookup"><span data-stu-id="572a5-103">InstanceParameters.CheckpointDepthMax property</span></span>

<span data-ttu-id="572a5-104">Obtiene o establece el umbral en bytes para el número de archivos de registro de transacciones que se deben reproducir después de un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="572a5-104">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="572a5-105">Si el registro circular está habilitado mediante CircularLog, este parámetro también controlará la cantidad aproximada de archivos de registro de transacciones que se conservarán en el disco.</span><span class="sxs-lookup"><span data-stu-id="572a5-105">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="572a5-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="572a5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="572a5-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="572a5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="572a5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="572a5-108">Syntax</span></span>

``` vb
'Declaration
Public Property CheckpointDepthMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CheckpointDepthMax

instance.CheckpointDepthMax = value
```

``` csharp
public int CheckpointDepthMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="572a5-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="572a5-109">Property value</span></span>

<span data-ttu-id="572a5-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="572a5-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="572a5-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="572a5-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="572a5-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="572a5-112">Reference</span></span>

[<span data-ttu-id="572a5-113">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="572a5-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="572a5-114">Miembros de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="572a5-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="572a5-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="572a5-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
