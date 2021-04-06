---
description: 'Más información sobre: API. JetEndExternalBackupInstance (método)'
title: Método API. JetEndExternalBackupInstance
TOCTitle: 'JetEndExternalBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100691
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16ec4dc235f677ba42b4ae3bae10a79b9d494576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001022"
---
# <a name="apijetendexternalbackupinstance-method"></a><span data-ttu-id="b9797-103">Método API. JetEndExternalBackupInstance</span><span class="sxs-lookup"><span data-stu-id="b9797-103">Api.JetEndExternalBackupInstance method</span></span>

<span data-ttu-id="b9797-104">Finaliza una sesión de copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="b9797-104">Ends an external backup session.</span></span> <span data-ttu-id="b9797-105">Esta API es la última API en una serie de API a las que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta.</span><span class="sxs-lookup"><span data-stu-id="b9797-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="b9797-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b9797-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b9797-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b9797-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b9797-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9797-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetEndExternalBackupInstance(instance)
```

``` csharp
public static void JetEndExternalBackupInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="b9797-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9797-109">Parameters</span></span>

  - <span data-ttu-id="b9797-110">instance</span><span class="sxs-lookup"><span data-stu-id="b9797-110">instance</span></span>  
    <span data-ttu-id="b9797-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b9797-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="b9797-112">Instancia para la que se va a finalizar la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b9797-112">The instance to end the backup for.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9797-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9797-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b9797-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="b9797-114">Reference</span></span>

[<span data-ttu-id="b9797-115">Clase de API</span><span class="sxs-lookup"><span data-stu-id="b9797-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b9797-116">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="b9797-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b9797-117">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b9797-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
