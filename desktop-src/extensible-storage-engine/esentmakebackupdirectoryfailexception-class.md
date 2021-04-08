---
description: 'Más información sobre: clase EsentMakeBackupDirectoryFailException'
title: Clase EsentMakeBackupDirectoryFailException
TOCTitle: EsentMakeBackupDirectoryFailException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmakebackupdirectoryfailexception(v=EXCHG.10)
ms:contentKeyID: 55102252
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aae8fdbf432656d5b75619c00b7aa230d2e22ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001690"
---
# <a name="esentmakebackupdirectoryfailexception-class"></a><span data-ttu-id="55452-103">Clase EsentMakeBackupDirectoryFailException</span><span class="sxs-lookup"><span data-stu-id="55452-103">EsentMakeBackupDirectoryFailException class</span></span>

<span data-ttu-id="55452-104">Clase base para JET_err. Excepciones MakeBackupDirectoryFail.</span><span class="sxs-lookup"><span data-stu-id="55452-104">Base class for JET_err.MakeBackupDirectoryFail exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="55452-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="55452-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="55452-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="55452-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="55452-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="55452-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="55452-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="55452-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="55452-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="55452-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="55452-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="55452-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="55452-111">Microsoft. ISAM. esent. Interop. EsentIOException</span><span class="sxs-lookup"><span data-stu-id="55452-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
            <span data-ttu-id="55452-112">Microsoft. ISAM. esent. Interop. EsentMakeBackupDirectoryFailException</span><span class="sxs-lookup"><span data-stu-id="55452-112">Microsoft.Isam.Esent.Interop.EsentMakeBackupDirectoryFailException</span></span>  

<span data-ttu-id="55452-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55452-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="55452-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55452-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55452-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55452-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMakeBackupDirectoryFailException _
    Inherits EsentIOException
'Usage
Dim instance As EsentMakeBackupDirectoryFailException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMakeBackupDirectoryFailException : EsentIOException
```

## <a name="thread-safety"></a><span data-ttu-id="55452-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="55452-116">Thread safety</span></span>

<span data-ttu-id="55452-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="55452-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="55452-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="55452-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="55452-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="55452-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55452-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="55452-120">Reference</span></span>

[<span data-ttu-id="55452-121">Miembros de EsentMakeBackupDirectoryFailException</span><span class="sxs-lookup"><span data-stu-id="55452-121">EsentMakeBackupDirectoryFailException members</span></span>](./esentmakebackupdirectoryfailexception-members.md)

[<span data-ttu-id="55452-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="55452-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
