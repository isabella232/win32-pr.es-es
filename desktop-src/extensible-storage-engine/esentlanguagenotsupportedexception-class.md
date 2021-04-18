---
description: 'Más información sobre: clase EsentLanguageNotSupportedException'
title: Clase EsentLanguageNotSupportedException
TOCTitle: EsentLanguageNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLanguageNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlanguagenotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55102130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLanguageNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLanguageNotSupportedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4c977cab062b2ab2eedae2f278edd8168f253013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648451"
---
# <a name="esentlanguagenotsupportedexception-class"></a><span data-ttu-id="d226c-103">Clase EsentLanguageNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="d226c-103">EsentLanguageNotSupportedException class</span></span>

<span data-ttu-id="d226c-104">Clase base para JET_err. Excepciones LanguageNotSupported.</span><span class="sxs-lookup"><span data-stu-id="d226c-104">Base class for JET_err.LanguageNotSupported exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d226c-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="d226c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d226c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d226c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d226c-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d226c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d226c-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d226c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d226c-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d226c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d226c-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="d226c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="d226c-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="d226c-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="d226c-112">Microsoft. ISAM. esent. Interop. EsentLanguageNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="d226c-112">Microsoft.Isam.Esent.Interop.EsentLanguageNotSupportedException</span></span>  

<span data-ttu-id="d226c-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d226c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d226c-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d226c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d226c-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d226c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLanguageNotSupportedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentLanguageNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLanguageNotSupportedException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="d226c-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="d226c-116">Thread safety</span></span>

<span data-ttu-id="d226c-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d226c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d226c-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d226c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d226c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d226c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d226c-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="d226c-120">Reference</span></span>

[<span data-ttu-id="d226c-121">Miembros de EsentLanguageNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="d226c-121">EsentLanguageNotSupportedException members</span></span>](./esentlanguagenotsupportedexception-members.md)

[<span data-ttu-id="d226c-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d226c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
