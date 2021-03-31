---
description: 'Más información sobre: constructor EsentApiException (String, JET_err)'
title: Constructor EsentApiException (String, JET_err)
TOCTitle: EsentApiException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101058
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 568cf61a1c5852b70d0e08647a39ab70140d2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808228"
---
# <a name="esentapiexception-constructor-string-jet_err"></a><span data-ttu-id="e90dd-103">Constructor EsentApiException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="e90dd-103">EsentApiException constructor (String, JET_err)</span></span>

<span data-ttu-id="e90dd-104">Inicializa una nueva instancia de la clase EsentApiException.</span><span class="sxs-lookup"><span data-stu-id="e90dd-104">Initializes a new instance of the EsentApiException class.</span></span>

<span data-ttu-id="e90dd-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e90dd-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e90dd-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e90dd-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e90dd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e90dd-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentApiException(description, _
    err)
```

``` csharp
protected EsentApiException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="e90dd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e90dd-108">Parameters</span></span>

  - <span data-ttu-id="e90dd-109">description</span><span class="sxs-lookup"><span data-stu-id="e90dd-109">description</span></span>  
    <span data-ttu-id="e90dd-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e90dd-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e90dd-111">Descripción del error.</span><span class="sxs-lookup"><span data-stu-id="e90dd-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="e90dd-112">err</span><span class="sxs-lookup"><span data-stu-id="e90dd-112">err</span></span>  
    <span data-ttu-id="e90dd-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e90dd-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="e90dd-114">El código de error de la excepción.</span><span class="sxs-lookup"><span data-stu-id="e90dd-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="e90dd-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="e90dd-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e90dd-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="e90dd-116">Reference</span></span>

[<span data-ttu-id="e90dd-117">Clase EsentApiException</span><span class="sxs-lookup"><span data-stu-id="e90dd-117">EsentApiException class</span></span>](./esentapiexception-class.md)

[<span data-ttu-id="e90dd-118">Miembros de EsentApiException</span><span class="sxs-lookup"><span data-stu-id="e90dd-118">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="e90dd-119">Sobrecarga EsentApiException</span><span class="sxs-lookup"><span data-stu-id="e90dd-119">EsentApiException overload</span></span>](./esentapiexception-constructor.md)

[<span data-ttu-id="e90dd-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e90dd-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
