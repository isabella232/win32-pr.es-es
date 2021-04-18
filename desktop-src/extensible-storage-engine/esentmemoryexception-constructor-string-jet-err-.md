---
description: 'Más información sobre: constructor EsentMemoryException (String, JET_err)'
title: Constructor EsentMemoryException (String, JET_err)
TOCTitle: EsentMemoryException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102199
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60cdb6fda03695a4afb41d82e83aaeeb9415f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697036"
---
# <a name="esentmemoryexception-constructor-string-jet_err"></a><span data-ttu-id="d6938-103">Constructor EsentMemoryException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="d6938-103">EsentMemoryException constructor (String, JET_err)</span></span>

<span data-ttu-id="d6938-104">Inicializa una nueva instancia de la clase EsentMemoryException.</span><span class="sxs-lookup"><span data-stu-id="d6938-104">Initializes a new instance of the EsentMemoryException class.</span></span>

<span data-ttu-id="d6938-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6938-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d6938-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d6938-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6938-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6938-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentMemoryException(description, _
    err)
```

``` csharp
protected EsentMemoryException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="d6938-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6938-108">Parameters</span></span>

  - <span data-ttu-id="d6938-109">description</span><span class="sxs-lookup"><span data-stu-id="d6938-109">description</span></span>  
    <span data-ttu-id="d6938-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d6938-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d6938-111">Descripción del error.</span><span class="sxs-lookup"><span data-stu-id="d6938-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6938-112">err</span><span class="sxs-lookup"><span data-stu-id="d6938-112">err</span></span>  
    <span data-ttu-id="d6938-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d6938-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="d6938-114">El código de error de la excepción.</span><span class="sxs-lookup"><span data-stu-id="d6938-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6938-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6938-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6938-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="d6938-116">Reference</span></span>

[<span data-ttu-id="d6938-117">Clase EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="d6938-117">EsentMemoryException class</span></span>](./esentmemoryexception-class.md)

[<span data-ttu-id="d6938-118">Miembros de EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="d6938-118">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="d6938-119">Sobrecarga EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="d6938-119">EsentMemoryException overload</span></span>](./esentmemoryexception-constructor.md)

[<span data-ttu-id="d6938-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d6938-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
