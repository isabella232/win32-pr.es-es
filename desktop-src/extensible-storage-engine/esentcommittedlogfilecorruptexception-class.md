---
description: 'Más información sobre: clase EsentCommittedLogFileCorruptException'
title: Clase EsentCommittedLogFileCorruptException
TOCTitle: EsentCommittedLogFileCorruptException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcommittedlogfilecorruptexception(v=EXCHG.10)
ms:contentKeyID: 55101273
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbc9d9342da650838aca4a291cc0196bc40fc77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705463"
---
# <a name="esentcommittedlogfilecorruptexception-class"></a><span data-ttu-id="82fe9-103">Clase EsentCommittedLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="82fe9-103">EsentCommittedLogFileCorruptException class</span></span>

<span data-ttu-id="82fe9-104">Clase base para las excepciones JET_err. CommittedLogFileCorrupt.</span><span class="sxs-lookup"><span data-stu-id="82fe9-104">Base class for JET_err.CommittedLogFileCorrupt exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="82fe9-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="82fe9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="82fe9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="82fe9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="82fe9-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="82fe9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="82fe9-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="82fe9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="82fe9-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="82fe9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="82fe9-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="82fe9-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="82fe9-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="82fe9-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="82fe9-112">Microsoft. ISAM. esent. Interop. EsentCommittedLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="82fe9-112">Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException</span></span>  

<span data-ttu-id="82fe9-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="82fe9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="82fe9-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="82fe9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="82fe9-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82fe9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCommittedLogFileCorruptException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentCommittedLogFileCorruptException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCommittedLogFileCorruptException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="82fe9-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="82fe9-116">Thread safety</span></span>

<span data-ttu-id="82fe9-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="82fe9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="82fe9-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="82fe9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="82fe9-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="82fe9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="82fe9-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="82fe9-120">Reference</span></span>

[<span data-ttu-id="82fe9-121">Miembros de EsentCommittedLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="82fe9-121">EsentCommittedLogFileCorruptException members</span></span>](./esentcommittedlogfilecorruptexception-members.md)

[<span data-ttu-id="82fe9-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="82fe9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
