---
description: 'Más información sobre: API. JetOpenFileInstance (método)'
title: Método API. JetOpenFileInstance
TOCTitle: 'JetOpenFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,Microsoft.Isam.Esent.Interop.JET_HANDLE@,System.Int64@,System.Int64@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopenfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100767
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b58b3a426fd2eb7e33cce1f5f539418bcc993ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717019"
---
# <a name="apijetopenfileinstance-method"></a><span data-ttu-id="4c191-103">Método API. JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="4c191-103">Api.JetOpenFileInstance method</span></span>

<span data-ttu-id="4c191-104">Abre una base de datos adjunta, un archivo de revisión de base de datos o un archivo de registro de transacciones de una instancia activa con el fin de realizar una copia de seguridad aproximada de streaming.</span><span class="sxs-lookup"><span data-stu-id="4c191-104">Opens an attached database, database patch file, or transaction log file of an active instance for the purpose of performing a streaming fuzzy backup.</span></span> <span data-ttu-id="4c191-105">Posteriormente, los datos de estos archivos se pueden leer a través del controlador devuelto mediante JetReadFileInstance.</span><span class="sxs-lookup"><span data-stu-id="4c191-105">The data from these files can subsequently be read through the returned handle using JetReadFileInstance.</span></span> <span data-ttu-id="4c191-106">El identificador devuelto debe cerrarse mediante JetCloseFileInstance.</span><span class="sxs-lookup"><span data-stu-id="4c191-106">The returned handle must be closed using JetCloseFileInstance.</span></span> <span data-ttu-id="4c191-107">Se debe haber iniciado previamente una copia de seguridad externa de la instancia mediante JetBeginExternalBackupInstance.</span><span class="sxs-lookup"><span data-stu-id="4c191-107">An external backup of the instance must have been previously initiated using JetBeginExternalBackupInstance.</span></span>

<span data-ttu-id="4c191-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4c191-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4c191-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4c191-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4c191-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c191-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenFileInstance ( _
    instance As JET_INSTANCE, _
    file As String, _
    <OutAttribute> ByRef handle As JET_HANDLE, _
    <OutAttribute> ByRef fileSizeLow As Long, _
    <OutAttribute> ByRef fileSizeHigh As Long _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As String
Dim handle As JET_HANDLE
Dim fileSizeLow As Long
Dim fileSizeHigh As LongApi.JetOpenFileInstance(instance, _
    file, handle, fileSizeLow, fileSizeHigh)
```

``` csharp
public static void JetOpenFileInstance(
    JET_INSTANCE instance,
    string file,
    out JET_HANDLE handle,
    out long fileSizeLow,
    out long fileSizeHigh
)
```

#### <a name="parameters"></a><span data-ttu-id="4c191-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c191-111">Parameters</span></span>

  - <span data-ttu-id="4c191-112">instance</span><span class="sxs-lookup"><span data-stu-id="4c191-112">instance</span></span>  
    <span data-ttu-id="4c191-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4c191-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="4c191-114">La instancia de que se utilizará.</span><span class="sxs-lookup"><span data-stu-id="4c191-114">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4c191-115">archivo</span><span class="sxs-lookup"><span data-stu-id="4c191-115">file</span></span>  
    <span data-ttu-id="4c191-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4c191-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4c191-117">Archivo que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="4c191-117">The file to open.</span></span>

<!-- end list -->

  - <span data-ttu-id="4c191-118">handle</span><span class="sxs-lookup"><span data-stu-id="4c191-118">handle</span></span>  
    <span data-ttu-id="4c191-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4c191-119">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="4c191-120">Devuelve un identificador para el archivo.</span><span class="sxs-lookup"><span data-stu-id="4c191-120">Returns a handle to the file.</span></span>

<!-- end list -->

  - <span data-ttu-id="4c191-121">fileSizeLow</span><span class="sxs-lookup"><span data-stu-id="4c191-121">fileSizeLow</span></span>  
    <span data-ttu-id="4c191-122">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="4c191-122">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="4c191-123">Devuelve los 32 bits menos significativos del tamaño de archivo.</span><span class="sxs-lookup"><span data-stu-id="4c191-123">Returns the least significant 32 bits of the file size.</span></span>

<!-- end list -->

  - <span data-ttu-id="4c191-124">fileSizeHigh</span><span class="sxs-lookup"><span data-stu-id="4c191-124">fileSizeHigh</span></span>  
    <span data-ttu-id="4c191-125">Tipo: [System. Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="4c191-125">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="4c191-126">Devuelve los bits 32 más significativos del tamaño de archivo.</span><span class="sxs-lookup"><span data-stu-id="4c191-126">Returns the most significant 32 bits of the file size.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c191-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c191-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4c191-128">Referencia</span><span class="sxs-lookup"><span data-stu-id="4c191-128">Reference</span></span>

[<span data-ttu-id="4c191-129">Clase de API</span><span class="sxs-lookup"><span data-stu-id="4c191-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4c191-130">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="4c191-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4c191-131">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4c191-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
