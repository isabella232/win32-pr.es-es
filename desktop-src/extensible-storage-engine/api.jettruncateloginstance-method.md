---
description: 'Más información sobre: API. JetTruncateLogInstance (método)'
title: Método API. JetTruncateLogInstance
TOCTitle: 'JetTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jettruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55100815
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc1693b3f84cd594bfeca81a8e854e49e28d955f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003002"
---
# <a name="apijettruncateloginstance-method"></a><span data-ttu-id="af91c-103">Método API. JetTruncateLogInstance</span><span class="sxs-lookup"><span data-stu-id="af91c-103">Api.JetTruncateLogInstance method</span></span>

<span data-ttu-id="af91c-104">Se usa durante una copia de seguridad iniciada por JetBeginExternalBackup para eliminar los archivos de registro de transacciones que ya no se necesitarán una vez que la copia de seguridad actual se complete correctamente.</span><span class="sxs-lookup"><span data-stu-id="af91c-104">Used during a backup initiated by JetBeginExternalBackup to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="af91c-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="af91c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="af91c-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="af91c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="af91c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af91c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTruncateLogInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetTruncateLogInstance(instance)
```

``` csharp
public static void JetTruncateLogInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="af91c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af91c-108">Parameters</span></span>

  - <span data-ttu-id="af91c-109">instance</span><span class="sxs-lookup"><span data-stu-id="af91c-109">instance</span></span>  
    <span data-ttu-id="af91c-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="af91c-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="af91c-111">Instancia de que se va a truncar.</span><span class="sxs-lookup"><span data-stu-id="af91c-111">The instance to truncate.</span></span>

## <a name="see-also"></a><span data-ttu-id="af91c-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="af91c-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="af91c-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="af91c-113">Reference</span></span>

[<span data-ttu-id="af91c-114">Clase de API</span><span class="sxs-lookup"><span data-stu-id="af91c-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="af91c-115">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="af91c-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="af91c-116">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="af91c-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
