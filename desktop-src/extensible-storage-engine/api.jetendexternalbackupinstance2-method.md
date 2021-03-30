---
description: 'Más información sobre: API. JetEndExternalBackupInstance2 (método)'
title: Método API. JetEndExternalBackupInstance2
TOCTitle: 'JetEndExternalBackupInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetendexternalbackupinstance2(v=EXCHG.10)
ms:contentKeyID: 55100692
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEndExternalBackupInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 71a405c5e0ba3a398071cc317e0d42dd98c4953d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275311"
---
# <a name="apijetendexternalbackupinstance2-method"></a><span data-ttu-id="44ea9-103">Método API. JetEndExternalBackupInstance2</span><span class="sxs-lookup"><span data-stu-id="44ea9-103">Api.JetEndExternalBackupInstance2 method</span></span>

<span data-ttu-id="44ea9-104">Finaliza una sesión de copia de seguridad externa.</span><span class="sxs-lookup"><span data-stu-id="44ea9-104">Ends an external backup session.</span></span> <span data-ttu-id="44ea9-105">Esta API es la última API en una serie de API a las que se debe llamar para ejecutar una copia de seguridad en línea (no basada en VSS) correcta.</span><span class="sxs-lookup"><span data-stu-id="44ea9-105">This API is the last API in a series of APIs that must be called to execute a successful online (non-VSS based) backup.</span></span>

<span data-ttu-id="44ea9-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="44ea9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="44ea9-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="44ea9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="44ea9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44ea9-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEndExternalBackupInstance2 ( _
    instance As JET_INSTANCE, _
    grbit As EndExternalBackupGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As EndExternalBackupGrbitApi.JetEndExternalBackupInstance2(instance, _
    grbit)
```

``` csharp
public static void JetEndExternalBackupInstance2(
    JET_INSTANCE instance,
    EndExternalBackupGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="44ea9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44ea9-109">Parameters</span></span>

  - <span data-ttu-id="44ea9-110">instance</span><span class="sxs-lookup"><span data-stu-id="44ea9-110">instance</span></span>  
    <span data-ttu-id="44ea9-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="44ea9-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="44ea9-112">Instancia para la que se va a finalizar la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="44ea9-112">The instance to end the backup for.</span></span>

<!-- end list -->

  - <span data-ttu-id="44ea9-113">grbit</span><span class="sxs-lookup"><span data-stu-id="44ea9-113">grbit</span></span>  
    <span data-ttu-id="44ea9-114">Tipo: [Microsoft. ISAM. esent. Interop. EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="44ea9-114">Type: [Microsoft.Isam.Esent.Interop.EndExternalBackupGrbit](./endexternalbackupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="44ea9-115">Opciones que especifican cómo finalizó la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="44ea9-115">Options that specify how the backup ended.</span></span>

## <a name="see-also"></a><span data-ttu-id="44ea9-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="44ea9-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="44ea9-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="44ea9-117">Reference</span></span>

[<span data-ttu-id="44ea9-118">Clase de API</span><span class="sxs-lookup"><span data-stu-id="44ea9-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="44ea9-119">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="44ea9-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="44ea9-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="44ea9-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
