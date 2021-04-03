---
description: 'Más información sobre: constructor EsentInconsistentException (String, JET_err)'
title: Constructor EsentInconsistentException (String, JET_err)
TOCTitle: EsentInconsistentException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentInconsistentException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinconsistentexception.esentinconsistentexception(v=EXCHG.10)
ms:contentKeyID: 55101740
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentInconsistentException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 96d8b7a055d07ae120a23665004712772f67f215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810633"
---
# <a name="esentinconsistentexception-constructor-string-jet_err"></a><span data-ttu-id="35d97-103">Constructor EsentInconsistentException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="35d97-103">EsentInconsistentException constructor (String, JET_err)</span></span>

<span data-ttu-id="35d97-104">Inicializa una nueva instancia de la clase EsentInconsistentException.</span><span class="sxs-lookup"><span data-stu-id="35d97-104">Initializes a new instance of the EsentInconsistentException class.</span></span>

<span data-ttu-id="35d97-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="35d97-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="35d97-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="35d97-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="35d97-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35d97-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentInconsistentException(description, _
    err)
```

``` csharp
protected EsentInconsistentException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="35d97-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35d97-108">Parameters</span></span>

  - <span data-ttu-id="35d97-109">description</span><span class="sxs-lookup"><span data-stu-id="35d97-109">description</span></span>  
    <span data-ttu-id="35d97-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="35d97-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="35d97-111">Descripción del error.</span><span class="sxs-lookup"><span data-stu-id="35d97-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="35d97-112">err</span><span class="sxs-lookup"><span data-stu-id="35d97-112">err</span></span>  
    <span data-ttu-id="35d97-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="35d97-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="35d97-114">El código de error de la excepción.</span><span class="sxs-lookup"><span data-stu-id="35d97-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="35d97-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="35d97-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="35d97-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="35d97-116">Reference</span></span>

[<span data-ttu-id="35d97-117">Clase EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="35d97-117">EsentInconsistentException class</span></span>](./esentinconsistentexception-class.md)

[<span data-ttu-id="35d97-118">Miembros de EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="35d97-118">EsentInconsistentException members</span></span>](./esentinconsistentexception-members.md)

[<span data-ttu-id="35d97-119">Sobrecarga EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="35d97-119">EsentInconsistentException overload</span></span>](./esentinconsistentexception-constructor.md)

[<span data-ttu-id="35d97-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="35d97-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
