---
description: 'Más información sobre: API. JetGetTruncateLogInfoInstance (método)'
title: Método API. JetGetTruncateLogInfoInstance
TOCTitle: 'JetGetTruncateLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettruncateloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100743
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc54d12796a724b382343c4a3514f03102df305f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279277"
---
# <a name="apijetgettruncateloginfoinstance-method"></a><span data-ttu-id="1cacf-103">Método API. JetGetTruncateLogInfoInstance</span><span class="sxs-lookup"><span data-stu-id="1cacf-103">Api.JetGetTruncateLogInfoInstance method</span></span>

<span data-ttu-id="1cacf-104">Se usa durante una copia de seguridad iniciada por [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) para consultar a una instancia los nombres de los archivos de registro de transacciones que se pueden eliminar de forma segura después de que la copia de seguridad se haya completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1cacf-104">Used during a backup initiated by [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) to query an instance for the names of the transaction log files that can be safely deleted after the backup has successfully completed.</span></span>

<span data-ttu-id="1cacf-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1cacf-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1cacf-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1cacf-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1cacf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cacf-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTruncateLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetTruncateLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetTruncateLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a><span data-ttu-id="1cacf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cacf-108">Parameters</span></span>

  - <span data-ttu-id="1cacf-109">instance</span><span class="sxs-lookup"><span data-stu-id="1cacf-109">instance</span></span>  
    <span data-ttu-id="1cacf-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1cacf-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="1cacf-111">Instancia para la que se va a obtener información.</span><span class="sxs-lookup"><span data-stu-id="1cacf-111">The instance to get the information for.</span></span>

<!-- end list -->

  - <span data-ttu-id="1cacf-112">files</span><span class="sxs-lookup"><span data-stu-id="1cacf-112">files</span></span>  
    <span data-ttu-id="1cacf-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="1cacf-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="1cacf-114">Devuelve una lista de cadenas terminadas en null que describen el conjunto de archivos de registro de base de datos que se pueden eliminar de forma segura una vez completada la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1cacf-114">Returns a list of null terminated strings describing the set of database log files that can be safely deleted after the backup completes.</span></span> <span data-ttu-id="1cacf-115">La lista de cadenas devueltas en este búfer está en el mismo formato que una cadena múltiple utilizada por el registro.</span><span class="sxs-lookup"><span data-stu-id="1cacf-115">The list of strings returned in this buffer is in the same format as a multi-string used by the registry.</span></span> <span data-ttu-id="1cacf-116">Cada cadena terminada en NULL se devuelve en secuencia seguida de un terminador nulo final.</span><span class="sxs-lookup"><span data-stu-id="1cacf-116">Each null-terminated string is returned in sequence followed by a final null terminator.</span></span>

<!-- end list -->

  - <span data-ttu-id="1cacf-117">maxChars</span><span class="sxs-lookup"><span data-stu-id="1cacf-117">maxChars</span></span>  
    <span data-ttu-id="1cacf-118">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1cacf-118">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1cacf-119">Número máximo de caracteres que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="1cacf-119">Maximum number of characters to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="1cacf-120">actualChars</span><span class="sxs-lookup"><span data-stu-id="1cacf-120">actualChars</span></span>  
    <span data-ttu-id="1cacf-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1cacf-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1cacf-122">Tamaño real de la lista de archivos.</span><span class="sxs-lookup"><span data-stu-id="1cacf-122">Actual size of the file list.</span></span> <span data-ttu-id="1cacf-123">Si es mayor que maxChars, la lista se ha truncado.</span><span class="sxs-lookup"><span data-stu-id="1cacf-123">If this is greater than maxChars then the list has been truncated.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cacf-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cacf-124">Remarks</span></span>

<span data-ttu-id="1cacf-125">Es importante tener en cuenta que esta API no devuelve un error o ADVERTENCIA Si el búfer de salida es demasiado pequeño para aceptar la lista completa de archivos que deben formar parte del conjunto de archivos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1cacf-125">It is important to note that this API does not return an error or warning if the output buffer is too small to accept the full list of files that should be part of the backup file set.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cacf-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cacf-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1cacf-127">Referencia</span><span class="sxs-lookup"><span data-stu-id="1cacf-127">Reference</span></span>

[<span data-ttu-id="1cacf-128">Clase de API</span><span class="sxs-lookup"><span data-stu-id="1cacf-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1cacf-129">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="1cacf-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1cacf-130">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1cacf-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
