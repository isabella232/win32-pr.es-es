---
description: 'Más información sobre: clase EsentDatabaseAlreadyUpgradedException'
title: Clase EsentDatabaseAlreadyUpgradedException
TOCTitle: EsentDatabaseAlreadyUpgradedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasealreadyupgradedexception(v=EXCHG.10)
ms:contentKeyID: 55101322
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27ad5a37676ef0b8e4a450619c19a45f3bdee1b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547174"
---
# <a name="esentdatabasealreadyupgradedexception-class"></a><span data-ttu-id="f956d-103">Clase EsentDatabaseAlreadyUpgradedException</span><span class="sxs-lookup"><span data-stu-id="f956d-103">EsentDatabaseAlreadyUpgradedException class</span></span>

<span data-ttu-id="f956d-104">Clase base para JET_err. Excepciones DatabaseAlreadyUpgraded.</span><span class="sxs-lookup"><span data-stu-id="f956d-104">Base class for JET_err.DatabaseAlreadyUpgraded exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f956d-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="f956d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f956d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f956d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f956d-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="f956d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f956d-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f956d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f956d-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f956d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f956d-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="f956d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f956d-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="f956d-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="f956d-112">Microsoft. ISAM. esent. Interop. EsentDatabaseAlreadyUpgradedException</span><span class="sxs-lookup"><span data-stu-id="f956d-112">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyUpgradedException</span></span>  

<span data-ttu-id="f956d-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f956d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f956d-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f956d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f956d-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f956d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseAlreadyUpgradedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseAlreadyUpgradedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseAlreadyUpgradedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="f956d-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="f956d-116">Thread safety</span></span>

<span data-ttu-id="f956d-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f956d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f956d-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f956d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f956d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="f956d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f956d-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="f956d-120">Reference</span></span>

[<span data-ttu-id="f956d-121">Miembros de EsentDatabaseAlreadyUpgradedException</span><span class="sxs-lookup"><span data-stu-id="f956d-121">EsentDatabaseAlreadyUpgradedException members</span></span>](./esentdatabasealreadyupgradedexception-members.md)

[<span data-ttu-id="f956d-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f956d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
