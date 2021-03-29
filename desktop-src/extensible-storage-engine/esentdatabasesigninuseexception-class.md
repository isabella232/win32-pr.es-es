---
description: 'Más información sobre: clase EsentDatabaseSignInUseException'
title: Clase EsentDatabaseSignInUseException
TOCTitle: EsentDatabaseSignInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseSignInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasesigninuseexception(v=EXCHG.10)
ms:contentKeyID: 55101550
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseSignInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseSignInUseException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ced6fbc9ead499375228f57f864ef2a95370b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648269"
---
# <a name="esentdatabasesigninuseexception-class"></a><span data-ttu-id="dc0c8-103">Clase EsentDatabaseSignInUseException</span><span class="sxs-lookup"><span data-stu-id="dc0c8-103">EsentDatabaseSignInUseException class</span></span>

<span data-ttu-id="dc0c8-104">Clase base para JET_err. Excepciones DatabaseSignInUse.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-104">Base class for JET_err.DatabaseSignInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="dc0c8-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="dc0c8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="dc0c8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="dc0c8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="dc0c8-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="dc0c8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="dc0c8-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="dc0c8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="dc0c8-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="dc0c8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="dc0c8-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="dc0c8-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="dc0c8-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="dc0c8-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="dc0c8-112">Microsoft. ISAM. esent. Interop. EsentDatabaseSignInUseException</span><span class="sxs-lookup"><span data-stu-id="dc0c8-112">Microsoft.Isam.Esent.Interop.EsentDatabaseSignInUseException</span></span>  

<span data-ttu-id="dc0c8-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dc0c8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dc0c8-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dc0c8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0c8-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc0c8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseSignInUseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseSignInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseSignInUseException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="dc0c8-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="dc0c8-116">Thread safety</span></span>

<span data-ttu-id="dc0c8-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="dc0c8-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="dc0c8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc0c8-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc0c8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dc0c8-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="dc0c8-120">Reference</span></span>

[<span data-ttu-id="dc0c8-121">Miembros de EsentDatabaseSignInUseException</span><span class="sxs-lookup"><span data-stu-id="dc0c8-121">EsentDatabaseSignInUseException members</span></span>](./esentdatabasesigninuseexception-members.md)

[<span data-ttu-id="dc0c8-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="dc0c8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
