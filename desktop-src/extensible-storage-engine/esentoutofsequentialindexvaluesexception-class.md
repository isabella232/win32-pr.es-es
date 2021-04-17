---
description: 'Más información sobre: clase EsentOutOfSequentialIndexValuesException'
title: Clase EsentOutOfSequentialIndexValuesException
TOCTitle: EsentOutOfSequentialIndexValuesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofsequentialindexvaluesexception(v=EXCHG.10)
ms:contentKeyID: 55107300
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e7bf70b63e4c5318f13704c176b55dfe7d98f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667655"
---
# <a name="esentoutofsequentialindexvaluesexception-class"></a><span data-ttu-id="3bed3-103">Clase EsentOutOfSequentialIndexValuesException</span><span class="sxs-lookup"><span data-stu-id="3bed3-103">EsentOutOfSequentialIndexValuesException class</span></span>

<span data-ttu-id="3bed3-104">Clase base para JET_err. Excepciones OutOfSequentialIndexValues.</span><span class="sxs-lookup"><span data-stu-id="3bed3-104">Base class for JET_err.OutOfSequentialIndexValues exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3bed3-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="3bed3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3bed3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3bed3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3bed3-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="3bed3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3bed3-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="3bed3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3bed3-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="3bed3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3bed3-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="3bed3-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="3bed3-111">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="3bed3-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="3bed3-112">Microsoft. ISAM. esent. Interop. EsentOutOfSequentialIndexValuesException</span><span class="sxs-lookup"><span data-stu-id="3bed3-112">Microsoft.Isam.Esent.Interop.EsentOutOfSequentialIndexValuesException</span></span>  

<span data-ttu-id="3bed3-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3bed3-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3bed3-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3bed3-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3bed3-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bed3-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfSequentialIndexValuesException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfSequentialIndexValuesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfSequentialIndexValuesException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="3bed3-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="3bed3-116">Thread safety</span></span>

<span data-ttu-id="3bed3-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="3bed3-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3bed3-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="3bed3-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3bed3-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="3bed3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3bed3-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="3bed3-120">Reference</span></span>

[<span data-ttu-id="3bed3-121">Miembros de EsentOutOfSequentialIndexValuesException</span><span class="sxs-lookup"><span data-stu-id="3bed3-121">EsentOutOfSequentialIndexValuesException members</span></span>](./esentoutofsequentialindexvaluesexception-members.md)

[<span data-ttu-id="3bed3-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3bed3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
