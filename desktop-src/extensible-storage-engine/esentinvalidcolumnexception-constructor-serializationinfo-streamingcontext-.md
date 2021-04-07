---
description: 'Más información acerca de: constructor EsentInvalidColumnException (SerializationInfo, StreamingContext)'
title: Constructor EsentInvalidColumnException (SerializationInfo, StreamingContext)
TOCTitle: EsentInvalidColumnException constructor (SerializationInfo, StreamingContext)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentInvalidColumnException.#ctor(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidcolumnexception.esentinvalidcolumnexception(v=EXCHG.10)
ms:contentKeyID: 55101741
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidColumnException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f439edeb0dad09f4c7f1bdd9521bb2410ca68be6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003199"
---
# <a name="esentinvalidcolumnexception-constructor-serializationinfo-streamingcontext"></a><span data-ttu-id="21a82-103">Constructor EsentInvalidColumnException (SerializationInfo, StreamingContext)</span><span class="sxs-lookup"><span data-stu-id="21a82-103">EsentInvalidColumnException constructor (SerializationInfo, StreamingContext)</span></span>

<span data-ttu-id="21a82-104">Inicializa una nueva instancia de la clase EsentInvalidColumnException.</span><span class="sxs-lookup"><span data-stu-id="21a82-104">Initializes a new instance of the EsentInvalidColumnException class.</span></span> <span data-ttu-id="21a82-105">Este constructor se utiliza para deserializar una excepción serializada.</span><span class="sxs-lookup"><span data-stu-id="21a82-105">This constructor is used to deserialize a serialized exception.</span></span>

<span data-ttu-id="21a82-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="21a82-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="21a82-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="21a82-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="21a82-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21a82-108">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim info As SerializationInfo
Dim context As StreamingContext

Dim instance As New EsentInvalidColumnException(info, context)
```

``` csharp
protected EsentInvalidColumnException(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="21a82-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21a82-109">Parameters</span></span>

  - <span data-ttu-id="21a82-110">info</span><span class="sxs-lookup"><span data-stu-id="21a82-110">info</span></span>  
    <span data-ttu-id="21a82-111">Tipo: [System. Runtime. Serialization. SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span><span class="sxs-lookup"><span data-stu-id="21a82-111">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="21a82-112">Los datos necesarios para deserializar el objeto.</span><span class="sxs-lookup"><span data-stu-id="21a82-112">The data needed to deserialize the object.</span></span>

<!-- end list -->

  - <span data-ttu-id="21a82-113">context</span><span class="sxs-lookup"><span data-stu-id="21a82-113">context</span></span>  
    <span data-ttu-id="21a82-114">Tipo: [System. Runtime. Serialization. StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span><span class="sxs-lookup"><span data-stu-id="21a82-114">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="21a82-115">Contexto de la deserialización.</span><span class="sxs-lookup"><span data-stu-id="21a82-115">The deserialization context.</span></span>

## <a name="see-also"></a><span data-ttu-id="21a82-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="21a82-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="21a82-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="21a82-117">Reference</span></span>

[<span data-ttu-id="21a82-118">Clase EsentInvalidColumnException</span><span class="sxs-lookup"><span data-stu-id="21a82-118">EsentInvalidColumnException class</span></span>](./esentinvalidcolumnexception-class.md)

[<span data-ttu-id="21a82-119">Miembros de EsentInvalidColumnException</span><span class="sxs-lookup"><span data-stu-id="21a82-119">EsentInvalidColumnException members</span></span>](./esentinvalidcolumnexception-members.md)

[<span data-ttu-id="21a82-120">Sobrecarga EsentInvalidColumnException</span><span class="sxs-lookup"><span data-stu-id="21a82-120">EsentInvalidColumnException overload</span></span>](./esentinvalidcolumnexception-constructor2.md)

[<span data-ttu-id="21a82-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="21a82-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
