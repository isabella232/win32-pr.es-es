---
description: 'Más información sobre: clase EsentFileInvalidTypeException'
title: Clase EsentFileInvalidTypeException
TOCTitle: EsentFileInvalidTypeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileinvalidtypeexception(v=EXCHG.10)
ms:contentKeyID: 55107272
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c2bf5cf30cb45734613fcabc446834085d5bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361431"
---
# <a name="esentfileinvalidtypeexception-class"></a><span data-ttu-id="3ebb5-103">Clase EsentFileInvalidTypeException</span><span class="sxs-lookup"><span data-stu-id="3ebb5-103">EsentFileInvalidTypeException class</span></span>

<span data-ttu-id="3ebb5-104">Clase base para JET_err. Excepciones FileInvalidType.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-104">Base class for JET_err.FileInvalidType exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3ebb5-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="3ebb5-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3ebb5-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3ebb5-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3ebb5-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="3ebb5-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3ebb5-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="3ebb5-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3ebb5-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="3ebb5-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3ebb5-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="3ebb5-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="3ebb5-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="3ebb5-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="3ebb5-112">Microsoft. ISAM. esent. Interop. EsentFileInvalidTypeException</span><span class="sxs-lookup"><span data-stu-id="3ebb5-112">Microsoft.Isam.Esent.Interop.EsentFileInvalidTypeException</span></span>  

<span data-ttu-id="3ebb5-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3ebb5-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3ebb5-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3ebb5-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3ebb5-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ebb5-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileInvalidTypeException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentFileInvalidTypeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileInvalidTypeException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="3ebb5-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="3ebb5-116">Thread safety</span></span>

<span data-ttu-id="3ebb5-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3ebb5-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="3ebb5-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ebb5-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ebb5-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3ebb5-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="3ebb5-120">Reference</span></span>

[<span data-ttu-id="3ebb5-121">Miembros de EsentFileInvalidTypeException</span><span class="sxs-lookup"><span data-stu-id="3ebb5-121">EsentFileInvalidTypeException members</span></span>](./esentfileinvalidtypeexception-members.md)

[<span data-ttu-id="3ebb5-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3ebb5-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
