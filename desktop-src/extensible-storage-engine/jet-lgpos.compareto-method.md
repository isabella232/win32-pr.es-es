---
description: 'Más información acerca de: JET_LGPOS. CompareTo (método)'
title: JET_LGPOS. CompareTo (método)
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo(Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.compareto(v=EXCHG.10)
ms:contentKeyID: 39514516
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83012ed755ab876618147c013e99868927e16f1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687976"
---
# <a name="jet_lgposcompareto-method"></a><span data-ttu-id="17936-103">JET_LGPOS. CompareTo (método)</span><span class="sxs-lookup"><span data-stu-id="17936-103">JET_LGPOS.CompareTo method</span></span>

<span data-ttu-id="17936-104">Compara esta posición del registro con otra posición del registro y determina si esta instancia es anterior, igual o posterior a la otra instancia.</span><span class="sxs-lookup"><span data-stu-id="17936-104">Compares this log position to another log position and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="17936-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="17936-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="17936-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="17936-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="17936-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17936-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_LGPOS _
) As Integer
'Usage
Dim instance As JET_LGPOS
Dim other As JET_LGPOS
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_LGPOS other
)
```

#### <a name="parameters"></a><span data-ttu-id="17936-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17936-108">Parameters</span></span>

  - <span data-ttu-id="17936-109">Otros</span><span class="sxs-lookup"><span data-stu-id="17936-109">other</span></span>  
    <span data-ttu-id="17936-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="17936-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="17936-111">La posición del registro que se va a comparar con la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="17936-111">The log position to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="17936-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17936-112">Return value</span></span>

<span data-ttu-id="17936-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="17936-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="17936-114">Número con signo que indica las posiciones relativas de esta instancia y el parámetro de valor.</span><span class="sxs-lookup"><span data-stu-id="17936-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="17936-115">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="17936-115">Implements</span></span>

[<span data-ttu-id="17936-116">IComparable \<T\> . CompareTo (T)</span><span class="sxs-lookup"><span data-stu-id="17936-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="17936-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="17936-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="17936-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="17936-118">Reference</span></span>

[<span data-ttu-id="17936-119">Estructura de JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="17936-119">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="17936-120">Miembros de JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="17936-120">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="17936-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="17936-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
