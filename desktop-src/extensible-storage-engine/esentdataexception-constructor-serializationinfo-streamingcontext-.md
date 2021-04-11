---
description: 'Más información acerca de: constructor EsentDataException (SerializationInfo, StreamingContext)'
title: Constructor EsentDataException (SerializationInfo, StreamingContext)
TOCTitle: EsentDataException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDataException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101275
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43e7578adb10f607ff88062b48d3f2ebb73d34ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276088"
---
# <a name="esentdataexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="c1d7d-103">Constructor EsentDataException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="c1d7d-103">EsentDataException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="c1d7d-104">Inicializa una nueva instancia de la clase EsentDataException.</span><span class="sxs-lookup"><span data-stu-id="c1d7d-104">Initializes a new instance of the EsentDataException class.</span></span> <span data-ttu-id="c1d7d-105">Este constructor se utiliza para deserializar una excepción serializada.</span><span class="sxs-lookup"><span data-stu-id="c1d7d-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="c1d7d-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c1d7d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c1d7d-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c1d7d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d7d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1d7d-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentDataException(info, context)
```

``` csharp
protected EsentDataException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="c1d7d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c1d7d-109">Parameters</span></span>

  - <span data-ttu-id="c1d7d-110">info</span><span class="sxs-lookup"><span data-stu-id="c1d7d-110">info</span></span>  
    <span data-ttu-id="c1d7d-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="c1d7d-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="c1d7d-112">Los datos necesarios para deserializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="c1d7d-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1d7d-113">context</span><span class="sxs-lookup"><span data-stu-id="c1d7d-113">context</span></span>  
    <span data-ttu-id="c1d7d-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="c1d7d-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="c1d7d-115">Contexto de la deserialización.</span><span class="sxs-lookup"><span data-stu-id="c1d7d-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1d7d-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1d7d-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c1d7d-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="c1d7d-117">Reference</span></span>

[<span data-ttu-id="c1d7d-118">Clase EsentDataException</span><span class="sxs-lookup"><span data-stu-id="c1d7d-118">EsentDataException class</span></span>](./esentdataexception-class.md)

[<span data-ttu-id="c1d7d-119">Miembros de EsentDataException</span><span class="sxs-lookup"><span data-stu-id="c1d7d-119">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="c1d7d-120">Sobrecarga EsentDataException</span><span class="sxs-lookup"><span data-stu-id="c1d7d-120">EsentDataException overload</span></span>](./esentdataexception-constructor.md)

[<span data-ttu-id="c1d7d-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c1d7d-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
