---
description: 'Más información sobre: API. JetGetAttachInfoInstance (método)'
title: Método API. JetGetAttachInfoInstance
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94865042edf8b049b7140673a8aee1b4e2d91573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720345"
---
# <a name="apijetgetattachinfoinstance-method"></a><span data-ttu-id="430ac-103">Método API. JetGetAttachInfoInstance</span><span class="sxs-lookup"><span data-stu-id="430ac-103">Api.JetGetAttachInfoInstance method</span></span>

<span data-ttu-id="430ac-104">Se usa durante una copia de seguridad iniciada por [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar a una instancia los nombres de los archivos de base de datos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="430ac-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database files that should become part of the backup file set.</span></span> <span data-ttu-id="430ac-105">Solo se tendrán en cuenta las bases de datos que están asociadas actualmente a la instancia mediante [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) .</span><span class="sxs-lookup"><span data-stu-id="430ac-105">Only databases that are currently attached to the instance using [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) will be considered.</span></span> <span data-ttu-id="430ac-106">Estos archivos se pueden abrir posteriormente con [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) y leer mediante [JetReadFileInstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="430ac-106">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="430ac-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="430ac-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="430ac-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="430ac-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="430ac-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="430ac-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="430ac-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="430ac-110">Parameters</span></span>

  - <span data-ttu-id="430ac-111">instance</span><span class="sxs-lookup"><span data-stu-id="430ac-111">instance</span></span>  
    <span data-ttu-id="430ac-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="430ac-112">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="430ac-113">Instancia para la que se va a obtener información.</span><span class="sxs-lookup"><span data-stu-id="430ac-113">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="430ac-114">files</span><span class="sxs-lookup"><span data-stu-id="430ac-114">files</span></span>  
    <span data-ttu-id="430ac-115">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="430ac-115">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="430ac-116">Devuelve una lista de cadenas terminadas en null que describen el conjunto de archivos de base de datos que debe formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="430ac-116">Returns a list of null terminated strings describing the set of database files that should be a part of the backup file set.</span></span> <span data-ttu-id="430ac-117">La lista de cadenas devueltas en este búfer está en el mismo formato que una cadena múltiple utilizada por el registro.</span><span class="sxs-lookup"><span data-stu-id="430ac-117">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="430ac-118">Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="430ac-118">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="430ac-119">maxChars</span><span class="sxs-lookup"><span data-stu-id="430ac-119">maxChars</span></span>  
    <span data-ttu-id="430ac-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="430ac-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="430ac-121">Número máximo de caracteres que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="430ac-121">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="430ac-122">actualChars</span><span class="sxs-lookup"><span data-stu-id="430ac-122">actualChars</span></span>  
    <span data-ttu-id="430ac-123">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="430ac-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="430ac-124">Tamaño real de la lista de archivos.</span><span class="sxs-lookup"><span data-stu-id="430ac-124">Actual size of the file list.</span></span> <span data-ttu-id="430ac-125">Si es mayor que maxChars, la lista se ha truncado.</span><span class="sxs-lookup"><span data-stu-id="430ac-125">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="430ac-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="430ac-126">Remarks</span></span>

<span data-ttu-id="430ac-127">Es importante tener en cuenta que esta API no devuelve un error o ADVERTENCIA Si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="430ac-127">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="430ac-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="430ac-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="430ac-129">Referencia</span><span class="sxs-lookup"><span data-stu-id="430ac-129">Reference</span></span>

[<span data-ttu-id="430ac-130">Clase de API</span><span class="sxs-lookup"><span data-stu-id="430ac-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="430ac-131">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="430ac-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="430ac-132">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="430ac-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
