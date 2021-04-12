---
description: 'Más información sobre: API. JetStopBackupInstance (método)'
title: Método API. JetStopBackupInstance
TOCTitle: 'JetStopBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetStopBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetstopbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55100825
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetStopBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetStopBackupInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69b6b98b21dba4cffb37827b2965b4e62197121f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279272"
---
# <a name="apijetstopbackupinstance-method"></a><span data-ttu-id="0f071-103">Método API. JetStopBackupInstance</span><span class="sxs-lookup"><span data-stu-id="0f071-103">Api.JetStopBackupInstance method</span></span>

<span data-ttu-id="0f071-104">Impide que la actividad relacionada con la copia de seguridad de secuencias continúe en una instancia en ejecución específica, con lo que finaliza la copia de seguridad de streaming de una manera predecible.</span><span class="sxs-lookup"><span data-stu-id="0f071-104">Prevents streaming backup-related activity from continuing on a specific running instance, thus ending the streaming backup in a predictable way.</span></span>

<span data-ttu-id="0f071-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0f071-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0f071-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0f071-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0f071-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f071-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetStopBackupInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetStopBackupInstance(instance)
```

``` csharp
public static void JetStopBackupInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="0f071-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f071-108">Parameters</span></span>

  - <span data-ttu-id="0f071-109">instance</span><span class="sxs-lookup"><span data-stu-id="0f071-109">instance</span></span>  
    <span data-ttu-id="0f071-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0f071-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="0f071-111">La instancia de que se utilizará.</span><span class="sxs-lookup"><span data-stu-id="0f071-111">The instance to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f071-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f071-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0f071-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="0f071-113">Reference</span></span>

[<span data-ttu-id="0f071-114">Clase de API</span><span class="sxs-lookup"><span data-stu-id="0f071-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0f071-115">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="0f071-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0f071-116">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0f071-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
