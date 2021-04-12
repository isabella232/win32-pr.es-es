---
description: 'Más información sobre: constructor EsentUsageException (String, JET_err)'
title: Constructor EsentUsageException (String, JET_err)
TOCTitle: EsentUsageException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentUsageException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentusageexception.esentusageexception(v=EXCHG.10)
ms:contentKeyID: 55103223
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentUsageException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4f9d38ebc5be25eb8f036583404d340a8882de6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361691"
---
# <a name="esentusageexception-constructor-string-jet_err"></a><span data-ttu-id="45f4d-103">Constructor EsentUsageException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="45f4d-103">EsentUsageException constructor (String, JET_err)</span></span>

<span data-ttu-id="45f4d-104">Inicializa una nueva instancia de la clase EsentUsageException.</span><span class="sxs-lookup"><span data-stu-id="45f4d-104">Initializes a new instance of the EsentUsageException class.</span></span>

<span data-ttu-id="45f4d-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="45f4d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="45f4d-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="45f4d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="45f4d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45f4d-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentUsageException(description, _
    err)
```

``` csharp
protected EsentUsageException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="45f4d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45f4d-108">Parameters</span></span>

  - <span data-ttu-id="45f4d-109">description</span><span class="sxs-lookup"><span data-stu-id="45f4d-109">description</span></span>  
    <span data-ttu-id="45f4d-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="45f4d-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="45f4d-111">Descripción del error.</span><span class="sxs-lookup"><span data-stu-id="45f4d-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="45f4d-112">err</span><span class="sxs-lookup"><span data-stu-id="45f4d-112">err</span></span>  
    <span data-ttu-id="45f4d-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="45f4d-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="45f4d-114">El código de error de la excepción.</span><span class="sxs-lookup"><span data-stu-id="45f4d-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="45f4d-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="45f4d-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="45f4d-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="45f4d-116">Reference</span></span>

[<span data-ttu-id="45f4d-117">Clase EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="45f4d-117">EsentUsageException class</span></span>](./esentusageexception-class.md)

[<span data-ttu-id="45f4d-118">Miembros de EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="45f4d-118">EsentUsageException members</span></span>](./esentusageexception-members.md)

[<span data-ttu-id="45f4d-119">Sobrecarga EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="45f4d-119">EsentUsageException overload</span></span>](./esentusageexception-constructor.md)

[<span data-ttu-id="45f4d-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="45f4d-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
