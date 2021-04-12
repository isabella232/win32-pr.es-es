---
description: 'Más información sobre: clase EsentInvalidDatabaseVersionException'
title: Clase EsentInvalidDatabaseVersionException
TOCTitle: EsentInvalidDatabaseVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvaliddatabaseversionexception(v=EXCHG.10)
ms:contentKeyID: 55101922
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24b3e348c0c0adaf4d261705c1e4de7bf5d7297b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279589"
---
# <a name="esentinvaliddatabaseversionexception-class"></a><span data-ttu-id="2e271-103">Clase EsentInvalidDatabaseVersionException</span><span class="sxs-lookup"><span data-stu-id="2e271-103">EsentInvalidDatabaseVersionException class</span></span>

<span data-ttu-id="2e271-104">Clase base para JET_err. Excepciones InvalidDatabaseVersion.</span><span class="sxs-lookup"><span data-stu-id="2e271-104">Base class for JET_err.InvalidDatabaseVersion exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2e271-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="2e271-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2e271-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2e271-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2e271-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2e271-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2e271-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="2e271-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2e271-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2e271-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2e271-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="2e271-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="2e271-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="2e271-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="2e271-112">Microsoft. ISAM. esent. Interop. EsentInvalidDatabaseVersionException</span><span class="sxs-lookup"><span data-stu-id="2e271-112">Microsoft.Isam.Esent.Interop.EsentInvalidDatabaseVersionException</span></span>  

<span data-ttu-id="2e271-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2e271-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2e271-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2e271-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2e271-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e271-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidDatabaseVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentInvalidDatabaseVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidDatabaseVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="2e271-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="2e271-116">Thread safety</span></span>

<span data-ttu-id="2e271-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="2e271-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2e271-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="2e271-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e271-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e271-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2e271-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="2e271-120">Reference</span></span>

[<span data-ttu-id="2e271-121">Miembros de EsentInvalidDatabaseVersionException</span><span class="sxs-lookup"><span data-stu-id="2e271-121">EsentInvalidDatabaseVersionException members</span></span>](./esentinvaliddatabaseversionexception-members.md)

[<span data-ttu-id="2e271-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2e271-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
