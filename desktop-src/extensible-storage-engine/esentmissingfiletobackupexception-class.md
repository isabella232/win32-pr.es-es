---
description: 'Más información sobre: clase EsentMissingFileToBackupException'
title: Clase EsentMissingFileToBackupException
TOCTitle: EsentMissingFileToBackupException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingfiletobackupexception(v=EXCHG.10)
ms:contentKeyID: 55102216
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5941140df070abb3a273378f3ec275eaf1c6fdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276052"
---
# <a name="esentmissingfiletobackupexception-class"></a><span data-ttu-id="d53c9-103">Clase EsentMissingFileToBackupException</span><span class="sxs-lookup"><span data-stu-id="d53c9-103">EsentMissingFileToBackupException class</span></span>

<span data-ttu-id="d53c9-104">Clase base para JET_err. Excepciones MissingFileToBackup.</span><span class="sxs-lookup"><span data-stu-id="d53c9-104">Base class for JET_err.MissingFileToBackup exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d53c9-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="d53c9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d53c9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d53c9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d53c9-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="d53c9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d53c9-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d53c9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d53c9-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d53c9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d53c9-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="d53c9-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="d53c9-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="d53c9-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="d53c9-112">Microsoft. ISAM. esent. Interop. EsentMissingFileToBackupException</span><span class="sxs-lookup"><span data-stu-id="d53c9-112">Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException</span></span>  

<span data-ttu-id="d53c9-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d53c9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d53c9-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d53c9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d53c9-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d53c9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingFileToBackupException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingFileToBackupException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingFileToBackupException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="d53c9-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="d53c9-116">Thread safety</span></span>

<span data-ttu-id="d53c9-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d53c9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d53c9-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d53c9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d53c9-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="d53c9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d53c9-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="d53c9-120">Reference</span></span>

[<span data-ttu-id="d53c9-121">Miembros de EsentMissingFileToBackupException</span><span class="sxs-lookup"><span data-stu-id="d53c9-121">EsentMissingFileToBackupException members</span></span>](./esentmissingfiletobackupexception-members.md)

[<span data-ttu-id="d53c9-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d53c9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
