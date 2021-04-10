---
description: 'Más información sobre: API. JetBackupInstance (método)'
title: Método API. JetBackupInstance
TOCTitle: 'JetBackupInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBackupInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.BackupGrbit,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbackupinstance(v=EXCHG.10)
ms:contentKeyID: 55107221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBackupInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73c5b44f1f0b69aaed6066635ad4e82690bc3c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153716"
---
# <a name="apijetbackupinstance-method"></a><span data-ttu-id="10b01-103">Método API. JetBackupInstance</span><span class="sxs-lookup"><span data-stu-id="10b01-103">Api.JetBackupInstance method</span></span>

<span data-ttu-id="10b01-104">Realiza una copia de seguridad de secuencias de una instancia, incluidas todas las bases de datos adjuntas, en un directorio.</span><span class="sxs-lookup"><span data-stu-id="10b01-104">Performs a streaming backup of an instance, including all the attached databases, to a directory.</span></span> <span data-ttu-id="10b01-105">Con varios métodos de copia de seguridad admitidos por el motor de, esta es la función más sencilla y encapsulada.</span><span class="sxs-lookup"><span data-stu-id="10b01-105">With multiple backup methods supported by the engine, this is the simplest and most encapsulated function.</span></span>

<span data-ttu-id="10b01-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="10b01-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="10b01-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="10b01-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="10b01-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10b01-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBackupInstance ( _
    instance As JET_INSTANCE, _
    destination As String, _
    grbit As BackupGrbit, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim destination As String
Dim grbit As BackupGrbit
Dim statusCallback As JET_PFNSTATUSApi.JetBackupInstance(instance, _
    destination, grbit, statusCallback)
```

``` csharp
public static void JetBackupInstance(
    JET_INSTANCE instance,
    string destination,
    BackupGrbit grbit,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="10b01-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10b01-109">Parameters</span></span>

  - <span data-ttu-id="10b01-110">instance</span><span class="sxs-lookup"><span data-stu-id="10b01-110">instance</span></span>  
    <span data-ttu-id="10b01-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="10b01-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="10b01-112">Instancia de que se va a hacer copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="10b01-112">The instance to backup.</span></span>

<!-- end list -->

  - <span data-ttu-id="10b01-113">destination</span><span class="sxs-lookup"><span data-stu-id="10b01-113">destination</span></span>  
    <span data-ttu-id="10b01-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="10b01-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="10b01-115">Directorio en el que se va a almacenar la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="10b01-115">The directory where the backup is to be stored.</span></span> <span data-ttu-id="10b01-116">Si la ruta de acceso de copia de seguridad es null para usar la función, truncará los registros, si es posible.</span><span class="sxs-lookup"><span data-stu-id="10b01-116">If the backup path is null to use the function will truncate the logs, if possible.</span></span>

<!-- end list -->

  - <span data-ttu-id="10b01-117">grbit</span><span class="sxs-lookup"><span data-stu-id="10b01-117">grbit</span></span>  
    <span data-ttu-id="10b01-118">Tipo: [Microsoft. ISAM. esent. Interop. BackupGrbit](./backupgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="10b01-118">Type: [Microsoft.Isam.Esent.Interop.BackupGrbit](./backupgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="10b01-119">Opciones de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="10b01-119">Backup options.</span></span>

<!-- end list -->

  - <span data-ttu-id="10b01-120">statusCallback</span><span class="sxs-lookup"><span data-stu-id="10b01-120">statusCallback</span></span>  
    <span data-ttu-id="10b01-121">Tipo: [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="10b01-121">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="10b01-122">Devolución de llamada de notificación de estado opcional.</span><span class="sxs-lookup"><span data-stu-id="10b01-122">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="10b01-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="10b01-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="10b01-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="10b01-124">Reference</span></span>

[<span data-ttu-id="10b01-125">Clase de API</span><span class="sxs-lookup"><span data-stu-id="10b01-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="10b01-126">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="10b01-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="10b01-127">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="10b01-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
