---
description: 'Más información sobre: clase EsentMissingPatchPageException'
title: Clase EsentMissingPatchPageException
TOCTitle: EsentMissingPatchPageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingPatchPageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingpatchpageexception(v=EXCHG.10)
ms:contentKeyID: 55102239
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingPatchPageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingPatchPageException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 59ebed57297a294c4e1e181594d0576b5714df9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666979"
---
# <a name="esentmissingpatchpageexception-class"></a><span data-ttu-id="71418-103">Clase EsentMissingPatchPageException</span><span class="sxs-lookup"><span data-stu-id="71418-103">EsentMissingPatchPageException class</span></span>

<span data-ttu-id="71418-104">Clase base para JET_err. Excepciones MissingPatchPage.</span><span class="sxs-lookup"><span data-stu-id="71418-104">Base class for JET_err.MissingPatchPage exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="71418-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="71418-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="71418-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="71418-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="71418-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="71418-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="71418-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="71418-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="71418-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="71418-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="71418-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="71418-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="71418-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="71418-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="71418-112">Microsoft. ISAM. esent. Interop. EsentMissingPatchPageException</span><span class="sxs-lookup"><span data-stu-id="71418-112">Microsoft.Isam.Esent.Interop.EsentMissingPatchPageException</span></span>  

<span data-ttu-id="71418-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="71418-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="71418-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="71418-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="71418-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71418-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingPatchPageException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentMissingPatchPageException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingPatchPageException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="71418-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="71418-116">Thread safety</span></span>

<span data-ttu-id="71418-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="71418-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="71418-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="71418-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="71418-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="71418-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71418-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="71418-120">Reference</span></span>

[<span data-ttu-id="71418-121">Miembros de EsentMissingPatchPageException</span><span class="sxs-lookup"><span data-stu-id="71418-121">EsentMissingPatchPageException members</span></span>](./esentmissingpatchpageexception-members.md)

[<span data-ttu-id="71418-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="71418-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
