---
description: 'Más información sobre: API. JetReadFileInstance (método)'
title: Método API. JetReadFileInstance
TOCTitle: 'JetReadFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetreadfileinstance(v=EXCHG.10)
ms:contentKeyID: 55100781
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetReadFileInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 80eaf61fd9cd07fce80d32fddf7056f6bff683c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707253"
---
# <a name="apijetreadfileinstance-method"></a><span data-ttu-id="d3547-103">Método API. JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="d3547-103">Api.JetReadFileInstance method</span></span>

<span data-ttu-id="d3547-104">Recupera el contenido de un archivo abierto con [JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="d3547-104">Retrieves the contents of a file opened with [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md).</span></span>

<span data-ttu-id="d3547-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d3547-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d3547-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d3547-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d3547-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3547-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetReadFileInstance ( _
    instance As JET_INSTANCE, _
    file As JET_HANDLE, _
    buffer As Byte(), _
    bufferSize As Integer, _
    <OutAttribute> ByRef bytesRead As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim file As JET_HANDLE
Dim buffer As Byte()
Dim bufferSize As Integer
Dim bytesRead As IntegerApi.JetReadFileInstance(instance, _
    file, buffer, bufferSize, bytesRead)
```

``` csharp
public static void JetReadFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE file,
    byte[] buffer,
    int bufferSize,
    out int bytesRead
)
```

#### <a name="parameters"></a><span data-ttu-id="d3547-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3547-108">Parameters</span></span>

  - <span data-ttu-id="d3547-109">instance</span><span class="sxs-lookup"><span data-stu-id="d3547-109">instance</span></span>  
    <span data-ttu-id="d3547-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3547-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="d3547-111">La instancia de que se utilizará.</span><span class="sxs-lookup"><span data-stu-id="d3547-111">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3547-112">archivo</span><span class="sxs-lookup"><span data-stu-id="d3547-112">file</span></span>  
    <span data-ttu-id="d3547-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d3547-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="d3547-114">Archivo desde el que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="d3547-114">The file to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3547-115">buffer</span><span class="sxs-lookup"><span data-stu-id="d3547-115">buffer</span></span>  
    <span data-ttu-id="d3547-116">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="d3547-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="d3547-117">Búfer en el que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="d3547-117">The buffer to read into.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3547-118">bufferSize</span><span class="sxs-lookup"><span data-stu-id="d3547-118">bufferSize</span></span>  
    <span data-ttu-id="d3547-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d3547-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d3547-120">Tamaño del búfer.</span><span class="sxs-lookup"><span data-stu-id="d3547-120">The size of the buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="d3547-121">bytesRead</span><span class="sxs-lookup"><span data-stu-id="d3547-121">bytesRead</span></span>  
    <span data-ttu-id="d3547-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="d3547-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="d3547-123">Devuelve la cantidad de datos leídos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="d3547-123">Returns the amount of data read into the buffer.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3547-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3547-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d3547-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="d3547-125">Reference</span></span>

[<span data-ttu-id="d3547-126">Clase de API</span><span class="sxs-lookup"><span data-stu-id="d3547-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d3547-127">Miembros de API</span><span class="sxs-lookup"><span data-stu-id="d3547-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d3547-128">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d3547-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
