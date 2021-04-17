---
description: 'Más información sobre: clase EsentCannotDeleteTempTableException'
title: Clase EsentCannotDeleteTempTableException
TOCTitle: EsentCannotDeleteTempTableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotdeletetemptableexception(v=EXCHG.10)
ms:contentKeyID: 55101145
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f333798a6b151b63cbd40c69fab438ecdff68ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716749"
---
# <a name="esentcannotdeletetemptableexception-class"></a><span data-ttu-id="a17c4-103">Clase EsentCannotDeleteTempTableException</span><span class="sxs-lookup"><span data-stu-id="a17c4-103">EsentCannotDeleteTempTableException class</span></span>

<span data-ttu-id="a17c4-104">Clase base para JET_err. Excepciones CannotDeleteTempTable.</span><span class="sxs-lookup"><span data-stu-id="a17c4-104">Base class for JET_err.CannotDeleteTempTable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a17c4-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="a17c4-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a17c4-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a17c4-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a17c4-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a17c4-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a17c4-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="a17c4-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a17c4-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a17c4-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a17c4-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="a17c4-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a17c4-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="a17c4-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="a17c4-112">Microsoft. ISAM. esent. Interop. EsentCannotDeleteTempTableException</span><span class="sxs-lookup"><span data-stu-id="a17c4-112">Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException</span></span>  

<span data-ttu-id="a17c4-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a17c4-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a17c4-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a17c4-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a17c4-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a17c4-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotDeleteTempTableException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotDeleteTempTableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotDeleteTempTableException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="a17c4-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="a17c4-116">Thread safety</span></span>

<span data-ttu-id="a17c4-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a17c4-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a17c4-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a17c4-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a17c4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="a17c4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a17c4-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="a17c4-120">Reference</span></span>

[<span data-ttu-id="a17c4-121">Miembros de EsentCannotDeleteTempTableException</span><span class="sxs-lookup"><span data-stu-id="a17c4-121">EsentCannotDeleteTempTableException members</span></span>](./esentcannotdeletetemptableexception-members.md)

[<span data-ttu-id="a17c4-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a17c4-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
