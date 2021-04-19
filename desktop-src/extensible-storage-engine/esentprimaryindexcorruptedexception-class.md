---
description: 'Más información sobre: clase EsentPrimaryIndexCorruptedException'
title: Clase EsentPrimaryIndexCorruptedException
TOCTitle: EsentPrimaryIndexCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentprimaryindexcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102484
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a2d95d50e7cb8ba7bb962686e3c452c35c3b295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716842"
---
# <a name="esentprimaryindexcorruptedexception-class"></a><span data-ttu-id="cb8cf-103">Clase EsentPrimaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="cb8cf-103">EsentPrimaryIndexCorruptedException class</span></span>

<span data-ttu-id="cb8cf-104">Clase base para JET_err. Excepciones PrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-104">Base class for JET_err.PrimaryIndexCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="cb8cf-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="cb8cf-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="cb8cf-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="cb8cf-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="cb8cf-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="cb8cf-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="cb8cf-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="cb8cf-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="cb8cf-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="cb8cf-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="cb8cf-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="cb8cf-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="cb8cf-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="cb8cf-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="cb8cf-112">Microsoft. ISAM. esent. Interop. EsentPrimaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="cb8cf-112">Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException</span></span>  

<span data-ttu-id="cb8cf-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb8cf-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cb8cf-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cb8cf-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb8cf-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb8cf-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPrimaryIndexCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentPrimaryIndexCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPrimaryIndexCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="cb8cf-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="cb8cf-116">Thread safety</span></span>

<span data-ttu-id="cb8cf-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="cb8cf-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="cb8cf-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb8cf-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb8cf-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="cb8cf-120">Reference</span></span>

[<span data-ttu-id="cb8cf-121">Miembros de EsentPrimaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="cb8cf-121">EsentPrimaryIndexCorruptedException members</span></span>](./esentprimaryindexcorruptedexception-members.md)

[<span data-ttu-id="cb8cf-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cb8cf-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
