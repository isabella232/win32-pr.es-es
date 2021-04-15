---
description: 'Más información sobre: API. JetRestoreInstance (método)'
title: Método API. JetRestoreInstance
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e2c2976eb8bf661dc53bdc86723bb21309ab973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696305"
---
# <a name="apijetrestoreinstance-method"></a><span data-ttu-id="6dd2c-103">Método API. JetRestoreInstance</span><span class="sxs-lookup"><span data-stu-id="6dd2c-103">Api.JetRestoreInstance method</span></span>

<span data-ttu-id="6dd2c-104">Restaura y recupera una copia de seguridad de streaming de una instancia de, incluidas todas las bases de datos adjuntas.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-104">Restores and recovers a streaming backup of an instance including all the attached databases.</span></span> <span data-ttu-id="6dd2c-105">Está diseñado para trabajar con una copia de seguridad creada con la función [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) .</span><span class="sxs-lookup"><span data-stu-id="6dd2c-105">It is designed to work with a backup created with the [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md) function.</span></span> <span data-ttu-id="6dd2c-106">Esta es la función de restauración más sencilla y encapsulada.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-106">This is the simplest and most encapsulated restore function.</span></span>

<span data-ttu-id="6dd2c-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6dd2c-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6dd2c-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6dd2c-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd2c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6dd2c-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a><span data-ttu-id="6dd2c-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6dd2c-110">Parameters</span></span>

  - <span data-ttu-id="6dd2c-111">instance</span><span class="sxs-lookup"><span data-stu-id="6dd2c-111">instance</span></span>  
    <span data-ttu-id="6dd2c-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6dd2c-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="6dd2c-113">La instancia de que se utilizará.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-113">The instance to use.</span></span> <span data-ttu-id="6dd2c-114">La instancia no se debe inicializar.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-114">The instance should not be initialized.</span></span> <span data-ttu-id="6dd2c-115">Al restaurar los archivos se inicializará la instancia.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-115">Restoring the files will initialize the instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="6dd2c-116">source</span><span class="sxs-lookup"><span data-stu-id="6dd2c-116">source</span></span>  
    <span data-ttu-id="6dd2c-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6dd2c-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6dd2c-118">Ubicación de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-118">Location of the backup.</span></span> <span data-ttu-id="6dd2c-119">La copia de seguridad se debe haber creado con [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="6dd2c-119">The backup should have been created with [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).</span></span>

<!-- end list -->

  - <span data-ttu-id="6dd2c-120">destination</span><span class="sxs-lookup"><span data-stu-id="6dd2c-120">destination</span></span>  
    <span data-ttu-id="6dd2c-121">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6dd2c-121">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6dd2c-122">Nombre de la carpeta donde se copiarán y recuperarán los archivos de base de datos del conjunto de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-122">Name of the folder where the database files from the backup set will be copied and recovered.</span></span> <span data-ttu-id="6dd2c-123">Si se establece en null, los archivos de base de datos se copiarán y recuperarán en su ubicación original.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-123">If this is set to null, the database files will be copied and recovered to their original location.</span></span>

<!-- end list -->

  - <span data-ttu-id="6dd2c-124">statusCallback</span><span class="sxs-lookup"><span data-stu-id="6dd2c-124">statusCallback</span></span>  
    <span data-ttu-id="6dd2c-125">Tipo: [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="6dd2c-125">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="6dd2c-126">Devolución de llamada de notificación de estado opcional.</span><span class="sxs-lookup"><span data-stu-id="6dd2c-126">Optional status notification callback.</span></span>

## <a name="see-also"></a><span data-ttu-id="6dd2c-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="6dd2c-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6dd2c-128">Referencia</span><span class="sxs-lookup"><span data-stu-id="6dd2c-128">Reference</span></span>

[<span data-ttu-id="6dd2c-129">Clase de API</span><span class="sxs-lookup"><span data-stu-id="6dd2c-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6dd2c-130">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="6dd2c-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6dd2c-131">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6dd2c-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
