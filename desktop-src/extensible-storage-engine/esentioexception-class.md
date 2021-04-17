---
description: 'Más información sobre: clase EsentIOException'
title: Clase EsentIOException
TOCTitle: EsentIOException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIOException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102033
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIOException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5fbcbf38ae60ae17f74e650c403611a88d89662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707465"
---
# <a name="esentioexception-class"></a><span data-ttu-id="d891a-103">Clase EsentIOException</span><span class="sxs-lookup"><span data-stu-id="d891a-103">EsentIOException class</span></span>

<span data-ttu-id="d891a-104">Clase base para las excepciones de e/s.</span><span class="sxs-lookup"><span data-stu-id="d891a-104">Base class for IO exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d891a-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="d891a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d891a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d891a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d891a-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d891a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d891a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d891a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d891a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d891a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d891a-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="d891a-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="d891a-111">Microsoft. ISAM. esent. Interop. EsentIOException</span><span class="sxs-lookup"><span data-stu-id="d891a-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>  
            [<span data-ttu-id="d891a-112">Microsoft. ISAM. esent. Interop. EsentDeleteBackupFileFailException</span><span class="sxs-lookup"><span data-stu-id="d891a-112">Microsoft.Isam.Esent.Interop.EsentDeleteBackupFileFailException</span></span>](./esentdeletebackupfilefailexception-class.md)  
            [<span data-ttu-id="d891a-113">Microsoft. ISAM. esent. Interop. EsentDiskIOException</span><span class="sxs-lookup"><span data-stu-id="d891a-113">Microsoft.Isam.Esent.Interop.EsentDiskIOException</span></span>](./esentdiskioexception-class.md)  
            [<span data-ttu-id="d891a-114">Microsoft. ISAM. esent. Interop. EsentFileAccessDeniedException</span><span class="sxs-lookup"><span data-stu-id="d891a-114">Microsoft.Isam.Esent.Interop.EsentFileAccessDeniedException</span></span>](./esentfileaccessdeniedexception-class.md)  
            [<span data-ttu-id="d891a-115">Microsoft. ISAM. esent. Interop. EsentLogWriteFailException</span><span class="sxs-lookup"><span data-stu-id="d891a-115">Microsoft.Isam.Esent.Interop.EsentLogWriteFailException</span></span>](./esentlogwritefailexception-class.md)  
            [<span data-ttu-id="d891a-116">Microsoft. ISAM. esent. Interop. EsentMakeBackupDirectoryFailException</span><span class="sxs-lookup"><span data-stu-id="d891a-116">Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException</span></span>](./esentmakebackupdirectoryfailexception-class.md)  

<span data-ttu-id="d891a-117">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d891a-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d891a-118">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d891a-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d891a-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d891a-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentIOException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentIOException
```

``` csharp
[SerializableAttribute]
public abstract class EsentIOException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="d891a-120">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="d891a-120">Thread safety</span></span>

<span data-ttu-id="d891a-121">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d891a-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d891a-122">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d891a-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d891a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="d891a-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d891a-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="d891a-124">Reference</span></span>

[<span data-ttu-id="d891a-125">Miembros de EsentIOException</span><span class="sxs-lookup"><span data-stu-id="d891a-125">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="d891a-126">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d891a-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
