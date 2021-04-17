---
description: 'Más información sobre: InstanceParameters. CircularLog (propiedad)'
title: Propiedad InstanceParameters. CircularLog
TOCTitle: 'CircularLog property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.circularlog(v=EXCHG.10)
ms:contentKeyID: 55103320
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CircularLog
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f9a77aa0d0f60b49269dc939787b165a3f2f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717250"
---
# <a name="instanceparameterscircularlog-property"></a><span data-ttu-id="aa0b3-103">Propiedad InstanceParameters. CircularLog</span><span class="sxs-lookup"><span data-stu-id="aa0b3-103">InstanceParameters.CircularLog property</span></span>

<span data-ttu-id="aa0b3-104">Obtiene o establece un valor que indica si el registro circular está activado.</span><span class="sxs-lookup"><span data-stu-id="aa0b3-104">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="aa0b3-105">Cuando el registro circular está desactivado, todos los archivos de registro de transacciones que se generan se conservan en el disco hasta que ya no son necesarios porque se ha realizado una copia de seguridad completa de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="aa0b3-105">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="aa0b3-106">Cuando el registro circular está activado, solo se conservan en el disco los archivos de registro de transacciones que son más jóvenes que el punto de control actual.</span><span class="sxs-lookup"><span data-stu-id="aa0b3-106">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="aa0b3-107">La ventaja de este modo es que las copias de seguridad no son necesarias para retirar los archivos de registro de transacciones antiguos.</span><span class="sxs-lookup"><span data-stu-id="aa0b3-107">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span>

<span data-ttu-id="aa0b3-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aa0b3-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aa0b3-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aa0b3-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aa0b3-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa0b3-110">Syntax</span></span>

``` vb
'Declaration
Public Property CircularLog As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CircularLog

instance.CircularLog = value
```

``` csharp
public bool CircularLog { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="aa0b3-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="aa0b3-111">Property value</span></span>

<span data-ttu-id="aa0b3-112">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="aa0b3-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="aa0b3-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa0b3-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aa0b3-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="aa0b3-114">Reference</span></span>

[<span data-ttu-id="aa0b3-115">Clase InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="aa0b3-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="aa0b3-116">Miembros de InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="aa0b3-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="aa0b3-117">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="aa0b3-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
