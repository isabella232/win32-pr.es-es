---
description: 'Más información sobre: Conversions. ConvertDoubleToDateTime (método)'
title: Método Conversions. ConvertDoubleToDateTime
TOCTitle: 'ConvertDoubleToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime(System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.convertdoubletodatetime(v=EXCHG.10)
ms:contentKeyID: 55101133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1d066780ade3da95f4d4d5500143700f7a7d5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697468"
---
# <a name="conversionsconvertdoubletodatetime-method"></a><span data-ttu-id="f679a-103">Método Conversions. ConvertDoubleToDateTime</span><span class="sxs-lookup"><span data-stu-id="f679a-103">Conversions.ConvertDoubleToDateTime method</span></span>

<span data-ttu-id="f679a-104">Convierte un valor Double (formato de fecha y hora de OA) en un valor DateTime.</span><span class="sxs-lookup"><span data-stu-id="f679a-104">Convert a double (OA date time format) to a DateTime.</span></span> <span data-ttu-id="f679a-105">A diferencia de DateTime. FromOADate, esto no inicia excepciones.</span><span class="sxs-lookup"><span data-stu-id="f679a-105">Unlike DateTime.FromOADate this doesn't throw exceptions.</span></span>

<span data-ttu-id="f679a-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f679a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f679a-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f679a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f679a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f679a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function ConvertDoubleToDateTime ( _
    d As Double _
) As DateTime
'Usage
Dim d As Double
Dim returnValue As DateTime

returnValue = Conversions.ConvertDoubleToDateTime(d)
```

``` csharp
public static DateTime ConvertDoubleToDateTime(
    double d
)
```

#### <a name="parameters"></a><span data-ttu-id="f679a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f679a-109">Parameters</span></span>

  - <span data-ttu-id="f679a-110">d</span><span class="sxs-lookup"><span data-stu-id="f679a-110">d</span></span>  
    <span data-ttu-id="f679a-111">Tipo: [System. Double](/dotnet/api/system.double)</span><span class="sxs-lookup"><span data-stu-id="f679a-111">Type: [System.Double](/dotnet/api/system.double)</span></span>  
    
    <span data-ttu-id="f679a-112">Valor Double.</span><span class="sxs-lookup"><span data-stu-id="f679a-112">The double value.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f679a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f679a-113">Return value</span></span>

<span data-ttu-id="f679a-114">Tipo: [System. DateTime](/dotnet/api/system.datetime)</span><span class="sxs-lookup"><span data-stu-id="f679a-114">Type: [System.DateTime](/dotnet/api/system.datetime)</span></span>  
<span data-ttu-id="f679a-115">Un valor de fecha y hora.</span><span class="sxs-lookup"><span data-stu-id="f679a-115">A DateTime.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f679a-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="f679a-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f679a-117">Referencia</span><span class="sxs-lookup"><span data-stu-id="f679a-117">Reference</span></span>

[<span data-ttu-id="f679a-118">Conversions (clase)</span><span class="sxs-lookup"><span data-stu-id="f679a-118">Conversions class</span></span>](./conversions-class.md)

[<span data-ttu-id="f679a-119">Miembros de conversiones</span><span class="sxs-lookup"><span data-stu-id="f679a-119">Conversions members</span></span>](./conversions-members.md)

[<span data-ttu-id="f679a-120">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f679a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
