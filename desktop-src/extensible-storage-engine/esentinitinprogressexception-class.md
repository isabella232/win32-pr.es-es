---
description: 'Más información sobre: clase EsentInitInProgressException'
title: Clase EsentInitInProgressException
TOCTitle: EsentInitInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInitInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinitinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55101813
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInitInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInitInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b035465e575dd94f68b38cf72f8771c24add49d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648323"
---
# <a name="esentinitinprogressexception-class"></a><span data-ttu-id="1e8c2-103">Clase EsentInitInProgressException</span><span class="sxs-lookup"><span data-stu-id="1e8c2-103">EsentInitInProgressException class</span></span>

<span data-ttu-id="1e8c2-104">Clase base para las excepciones de tInProgress de JET_err.Ini.</span><span class="sxs-lookup"><span data-stu-id="1e8c2-104">Base class for JET_err.InitInProgress exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="1e8c2-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="1e8c2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="1e8c2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="1e8c2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="1e8c2-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="1e8c2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="1e8c2-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="1e8c2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="1e8c2-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="1e8c2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="1e8c2-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="1e8c2-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="1e8c2-111">Microsoft. ISAM. esent. Interop. EsentInitInProgressException</span><span class="sxs-lookup"><span data-stu-id="1e8c2-111">Microsoft.Isam.Esent.Interop.EsentInitInProgressException</span></span>  

<span data-ttu-id="1e8c2-112">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1e8c2-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1e8c2-113">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1e8c2-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1e8c2-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e8c2-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInitInProgressException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentInitInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInitInProgressException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="1e8c2-115">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="1e8c2-115">Thread safety</span></span>

<span data-ttu-id="1e8c2-116">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1e8c2-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="1e8c2-117">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="1e8c2-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e8c2-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e8c2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1e8c2-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="1e8c2-119">Reference</span></span>

[<span data-ttu-id="1e8c2-120">Miembros de EsentInitInProgressException</span><span class="sxs-lookup"><span data-stu-id="1e8c2-120">EsentInitInProgressException members</span></span>](./esentinitinprogressexception-members.md)

[<span data-ttu-id="1e8c2-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1e8c2-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
