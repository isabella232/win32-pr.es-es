---
description: 'Más información sobre: clase EsentFileIOBeyondEOFException'
title: Clase EsentFileIOBeyondEOFException
TOCTitle: EsentFileIOBeyondEOFException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileiobeyondeofexception(v=EXCHG.10)
ms:contentKeyID: 55101689
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67d7fa0730a265ddb0ed0f37cc6db250325b5a4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707245"
---
# <a name="esentfileiobeyondeofexception-class"></a><span data-ttu-id="98767-103">Clase EsentFileIOBeyondEOFException</span><span class="sxs-lookup"><span data-stu-id="98767-103">EsentFileIOBeyondEOFException class</span></span>

<span data-ttu-id="98767-104">Clase base para JET_err. Excepciones FileIOBeyondEOF.</span><span class="sxs-lookup"><span data-stu-id="98767-104">Base class for JET_err.FileIOBeyondEOF exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="98767-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="98767-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="98767-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="98767-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="98767-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="98767-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="98767-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="98767-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="98767-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="98767-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="98767-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="98767-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="98767-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="98767-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="98767-112">Microsoft. ISAM. esent. Interop. EsentFileIOBeyondEOFException</span><span class="sxs-lookup"><span data-stu-id="98767-112">Microsoft.Isam.Esent.Interop.EsentFileIOBeyondEOFException</span></span>  

<span data-ttu-id="98767-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="98767-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="98767-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="98767-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="98767-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98767-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileIOBeyondEOFException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentFileIOBeyondEOFException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileIOBeyondEOFException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="98767-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="98767-116">Thread safety</span></span>

<span data-ttu-id="98767-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="98767-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="98767-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="98767-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="98767-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="98767-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="98767-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="98767-120">Reference</span></span>

[<span data-ttu-id="98767-121">Miembros de EsentFileIOBeyondEOFException</span><span class="sxs-lookup"><span data-stu-id="98767-121">EsentFileIOBeyondEOFException members</span></span>](./esentfileiobeyondeofexception-members.md)

[<span data-ttu-id="98767-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="98767-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
