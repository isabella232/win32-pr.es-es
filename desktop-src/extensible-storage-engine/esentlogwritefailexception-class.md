---
description: 'Más información sobre: clase EsentLogWriteFailException'
title: Clase EsentLogWriteFailException
TOCTitle: EsentLogWriteFailException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogwritefailexception(v=EXCHG.10)
ms:contentKeyID: 55102169
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9cd3fe6b541a58b7498ca4117f7ba2af7662d5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706542"
---
# <a name="esentlogwritefailexception-class"></a><span data-ttu-id="2706d-103">Clase EsentLogWriteFailException</span><span class="sxs-lookup"><span data-stu-id="2706d-103">EsentLogWriteFailException class</span></span>

<span data-ttu-id="2706d-104">Clase base para JET_err. Excepciones LogWriteFail.</span><span class="sxs-lookup"><span data-stu-id="2706d-104">Base class for JET_err.LogWriteFail exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2706d-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="2706d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2706d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2706d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2706d-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="2706d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2706d-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="2706d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2706d-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2706d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2706d-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="2706d-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="2706d-111">Microsoft. ISAM. esent. Interop. EsentIOException</span><span class="sxs-lookup"><span data-stu-id="2706d-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
            <span data-ttu-id="2706d-112">Microsoft. ISAM. esent. Interop. EsentLogWriteFailException</span><span class="sxs-lookup"><span data-stu-id="2706d-112">Microsoft.Isam.Esent.Interop.EsentLogWriteFailException</span></span>  

<span data-ttu-id="2706d-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2706d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2706d-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2706d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2706d-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2706d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogWriteFailException _
    Inherits EsentIOException
'Usage
Dim instance As EsentLogWriteFailException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogWriteFailException : EsentIOException
```

## <a name="thread-safety"></a><span data-ttu-id="2706d-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="2706d-116">Thread safety</span></span>

<span data-ttu-id="2706d-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="2706d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2706d-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="2706d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2706d-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2706d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2706d-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="2706d-120">Reference</span></span>

[<span data-ttu-id="2706d-121">Miembros de EsentLogWriteFailException</span><span class="sxs-lookup"><span data-stu-id="2706d-121">EsentLogWriteFailException members</span></span>](./esentlogwritefailexception-members.md)

[<span data-ttu-id="2706d-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2706d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
