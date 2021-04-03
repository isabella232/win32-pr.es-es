---
description: 'Más información sobre: clase EsentSessionWriteConflictException'
title: Clase EsentSessionWriteConflictException
TOCTitle: EsentSessionWriteConflictException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessionwriteconflictexception(v=EXCHG.10)
ms:contentKeyID: 55107337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0725bc2d1215e4e71e0e68b2fa7e0d4246a96b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913593"
---
# <a name="esentsessionwriteconflictexception-class"></a><span data-ttu-id="0a835-103">Clase EsentSessionWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="0a835-103">EsentSessionWriteConflictException class</span></span>

<span data-ttu-id="0a835-104">Clase base para JET_err. Excepciones SessionWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="0a835-104">Base class for JET_err.SessionWriteConflict exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0a835-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="0a835-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0a835-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0a835-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0a835-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0a835-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0a835-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0a835-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0a835-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0a835-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0a835-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="0a835-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="0a835-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="0a835-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="0a835-112">Microsoft. ISAM. esent. Interop. EsentSessionWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="0a835-112">Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException</span></span>  

<span data-ttu-id="0a835-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0a835-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0a835-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0a835-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0a835-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a835-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionWriteConflictException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionWriteConflictException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionWriteConflictException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="0a835-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="0a835-116">Thread safety</span></span>

<span data-ttu-id="0a835-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0a835-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0a835-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0a835-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a835-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a835-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0a835-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="0a835-120">Reference</span></span>

[<span data-ttu-id="0a835-121">Miembros de EsentSessionWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="0a835-121">EsentSessionWriteConflictException members</span></span>](./esentsessionwriteconflictexception-members.md)

[<span data-ttu-id="0a835-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0a835-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
