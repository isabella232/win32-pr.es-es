---
description: 'Más información sobre: clase EsentTooManyActiveUsersException'
title: Clase EsentTooManyActiveUsersException
TOCTitle: EsentTooManyActiveUsersException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyActiveUsersException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyactiveusersexception(v=EXCHG.10)
ms:contentKeyID: 55103048
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyActiveUsersException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyActiveUsersException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2376821027d1ef51f2e96dab62c7e9a56542c61d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678439"
---
# <a name="esenttoomanyactiveusersexception-class"></a><span data-ttu-id="6e56c-103">Clase EsentTooManyActiveUsersException</span><span class="sxs-lookup"><span data-stu-id="6e56c-103">EsentTooManyActiveUsersException class</span></span>

<span data-ttu-id="6e56c-104">Clase base para JET_err. Excepciones TooManyActiveUsers.</span><span class="sxs-lookup"><span data-stu-id="6e56c-104">Base class for JET_err.TooManyActiveUsers exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6e56c-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="6e56c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6e56c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6e56c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6e56c-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="6e56c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6e56c-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="6e56c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6e56c-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="6e56c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6e56c-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="6e56c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="6e56c-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="6e56c-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="6e56c-112">Microsoft. ISAM. esent. Interop. EsentTooManyActiveUsersException</span><span class="sxs-lookup"><span data-stu-id="6e56c-112">Microsoft.Isam.Esent.Interop.EsentTooManyActiveUsersException</span></span>  

<span data-ttu-id="6e56c-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6e56c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6e56c-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6e56c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6e56c-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e56c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyActiveUsersException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyActiveUsersException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyActiveUsersException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="6e56c-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="6e56c-116">Thread safety</span></span>

<span data-ttu-id="6e56c-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="6e56c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6e56c-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="6e56c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e56c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e56c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6e56c-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="6e56c-120">Reference</span></span>

[<span data-ttu-id="6e56c-121">Miembros de EsentTooManyActiveUsersException</span><span class="sxs-lookup"><span data-stu-id="6e56c-121">EsentTooManyActiveUsersException members</span></span>](./esenttoomanyactiveusersexception-members.md)

[<span data-ttu-id="6e56c-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6e56c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
