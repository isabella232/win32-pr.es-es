---
description: 'Más información sobre: clase EsentInvalidFilenameException'
title: Clase EsentInvalidFilenameException
TOCTitle: EsentInvalidFilenameException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidfilenameexception(v=EXCHG.10)
ms:contentKeyID: 55101955
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 209347096064d61f9f31fac8ae0552f36fbc9109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717277"
---
# <a name="esentinvalidfilenameexception-class"></a><span data-ttu-id="d2e1e-103">Clase EsentInvalidFilenameException</span><span class="sxs-lookup"><span data-stu-id="d2e1e-103">EsentInvalidFilenameException class</span></span>

<span data-ttu-id="d2e1e-104">Clase base para JET_err. Excepciones InvalidFilename.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-104">Base class for JET_err.InvalidFilename exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d2e1e-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="d2e1e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d2e1e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d2e1e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d2e1e-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d2e1e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d2e1e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d2e1e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d2e1e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d2e1e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d2e1e-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="d2e1e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="d2e1e-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="d2e1e-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="d2e1e-112">Microsoft. ISAM. esent. Interop. EsentInvalidFilenameException</span><span class="sxs-lookup"><span data-stu-id="d2e1e-112">Microsoft.Isam.Esent.Interop.EsentInvalidFilenameException</span></span>  

<span data-ttu-id="d2e1e-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d2e1e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d2e1e-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d2e1e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d2e1e-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2e1e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidFilenameException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidFilenameException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidFilenameException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="d2e1e-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="d2e1e-116">Thread safety</span></span>

<span data-ttu-id="d2e1e-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d2e1e-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2e1e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2e1e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d2e1e-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="d2e1e-120">Reference</span></span>

[<span data-ttu-id="d2e1e-121">Miembros de EsentInvalidFilenameException</span><span class="sxs-lookup"><span data-stu-id="d2e1e-121">EsentInvalidFilenameException members</span></span>](./esentinvalidfilenameexception-members.md)

[<span data-ttu-id="d2e1e-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d2e1e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
