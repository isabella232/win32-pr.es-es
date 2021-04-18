---
description: 'Más información sobre: clase EsentDatabaseInvalidPathException'
title: Clase EsentDatabaseInvalidPathException
TOCTitle: EsentDatabaseInvalidPathException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPathException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseinvalidpathexception(v=EXCHG.10)
ms:contentKeyID: 55101511
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPathException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPathException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd275a599aa8b2cb8fb6f072ef1a413706d2c175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707392"
---
# <a name="esentdatabaseinvalidpathexception-class"></a><span data-ttu-id="abc31-103">Clase EsentDatabaseInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="abc31-103">EsentDatabaseInvalidPathException class</span></span>

<span data-ttu-id="abc31-104">Clase base para JET_err. Excepciones DatabaseInvalidPath.</span><span class="sxs-lookup"><span data-stu-id="abc31-104">Base class for JET_err.DatabaseInvalidPath exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="abc31-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="abc31-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="abc31-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="abc31-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="abc31-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="abc31-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="abc31-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="abc31-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="abc31-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="abc31-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="abc31-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="abc31-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="abc31-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="abc31-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="abc31-112">Microsoft. ISAM. esent. Interop. EsentDatabaseInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="abc31-112">Microsoft.Isam.Esent.Interop.EsentDatabaseInvalidPathException</span></span>  

<span data-ttu-id="abc31-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="abc31-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="abc31-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="abc31-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="abc31-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abc31-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseInvalidPathException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseInvalidPathException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseInvalidPathException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="abc31-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="abc31-116">Thread safety</span></span>

<span data-ttu-id="abc31-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="abc31-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="abc31-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="abc31-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="abc31-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="abc31-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="abc31-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="abc31-120">Reference</span></span>

[<span data-ttu-id="abc31-121">Miembros de EsentDatabaseInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="abc31-121">EsentDatabaseInvalidPathException members</span></span>](./esentdatabaseinvalidpathexception-members.md)

[<span data-ttu-id="abc31-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="abc31-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
