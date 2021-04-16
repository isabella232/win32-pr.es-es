---
description: 'Más información sobre: clase EsentLogSequenceEndException'
title: Clase EsentLogSequenceEndException
TOCTitle: EsentLogSequenceEndException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogsequenceendexception(v=EXCHG.10)
ms:contentKeyID: 55102213
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78de803d31d8e97f9493d605d688916501edba6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276061"
---
# <a name="esentlogsequenceendexception-class"></a><span data-ttu-id="6ed22-103">Clase EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="6ed22-103">EsentLogSequenceEndException class</span></span>

<span data-ttu-id="6ed22-104">Clase base para JET_err. Excepciones LogSequenceEnd.</span><span class="sxs-lookup"><span data-stu-id="6ed22-104">Base class for JET_err.LogSequenceEnd exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6ed22-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="6ed22-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6ed22-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6ed22-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6ed22-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="6ed22-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6ed22-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="6ed22-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6ed22-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="6ed22-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6ed22-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="6ed22-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="6ed22-111">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="6ed22-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="6ed22-112">Microsoft. ISAM. esent. Interop. EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="6ed22-112">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException</span></span>  

<span data-ttu-id="6ed22-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6ed22-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6ed22-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6ed22-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6ed22-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ed22-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogSequenceEndException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentLogSequenceEndException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogSequenceEndException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="6ed22-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="6ed22-116">Thread safety</span></span>

<span data-ttu-id="6ed22-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="6ed22-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6ed22-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="6ed22-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ed22-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ed22-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6ed22-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="6ed22-120">Reference</span></span>

[<span data-ttu-id="6ed22-121">Miembros de EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="6ed22-121">EsentLogSequenceEndException members</span></span>](./esentlogsequenceendexception-members.md)

[<span data-ttu-id="6ed22-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6ed22-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
