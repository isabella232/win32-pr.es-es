---
description: 'Más información sobre: constructor EsentDiskException (String, JET_err)'
title: Constructor EsentDiskException (String, JET_err)
TOCTitle: EsentDiskException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDiskException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101616
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d518fcb263481c2563b92d0b579a686db13c0175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688608"
---
# <a name="esentdiskexception-constructor-string-jet_err"></a><span data-ttu-id="df16e-103">Constructor EsentDiskException (String, JET_err)</span><span class="sxs-lookup"><span data-stu-id="df16e-103">EsentDiskException constructor (String, JET_err)</span></span>

<span data-ttu-id="df16e-104">Inicializa una nueva instancia de la clase EsentDiskException.</span><span class="sxs-lookup"><span data-stu-id="df16e-104">Initializes a new instance of the EsentDiskException class.</span></span>

<span data-ttu-id="df16e-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="df16e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="df16e-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="df16e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="df16e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df16e-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentDiskException(description, _
    err)
```

``` csharp
protected EsentDiskException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="df16e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df16e-108">Parameters</span></span>

  - <span data-ttu-id="df16e-109">description</span><span class="sxs-lookup"><span data-stu-id="df16e-109">description</span></span>  
    <span data-ttu-id="df16e-110">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="df16e-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="df16e-111">Descripción del error.</span><span class="sxs-lookup"><span data-stu-id="df16e-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="df16e-112">err</span><span class="sxs-lookup"><span data-stu-id="df16e-112">err</span></span>  
    <span data-ttu-id="df16e-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="df16e-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="df16e-114">El código de error de la excepción.</span><span class="sxs-lookup"><span data-stu-id="df16e-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="df16e-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="df16e-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="df16e-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="df16e-116">Reference</span></span>

[<span data-ttu-id="df16e-117">Clase EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="df16e-117">EsentDiskException class</span></span>](./esentdiskexception-class.md)

[<span data-ttu-id="df16e-118">Miembros de EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="df16e-118">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="df16e-119">Sobrecarga EsentDiskException</span><span class="sxs-lookup"><span data-stu-id="df16e-119">EsentDiskException overload</span></span>](./esentdiskexception-constructor.md)

[<span data-ttu-id="df16e-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="df16e-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
