---
description: 'Más información sobre: clase EsentDTCMissingCallbackException'
title: Clase EsentDTCMissingCallbackException
TOCTitle: EsentDTCMissingCallbackException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdtcmissingcallbackexception(v=EXCHG.10)
ms:contentKeyID: 55101556
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3e9409b03b103ade25fde08fd01949a1a84dbf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545622"
---
# <a name="esentdtcmissingcallbackexception-class"></a><span data-ttu-id="4ff28-103">Clase EsentDTCMissingCallbackException</span><span class="sxs-lookup"><span data-stu-id="4ff28-103">EsentDTCMissingCallbackException class</span></span>

<span data-ttu-id="4ff28-104">Clase base para JET_err. Excepciones DTCMissingCallback.</span><span class="sxs-lookup"><span data-stu-id="4ff28-104">Base class for JET_err.DTCMissingCallback exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4ff28-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="4ff28-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4ff28-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4ff28-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4ff28-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="4ff28-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4ff28-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="4ff28-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4ff28-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="4ff28-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4ff28-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="4ff28-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4ff28-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="4ff28-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="4ff28-112">Microsoft. ISAM. esent. Interop. EsentDTCMissingCallbackException</span><span class="sxs-lookup"><span data-stu-id="4ff28-112">Microsoft.Isam.Esent.Interop.EsentDTCMissingCallbackException</span></span>  

<span data-ttu-id="4ff28-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ff28-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ff28-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4ff28-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ff28-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ff28-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDTCMissingCallbackException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDTCMissingCallbackException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDTCMissingCallbackException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="4ff28-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="4ff28-116">Thread safety</span></span>

<span data-ttu-id="4ff28-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4ff28-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4ff28-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="4ff28-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ff28-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ff28-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ff28-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="4ff28-120">Reference</span></span>

[<span data-ttu-id="4ff28-121">Miembros de EsentDTCMissingCallbackException</span><span class="sxs-lookup"><span data-stu-id="4ff28-121">EsentDTCMissingCallbackException members</span></span>](./esentdtcmissingcallbackexception-members.md)

[<span data-ttu-id="4ff28-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4ff28-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
