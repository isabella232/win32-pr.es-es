---
description: 'Más información sobre: clase EsentTooManyOpenTablesException'
title: Clase EsentTooManyOpenTablesException
TOCTitle: EsentTooManyOpenTablesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopentablesexception(v=EXCHG.10)
ms:contentKeyID: 55107362
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 066191af07aab606731f98a16369b2500d24cda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155416"
---
# <a name="esenttoomanyopentablesexception-class"></a><span data-ttu-id="a2c20-103">Clase EsentTooManyOpenTablesException</span><span class="sxs-lookup"><span data-stu-id="a2c20-103">EsentTooManyOpenTablesException class</span></span>

<span data-ttu-id="a2c20-104">Clase base para JET_err. Excepciones TooManyOpenTables.</span><span class="sxs-lookup"><span data-stu-id="a2c20-104">Base class for JET_err.TooManyOpenTables exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a2c20-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="a2c20-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a2c20-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a2c20-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a2c20-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="a2c20-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a2c20-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="a2c20-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a2c20-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a2c20-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a2c20-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="a2c20-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="a2c20-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="a2c20-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="a2c20-112">Microsoft. ISAM. esent. Interop. EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="a2c20-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="a2c20-113">Microsoft. ISAM. esent. Interop. EsentTooManyOpenTablesException</span><span class="sxs-lookup"><span data-stu-id="a2c20-113">Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException</span></span>  

<span data-ttu-id="a2c20-114">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a2c20-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a2c20-115">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a2c20-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c20-116">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2c20-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenTablesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyOpenTablesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenTablesException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="a2c20-117">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="a2c20-117">Thread safety</span></span>

<span data-ttu-id="a2c20-118">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a2c20-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a2c20-119">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a2c20-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2c20-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2c20-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a2c20-121">Referencia</span><span class="sxs-lookup"><span data-stu-id="a2c20-121">Reference</span></span>

[<span data-ttu-id="a2c20-122">Miembros de EsentTooManyOpenTablesException</span><span class="sxs-lookup"><span data-stu-id="a2c20-122">EsentTooManyOpenTablesException members</span></span>](./esenttoomanyopentablesexception-members.md)

[<span data-ttu-id="a2c20-123">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a2c20-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
