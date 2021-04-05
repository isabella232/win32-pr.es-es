---
description: 'Más información sobre: API. JetInit (método)'
title: Método API. JetInit
TOCTitle: 'JetInit method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetInit(Microsoft.Isam.Esent.Interop.JET_INSTANCE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetinit(v=EXCHG.10)
ms:contentKeyID: 55100760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetInit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetInit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27b0ad5fa640b853b46cd39ae595a1f486812adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913357"
---
# <a name="apijetinit-method"></a><span data-ttu-id="042c2-103">Método API. JetInit</span><span class="sxs-lookup"><span data-stu-id="042c2-103">Api.JetInit method</span></span>

<span data-ttu-id="042c2-104">Inicialice el motor de base de datos ESENT.</span><span class="sxs-lookup"><span data-stu-id="042c2-104">Initialize the ESENT database engine.</span></span>

<span data-ttu-id="042c2-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="042c2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="042c2-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="042c2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="042c2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="042c2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetInit ( _
    ByRef instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetInit(instance)
```

``` csharp
public static void JetInit(
    ref JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="042c2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="042c2-108">Parameters</span></span>

  - <span data-ttu-id="042c2-109">instance</span><span class="sxs-lookup"><span data-stu-id="042c2-109">instance</span></span>  
    <span data-ttu-id="042c2-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="042c2-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="042c2-111">Instancia de que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="042c2-111">The instance to initialize.</span></span> <span data-ttu-id="042c2-112">Si no se ha asignado una instancia, se crea una nueva y el motor funcionará en modo de instancia única.</span><span class="sxs-lookup"><span data-stu-id="042c2-112">If an instance hasn't been allocated then a new one is created and the engine will operate in single-instance mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="042c2-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="042c2-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="042c2-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="042c2-114">Reference</span></span>

[<span data-ttu-id="042c2-115">Clase de API</span><span class="sxs-lookup"><span data-stu-id="042c2-115">Api class</span></span>](./api-class.md)

[<span data-ttu-id="042c2-116">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="042c2-116">Api members</span></span>](./api-members.md)

[<span data-ttu-id="042c2-117">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="042c2-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
