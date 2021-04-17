---
description: 'Más información sobre: InstanceParameters. LogBuffers (propiedad)'
title: Propiedad InstanceParameters. LogBuffers
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f58e43ea38792549d384328dc0fd6c5d31616e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706907"
---
# <a name="instanceparameterslogbuffers-property"></a><span data-ttu-id="6a7dc-103">Propiedad InstanceParameters. LogBuffers</span><span class="sxs-lookup"><span data-stu-id="6a7dc-103">InstanceParameters.LogBuffers property</span></span>

<span data-ttu-id="6a7dc-104">Obtiene o establece la cantidad de memoria que se usa para almacenar en memoria caché las entradas del registro antes de que se escriban en el archivo de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-104">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="6a7dc-105">La unidad para este parámetro es el tamaño de sector del volumen que contiene los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-105">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="6a7dc-106">El tamaño del sector es casi siempre de 512 bytes, por lo que es seguro suponer ese tamaño para la unidad.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-106">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="6a7dc-107">Este parámetro afecta al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-107">This parameter has an impact on performance.</span></span> <span data-ttu-id="6a7dc-108">Cuando el motor de base de datos está sometido a una carga de actualización pesada, este búfer puede llenarse con mucha rapidez.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-108">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="6a7dc-109">Un tamaño de caché mayor para el archivo de registro de transacciones es fundamental para un buen rendimiento de actualización en una condición de carga elevada.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-109">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="6a7dc-110">Se sabe que el valor predeterminado es demasiado pequeño para este caso.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-110">The default is known to be too small for this case.</span></span> <span data-ttu-id="6a7dc-111">No establezca este parámetro en un número de búferes mayor (en bytes) de la mitad del tamaño de un archivo de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="6a7dc-111">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<span data-ttu-id="6a7dc-112">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a7dc-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a7dc-113">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6a7dc-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a7dc-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a7dc-114">Syntax</span></span>

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="6a7dc-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6a7dc-115">Property value</span></span>

<span data-ttu-id="6a7dc-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6a7dc-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="6a7dc-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a7dc-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a7dc-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="6a7dc-118">Reference</span></span>

[<span data-ttu-id="6a7dc-119">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="6a7dc-119">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="6a7dc-120">Miembros de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="6a7dc-120">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="6a7dc-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6a7dc-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
