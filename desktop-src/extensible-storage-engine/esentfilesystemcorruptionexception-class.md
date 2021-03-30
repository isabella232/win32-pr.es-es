---
description: 'Más información sobre: clase EsentFileSystemCorruptionException'
title: Clase EsentFileSystemCorruptionException
TOCTitle: EsentFileSystemCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfilesystemcorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101716
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 863766b5b4b768546ade161abf8c30659db1d720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816667"
---
# <a name="esentfilesystemcorruptionexception-class"></a><span data-ttu-id="24bbe-103">Clase EsentFileSystemCorruptionException</span><span class="sxs-lookup"><span data-stu-id="24bbe-103">EsentFileSystemCorruptionException class</span></span>

<span data-ttu-id="24bbe-104">Clase base para JET_err. Excepciones FileSystemCorruption.</span><span class="sxs-lookup"><span data-stu-id="24bbe-104">Base class for JET_err.FileSystemCorruption exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="24bbe-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="24bbe-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="24bbe-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="24bbe-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="24bbe-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="24bbe-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="24bbe-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="24bbe-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="24bbe-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="24bbe-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="24bbe-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="24bbe-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="24bbe-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="24bbe-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="24bbe-112">Microsoft. ISAM. esent. Interop. EsentFileSystemCorruptionException</span><span class="sxs-lookup"><span data-stu-id="24bbe-112">Microsoft.Isam.Esent.Interop.EsentFileSystemCorruptionException</span></span>  

<span data-ttu-id="24bbe-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="24bbe-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="24bbe-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="24bbe-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="24bbe-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24bbe-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileSystemCorruptionException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentFileSystemCorruptionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileSystemCorruptionException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="24bbe-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="24bbe-116">Thread safety</span></span>

<span data-ttu-id="24bbe-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="24bbe-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="24bbe-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="24bbe-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="24bbe-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="24bbe-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="24bbe-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="24bbe-120">Reference</span></span>

[<span data-ttu-id="24bbe-121">Miembros de EsentFileSystemCorruptionException</span><span class="sxs-lookup"><span data-stu-id="24bbe-121">EsentFileSystemCorruptionException members</span></span>](./esentfilesystemcorruptionexception-members.md)

[<span data-ttu-id="24bbe-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="24bbe-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
