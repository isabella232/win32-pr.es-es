---
description: 'Más información sobre: clase EsentRecordFormatConversionFailedException'
title: Clase EsentRecordFormatConversionFailedException
TOCTitle: EsentRecordFormatConversionFailedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordformatconversionfailedexception(v=EXCHG.10)
ms:contentKeyID: 55102564
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf1895eb3e7068106cc73bedc967b0c113c5c109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697832"
---
# <a name="esentrecordformatconversionfailedexception-class"></a><span data-ttu-id="0f04f-103">Clase EsentRecordFormatConversionFailedException</span><span class="sxs-lookup"><span data-stu-id="0f04f-103">EsentRecordFormatConversionFailedException class</span></span>

<span data-ttu-id="0f04f-104">Clase base para JET_err. Excepciones RecordFormatConversionFailed.</span><span class="sxs-lookup"><span data-stu-id="0f04f-104">Base class for JET_err.RecordFormatConversionFailed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0f04f-105">Jerarquía de herencia</span><span class="sxs-lookup"><span data-stu-id="0f04f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0f04f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0f04f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0f04f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="0f04f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0f04f-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0f04f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0f04f-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0f04f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0f04f-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="0f04f-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="0f04f-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="0f04f-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="0f04f-112">Microsoft. ISAM. esent. Interop. EsentRecordFormatConversionFailedException</span><span class="sxs-lookup"><span data-stu-id="0f04f-112">Microsoft.Isam.Esent.Interop.EsentRecordFormatConversionFailedException</span></span>  

<span data-ttu-id="0f04f-113">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0f04f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0f04f-114">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0f04f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0f04f-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f04f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordFormatConversionFailedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentRecordFormatConversionFailedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordFormatConversionFailedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="0f04f-116">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="0f04f-116">Thread safety</span></span>

<span data-ttu-id="0f04f-117">Todos los miembros estáticos públicos (Shared de Visual Basic) de este tipo son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0f04f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0f04f-118">No se garantiza que los miembros de instancia sean seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="0f04f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f04f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f04f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0f04f-120">Referencia</span><span class="sxs-lookup"><span data-stu-id="0f04f-120">Reference</span></span>

[<span data-ttu-id="0f04f-121">Miembros de EsentRecordFormatConversionFailedException</span><span class="sxs-lookup"><span data-stu-id="0f04f-121">EsentRecordFormatConversionFailedException members</span></span>](./esentrecordformatconversionfailedexception-members.md)

[<span data-ttu-id="0f04f-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0f04f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
