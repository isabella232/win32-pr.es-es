---
description: 'Más información sobre: clase EsentDTCCallbackUnexpectedErrorException'
title: Clase EsentDTCCallbackUnexpectedErrorException
TOCTitle: EsentDTCCallbackUnexpectedErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdtccallbackunexpectederrorexception(v=EXCHG.10)
ms:contentKeyID: 55107266
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ec2d5c2e204d0babeaf1e671d6096b8c52a9b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912729"
---
# <a name="esentdtccallbackunexpectederrorexception-class"></a><span data-ttu-id="74109-103">Clase EsentDTCCallbackUnexpectedErrorException</span><span class="sxs-lookup"><span data-stu-id="74109-103">EsentDTCCallbackUnexpectedErrorException class</span></span>

<span data-ttu-id="74109-104">Clase base para JET_err. Excepciones DTCCallbackUnexpectedError.</span><span class="sxs-lookup"><span data-stu-id="74109-104">Base class for JET_err.DTCCallbackUnexpectedError exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="74109-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="74109-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="74109-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="74109-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="74109-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="74109-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="74109-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="74109-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="74109-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="74109-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="74109-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="74109-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="74109-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="74109-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="74109-112">Microsoft. ISAM. esent. Interop. EsentDTCCallbackUnexpectedErrorException</span><span class="sxs-lookup"><span data-stu-id="74109-112">Microsoft.Isam.Esent.Interop.EsentDTCCallbackUnexpectedErrorException</span></span>  

<span data-ttu-id="74109-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="74109-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="74109-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="74109-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="74109-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74109-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDTCCallbackUnexpectedErrorException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDTCCallbackUnexpectedErrorException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDTCCallbackUnexpectedErrorException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="74109-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="74109-116">Thread safety</span></span>

<span data-ttu-id="74109-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="74109-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="74109-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="74109-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="74109-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="74109-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="74109-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="74109-120">Reference</span></span>

[<span data-ttu-id="74109-121">Miembros de EsentDTCCallbackUnexpectedErrorException</span><span class="sxs-lookup"><span data-stu-id="74109-121">EsentDTCCallbackUnexpectedErrorException members</span></span>](./esentdtccallbackunexpectederrorexception-members.md)

[<span data-ttu-id="74109-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="74109-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
