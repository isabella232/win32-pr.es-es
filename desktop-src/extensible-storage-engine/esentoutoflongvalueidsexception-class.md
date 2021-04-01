---
description: 'Más información sobre: clase EsentOutOfLongValueIDsException'
title: Clase EsentOutOfLongValueIDsException
TOCTitle: EsentOutOfLongValueIDsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutoflongvalueidsexception(v=EXCHG.10)
ms:contentKeyID: 55102476
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aada406390da086bc209094641a5ceca546d4932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275606"
---
# <a name="esentoutoflongvalueidsexception-class"></a><span data-ttu-id="50004-103">Clase EsentOutOfLongValueIDsException</span><span class="sxs-lookup"><span data-stu-id="50004-103">EsentOutOfLongValueIDsException class</span></span>

<span data-ttu-id="50004-104">Clase base para JET_err. Excepciones OutOfLongValueIDs.</span><span class="sxs-lookup"><span data-stu-id="50004-104">Base class for JET_err.OutOfLongValueIDs exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="50004-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="50004-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="50004-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="50004-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="50004-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="50004-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="50004-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="50004-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="50004-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="50004-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="50004-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="50004-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="50004-111">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="50004-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="50004-112">Microsoft. ISAM. esent. Interop. EsentOutOfLongValueIDsException</span><span class="sxs-lookup"><span data-stu-id="50004-112">Microsoft.Isam.Esent.Interop.EsentOutOfLongValueIDsException</span></span>  

<span data-ttu-id="50004-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="50004-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="50004-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="50004-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="50004-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50004-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfLongValueIDsException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfLongValueIDsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfLongValueIDsException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="50004-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="50004-116">Thread safety</span></span>

<span data-ttu-id="50004-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="50004-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="50004-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="50004-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="50004-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="50004-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="50004-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="50004-120">Reference</span></span>

[<span data-ttu-id="50004-121">Miembros de EsentOutOfLongValueIDsException</span><span class="sxs-lookup"><span data-stu-id="50004-121">EsentOutOfLongValueIDsException members</span></span>](./esentoutoflongvalueidsexception-members.md)

[<span data-ttu-id="50004-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="50004-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
