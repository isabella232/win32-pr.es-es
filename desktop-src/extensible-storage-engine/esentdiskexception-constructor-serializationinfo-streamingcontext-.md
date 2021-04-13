---
description: 'Más información acerca de: constructor EsentDiskException (SerializationInfo, StreamingContext)'
title: Constructor EsentDiskException (SerializationInfo, StreamingContext)
TOCTitle: EsentDiskException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDiskException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101228
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4abe19b16d9e6eb6d94d5b4fe1dd067b68c2c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361506"
---
# <a name="esentdiskexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="cd61f-103">Constructor EsentDiskException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="cd61f-103">EsentDiskException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="cd61f-104">Inicializa una nueva instancia de la clase EsentDiskException.</span><span class="sxs-lookup"><span data-stu-id="cd61f-104">Initializes a new instance of the EsentDiskException class.</span></span> <span data-ttu-id="cd61f-105">Este constructor se utiliza para deserializar una excepción serializada.</span><span class="sxs-lookup"><span data-stu-id="cd61f-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="cd61f-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cd61f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cd61f-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cd61f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cd61f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd61f-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentDiskException(info, context)
```

``` csharp
protected EsentDiskException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="cd61f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd61f-109">Parameters</span></span>

  - <span data-ttu-id="cd61f-110">info</span><span class="sxs-lookup"><span data-stu-id="cd61f-110">info</span></span>  
    <span data-ttu-id="cd61f-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="cd61f-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="cd61f-112">Los datos necesarios para deserializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="cd61f-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="cd61f-113">context</span><span class="sxs-lookup"><span data-stu-id="cd61f-113">context</span></span>  
    <span data-ttu-id="cd61f-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="cd61f-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="cd61f-115">Contexto de la deserialización.</span><span class="sxs-lookup"><span data-stu-id="cd61f-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd61f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd61f-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cd61f-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="cd61f-117">Reference</span></span>

[<span data-ttu-id="cd61f-118">Clase EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="cd61f-118">EsentDiskException class</span></span>](./esentdiskexception-class.md)

[<span data-ttu-id="cd61f-119">Miembros de EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="cd61f-119">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="cd61f-120">Sobrecarga EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="cd61f-120">EsentDiskException overload</span></span>](./esentdiskexception-constructor.md)

[<span data-ttu-id="cd61f-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cd61f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
