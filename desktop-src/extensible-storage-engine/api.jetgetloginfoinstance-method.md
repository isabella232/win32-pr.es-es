---
description: 'Más información sobre: API. JetGetLogInfoInstance (método)'
title: Método API. JetGetLogInfoInstance
TOCTitle: 'JetGetLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100726
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 85e252b74c47d3274fc83af59e3fb571906219fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652389"
---
# <a name="apijetgetloginfoinstance-method"></a><span data-ttu-id="33a90-103">Método API. JetGetLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="33a90-103">Api.JetGetLogInfoInstance method</span></span>

<span data-ttu-id="33a90-104">Se usa durante una copia de seguridad iniciada por [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar a una instancia los nombres de los archivos de revisión de la base de datos y los archivos de registro que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="33a90-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of database patch files and logfiles that should become part of the backup file set.</span></span> <span data-ttu-id="33a90-105">Estos archivos se pueden abrir posteriormente con [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) y leer mediante [JetReadFileInstance (JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32)](./api.jetreadfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="33a90-105">These files may subsequently be opened using [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) and read using [JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[\], Int32, Int32)](./api.jetreadfileinstance-method.md).</span></span>

<span data-ttu-id="33a90-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="33a90-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="33a90-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="33a90-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="33a90-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33a90-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="33a90-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33a90-109">Parameters</span></span>

  - <span data-ttu-id="33a90-110">instance</span><span class="sxs-lookup"><span data-stu-id="33a90-110">instance</span></span>  
    <span data-ttu-id="33a90-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="33a90-111">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="33a90-112">Instancia para la que se va a obtener información.</span><span class="sxs-lookup"><span data-stu-id="33a90-112">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="33a90-113">files</span><span class="sxs-lookup"><span data-stu-id="33a90-113">files</span></span>  
    <span data-ttu-id="33a90-114">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="33a90-114">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="33a90-115">Devuelve una lista de cadenas terminadas en null que describen el conjunto de archivos de revisión de la base de datos y los archivos de registro que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="33a90-115">Returns a list of null terminated strings describing the set of database patch files and log files that should be a part of the backup file set.</span></span> <span data-ttu-id="33a90-116">La lista de cadenas devueltas en este búfer está en el mismo formato que una cadena múltiple utilizada por el registro.</span><span class="sxs-lookup"><span data-stu-id="33a90-116">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="33a90-117">Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="33a90-117">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="33a90-118">maxChars</span><span class="sxs-lookup"><span data-stu-id="33a90-118">maxChars</span></span>  
    <span data-ttu-id="33a90-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="33a90-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="33a90-120">Número máximo de caracteres que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="33a90-120">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="33a90-121">actualChars</span><span class="sxs-lookup"><span data-stu-id="33a90-121">actualChars</span></span>  
    <span data-ttu-id="33a90-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="33a90-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="33a90-123">Tamaño real de la lista de archivos.</span><span class="sxs-lookup"><span data-stu-id="33a90-123">Actual size of the file list.</span></span> <span data-ttu-id="33a90-124">Si es mayor que maxChars, la lista se ha truncado.</span><span class="sxs-lookup"><span data-stu-id="33a90-124">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="33a90-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33a90-125">Remarks</span></span>

<span data-ttu-id="33a90-126">Es importante tener en cuenta que esta API no devuelve un error o ADVERTENCIA Si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="33a90-126">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="33a90-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="33a90-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="33a90-128">Referencia</span><span class="sxs-lookup"><span data-stu-id="33a90-128">Reference</span></span>

[<span data-ttu-id="33a90-129">Clase de API</span><span class="sxs-lookup"><span data-stu-id="33a90-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="33a90-130">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="33a90-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="33a90-131">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="33a90-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
