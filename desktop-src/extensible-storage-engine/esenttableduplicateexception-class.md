---
description: 'Más información sobre: clase EsentTableDuplicateException'
title: Clase EsentTableDuplicateException
TOCTitle: EsentTableDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTableDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttableduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55103013
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTableDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTableDuplicateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd6edfbb8990485a5e631c41f22f7156b2809e5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697280"
---
# <a name="esenttableduplicateexception-class"></a><span data-ttu-id="7c543-103">Clase EsentTableDuplicateException</span><span class="sxs-lookup"><span data-stu-id="7c543-103">EsentTableDuplicateException class</span></span>

<span data-ttu-id="7c543-104">Clase base para JET_err. Excepciones TableDuplicate.</span><span class="sxs-lookup"><span data-stu-id="7c543-104">Base class for JET_err.TableDuplicate exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7c543-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="7c543-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7c543-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7c543-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7c543-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="7c543-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7c543-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="7c543-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7c543-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="7c543-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7c543-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="7c543-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="7c543-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="7c543-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="7c543-112">Microsoft. ISAM. esent. Interop. EsentTableDuplicateException</span><span class="sxs-lookup"><span data-stu-id="7c543-112">Microsoft.Isam.Esent.Interop.EsentTableDuplicateException</span></span>  

<span data-ttu-id="7c543-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7c543-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7c543-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7c543-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7c543-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c543-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTableDuplicateException _
    Inherits EsentStateException
'Usage
Dim instance As EsentTableDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTableDuplicateException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="7c543-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="7c543-116">Thread safety</span></span>

<span data-ttu-id="7c543-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="7c543-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7c543-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="7c543-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c543-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c543-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7c543-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="7c543-120">Reference</span></span>

[<span data-ttu-id="7c543-121">Miembros de EsentTableDuplicateException</span><span class="sxs-lookup"><span data-stu-id="7c543-121">EsentTableDuplicateException members</span></span>](./esenttableduplicateexception-members.md)

[<span data-ttu-id="7c543-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7c543-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
