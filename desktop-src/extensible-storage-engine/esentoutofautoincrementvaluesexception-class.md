---
description: 'Más información sobre: clase EsentOutOfAutoincrementValuesException'
title: Clase EsentOutOfAutoincrementValuesException
TOCTitle: EsentOutOfAutoincrementValuesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofautoincrementvaluesexception(v=EXCHG.10)
ms:contentKeyID: 55102440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a37a25e508281083915cf549db5a1b65a4bdcadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715902"
---
# <a name="esentoutofautoincrementvaluesexception-class"></a><span data-ttu-id="b199c-103">Clase EsentOutOfAutoincrementValuesException</span><span class="sxs-lookup"><span data-stu-id="b199c-103">EsentOutOfAutoincrementValuesException class</span></span>

<span data-ttu-id="b199c-104">Clase base para JET_err. Excepciones OutOfAutoincrementValues.</span><span class="sxs-lookup"><span data-stu-id="b199c-104">Base class for JET_err.OutOfAutoincrementValues exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b199c-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="b199c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b199c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b199c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b199c-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b199c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b199c-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="b199c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b199c-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b199c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b199c-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="b199c-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="b199c-111">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="b199c-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="b199c-112">Microsoft. ISAM. esent. Interop. EsentOutOfAutoincrementValuesException</span><span class="sxs-lookup"><span data-stu-id="b199c-112">Microsoft.Isam.Esent.Interop.EsentOutOfAutoincrementValuesException</span></span>  

<span data-ttu-id="b199c-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b199c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b199c-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b199c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b199c-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b199c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfAutoincrementValuesException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfAutoincrementValuesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfAutoincrementValuesException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="b199c-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="b199c-116">Thread safety</span></span>

<span data-ttu-id="b199c-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b199c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b199c-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="b199c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b199c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b199c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b199c-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="b199c-120">Reference</span></span>

[<span data-ttu-id="b199c-121">Miembros de EsentOutOfAutoincrementValuesException</span><span class="sxs-lookup"><span data-stu-id="b199c-121">EsentOutOfAutoincrementValuesException members</span></span>](./esentoutofautoincrementvaluesexception-members.md)

[<span data-ttu-id="b199c-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b199c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
