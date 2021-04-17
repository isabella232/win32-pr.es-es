---
description: 'Más información sobre: InstanceParameters. LogFileSize (propiedad)'
title: Propiedad InstanceParameters. LogFileSize
TOCTitle: 'LogFileSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logfilesize(v=EXCHG.10)
ms:contentKeyID: 55103312
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogFileSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c141c76a92f49b4b5000cad65e302a7cf15d780f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706739"
---
# <a name="instanceparameterslogfilesize-property"></a><span data-ttu-id="e12b2-103">Propiedad InstanceParameters. LogFileSize</span><span class="sxs-lookup"><span data-stu-id="e12b2-103">InstanceParameters.LogFileSize property</span></span>

<span data-ttu-id="e12b2-104">Obtiene o establece el tamaño de los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="e12b2-104">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="e12b2-105">Este parámetro debe establecerse en unidades de 1024 bytes (por ejemplo, un valor de 2048 proporcionará 2 MB de archivo de registro).</span><span class="sxs-lookup"><span data-stu-id="e12b2-105">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span>

<span data-ttu-id="e12b2-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e12b2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e12b2-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e12b2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e12b2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e12b2-108">Syntax</span></span>

``` vb
'Declaration
Public Property LogFileSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogFileSize

instance.LogFileSize = value
```

``` csharp
public int LogFileSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e12b2-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e12b2-109">Property value</span></span>

<span data-ttu-id="e12b2-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e12b2-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="e12b2-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="e12b2-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e12b2-112">Referencia</span><span class="sxs-lookup"><span data-stu-id="e12b2-112">Reference</span></span>

[<span data-ttu-id="e12b2-113">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="e12b2-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="e12b2-114">Miembros de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="e12b2-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="e12b2-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e12b2-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
