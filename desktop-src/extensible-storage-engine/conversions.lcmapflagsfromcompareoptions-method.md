---
description: 'Más información sobre: Conversions. LCMapFlagsFromCompareOptions (método)'
title: Método Conversions. LCMapFlagsFromCompareOptions
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715415"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a><span data-ttu-id="21693-103">Método Conversions. LCMapFlagsFromCompareOptions</span><span class="sxs-lookup"><span data-stu-id="21693-103">Conversions.LCMapFlagsFromCompareOptions method</span></span>

<span data-ttu-id="21693-104">Asigne a la opción CompareOptions los marcadores de LCMapString.</span><span class="sxs-lookup"><span data-stu-id="21693-104">Give CompareOptions, turn them into flags from LCMapString.</span></span> <span data-ttu-id="21693-105">Se omiten las opciones desconocidas.</span><span class="sxs-lookup"><span data-stu-id="21693-105">Unknown options are ignored.</span></span>

<span data-ttu-id="21693-106">Esta API no es conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="21693-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="21693-107">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="21693-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="21693-108">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="21693-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="21693-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21693-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a><span data-ttu-id="21693-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21693-110">Parameters</span></span>

  - <span data-ttu-id="21693-111">compareOptions</span><span class="sxs-lookup"><span data-stu-id="21693-111">compareOptions</span></span>  
    <span data-ttu-id="21693-112">Tipo: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)</span><span class="sxs-lookup"><span data-stu-id="21693-112">Type: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)</span></span>  
    
    <span data-ttu-id="21693-113">Opciones que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="21693-113">The options to convert.</span></span>

#### <a name="return-value"></a><span data-ttu-id="21693-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21693-114">Return value</span></span>

<span data-ttu-id="21693-115">Tipo: [System. UInt32](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="21693-115">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
<span data-ttu-id="21693-116">Marcas de LCMapString que coinciden con las opciones de comparación.</span><span class="sxs-lookup"><span data-stu-id="21693-116">The LCMapString flags that match the compare options.</span></span> <span data-ttu-id="21693-117">Se omiten las opciones no admitidas.</span><span class="sxs-lookup"><span data-stu-id="21693-117">Unsupported options are ignored.</span></span>  

## <a name="see-also"></a><span data-ttu-id="21693-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="21693-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="21693-119">Referencia</span><span class="sxs-lookup"><span data-stu-id="21693-119">Reference</span></span>

[<span data-ttu-id="21693-120">Conversions (clase)</span><span class="sxs-lookup"><span data-stu-id="21693-120">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="21693-121">Miembros de conversiones</span><span class="sxs-lookup"><span data-stu-id="21693-121">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="21693-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="21693-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
