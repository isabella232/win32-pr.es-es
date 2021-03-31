---
description: 'Más información sobre: clase EsentInvalidCodePageException'
title: Clase EsentInvalidCodePageException
TOCTitle: EsentInvalidCodePageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidCodePageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidcodepageexception(v=EXCHG.10)
ms:contentKeyID: 55101881
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidCodePageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidCodePageException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37ff4fb4f5588cb38b8fc5e2e722408f4fb07e07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360733"
---
# <a name="esentinvalidcodepageexception-class"></a><span data-ttu-id="d00e4-103">Clase EsentInvalidCodePageException</span><span class="sxs-lookup"><span data-stu-id="d00e4-103">EsentInvalidCodePageException class</span></span>

<span data-ttu-id="d00e4-104">Clase base para JET_err. Excepciones InvalidCodePage.</span><span class="sxs-lookup"><span data-stu-id="d00e4-104">Base class for JET_err.InvalidCodePage exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d00e4-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="d00e4-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d00e4-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d00e4-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d00e4-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d00e4-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d00e4-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d00e4-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d00e4-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d00e4-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d00e4-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="d00e4-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="d00e4-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="d00e4-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="d00e4-112">Microsoft. ISAM. esent. Interop. EsentInvalidCodePageException</span><span class="sxs-lookup"><span data-stu-id="d00e4-112">Microsoft.Isam.Esent.Interop.EsentInvalidCodePageException</span></span>  

<span data-ttu-id="d00e4-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d00e4-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d00e4-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d00e4-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d00e4-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d00e4-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidCodePageException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidCodePageException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidCodePageException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="d00e4-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="d00e4-116">Thread safety</span></span>

<span data-ttu-id="d00e4-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d00e4-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d00e4-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d00e4-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d00e4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d00e4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d00e4-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="d00e4-120">Reference</span></span>

[<span data-ttu-id="d00e4-121">Miembros de EsentInvalidCodePageException</span><span class="sxs-lookup"><span data-stu-id="d00e4-121">EsentInvalidCodePageException members</span></span>](./esentinvalidcodepageexception-members.md)

[<span data-ttu-id="d00e4-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d00e4-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
