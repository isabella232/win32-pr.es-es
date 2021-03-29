---
description: 'Más información sobre: constructor EsentCorruptionException (String, JET_err)'
title: Constructor EsentCorruptionException (String, JET_err)
TOCTitle: EsentCorruptionException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentCorruptionException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcorruptionexception.esentcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101380
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentCorruptionException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30ed98ea56fe791ed949edc82b548990371c9671
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540115"
---
# <a name="esentcorruptionexception-constructor-string-jet_err"></a><span data-ttu-id="eb608-103">Constructor EsentCorruptionException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="eb608-103">EsentCorruptionException constructor (String, JET_err)</span></span>

<span data-ttu-id="eb608-104">Inicializa una nueva instancia de la clase EsentCorruptionException.</span><span class="sxs-lookup"><span data-stu-id="eb608-104">Initializes a new instance of the EsentCorruptionException class.</span></span>

<span data-ttu-id="eb608-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="eb608-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="eb608-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="eb608-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="eb608-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb608-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentCorruptionException(description, _
    err)
```

``` csharp
protected EsentCorruptionException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="eb608-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb608-108">Parameters</span></span>

  - <span data-ttu-id="eb608-109">description</span><span class="sxs-lookup"><span data-stu-id="eb608-109">description</span></span>  
    <span data-ttu-id="eb608-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="eb608-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="eb608-111">Descripción del error.</span><span class="sxs-lookup"><span data-stu-id="eb608-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="eb608-112">err</span><span class="sxs-lookup"><span data-stu-id="eb608-112">err</span></span>  
    <span data-ttu-id="eb608-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="eb608-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="eb608-114">El código de error de la excepción.</span><span class="sxs-lookup"><span data-stu-id="eb608-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb608-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb608-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="eb608-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="eb608-116">Reference</span></span>

[<span data-ttu-id="eb608-117">Clase EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="eb608-117">EsentCorruptionException class</span></span>](./esentcorruptionexception-class.md)

[<span data-ttu-id="eb608-118">Miembros de EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="eb608-118">EsentCorruptionException members</span></span>](./esentcorruptionexception-members.md)

[<span data-ttu-id="eb608-119">Sobrecarga EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="eb608-119">EsentCorruptionException overload</span></span>](./esentcorruptionexception-constructor.md)

[<span data-ttu-id="eb608-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="eb608-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
