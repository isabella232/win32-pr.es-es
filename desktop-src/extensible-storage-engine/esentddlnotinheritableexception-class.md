---
description: 'Más información sobre: clase EsentDDLNotInheritableException'
title: Clase EsentDDLNotInheritableException
TOCTitle: EsentDDLNotInheritableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentddlnotinheritableexception(v=EXCHG.10)
ms:contentKeyID: 55101474
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8c2a1d4b715bab34d33c12678dcd6808e119921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706014"
---
# <a name="esentddlnotinheritableexception-class"></a><span data-ttu-id="cec42-103">Clase EsentDDLNotInheritableException</span><span class="sxs-lookup"><span data-stu-id="cec42-103">EsentDDLNotInheritableException class</span></span>

<span data-ttu-id="cec42-104">Clase base para JET_err. Excepciones DDLNotInheritable.</span><span class="sxs-lookup"><span data-stu-id="cec42-104">Base class for JET_err.DDLNotInheritable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="cec42-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="cec42-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="cec42-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="cec42-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="cec42-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="cec42-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="cec42-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="cec42-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="cec42-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="cec42-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="cec42-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="cec42-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="cec42-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="cec42-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="cec42-112">Microsoft. ISAM. esent. Interop. EsentDDLNotInheritableException</span><span class="sxs-lookup"><span data-stu-id="cec42-112">Microsoft.Isam.Esent.Interop.EsentDDLNotInheritableException</span></span>  

<span data-ttu-id="cec42-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cec42-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cec42-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cec42-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cec42-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cec42-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDDLNotInheritableException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDDLNotInheritableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDDLNotInheritableException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="cec42-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="cec42-116">Thread safety</span></span>

<span data-ttu-id="cec42-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="cec42-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="cec42-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="cec42-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="cec42-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="cec42-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cec42-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="cec42-120">Reference</span></span>

[<span data-ttu-id="cec42-121">Miembros de EsentDDLNotInheritableException</span><span class="sxs-lookup"><span data-stu-id="cec42-121">EsentDDLNotInheritableException members</span></span>](./esentddlnotinheritableexception-members.md)

[<span data-ttu-id="cec42-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cec42-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
