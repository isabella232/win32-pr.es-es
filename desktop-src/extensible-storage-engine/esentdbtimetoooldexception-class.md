---
description: 'Más información sobre: clase EsentDbTimeTooOldException'
title: Clase EsentDbTimeTooOldException
TOCTitle: EsentDbTimeTooOldException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdbtimetoooldexception(v=EXCHG.10)
ms:contentKeyID: 55101581
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12dfb0b661d1bcc1469470c2cc4476f41499e6cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276078"
---
# <a name="esentdbtimetoooldexception-class"></a><span data-ttu-id="045cd-103">Clase EsentDbTimeTooOldException</span><span class="sxs-lookup"><span data-stu-id="045cd-103">EsentDbTimeTooOldException class</span></span>

<span data-ttu-id="045cd-104">Clase base para JET_err. Excepciones DbTimeTooOld.</span><span class="sxs-lookup"><span data-stu-id="045cd-104">Base class for JET_err.DbTimeTooOld exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="045cd-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="045cd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="045cd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="045cd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="045cd-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="045cd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="045cd-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="045cd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="045cd-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="045cd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="045cd-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="045cd-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="045cd-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="045cd-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="045cd-112">Microsoft. ISAM. esent. Interop. EsentDbTimeTooOldException</span><span class="sxs-lookup"><span data-stu-id="045cd-112">Microsoft.Isam.Esent.Interop.EsentDbTimeTooOldException</span></span>  

<span data-ttu-id="045cd-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="045cd-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="045cd-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="045cd-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="045cd-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="045cd-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDbTimeTooOldException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDbTimeTooOldException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDbTimeTooOldException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="045cd-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="045cd-116">Thread safety</span></span>

<span data-ttu-id="045cd-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="045cd-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="045cd-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="045cd-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="045cd-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="045cd-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="045cd-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="045cd-120">Reference</span></span>

[<span data-ttu-id="045cd-121">Miembros de EsentDbTimeTooOldException</span><span class="sxs-lookup"><span data-stu-id="045cd-121">EsentDbTimeTooOldException members</span></span>](./esentdbtimetoooldexception-members.md)

[<span data-ttu-id="045cd-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="045cd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
