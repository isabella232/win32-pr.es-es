---
description: 'Más información acerca de: JET_COLUMNID. CompareTo (método)'
title: JET_COLUMNID. CompareTo (método)
TOCTitle: 'CompareTo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo(Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.compareto(v=EXCHG.10)
ms:contentKeyID: 39509744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.CompareTo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7eea24875b0639f7f5b7968084a3fff2aa7cccec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155021"
---
# <a name="jet_columnidcompareto-method"></a><span data-ttu-id="fab25-103">JET_COLUMNID. CompareTo (método)</span><span class="sxs-lookup"><span data-stu-id="fab25-103">JET_COLUMNID.CompareTo method</span></span>

<span data-ttu-id="fab25-104">Compara este columnid con otro columnid y determina si esta instancia es anterior, igual o posterior a la otra instancia.</span><span class="sxs-lookup"><span data-stu-id="fab25-104">Compares this columnid to another columnid and determines whether this instance is before, the same as or after the other instance.</span></span>

<span data-ttu-id="fab25-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fab25-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fab25-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fab25-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fab25-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fab25-107">Syntax</span></span>

``` vb
'Declaration
Public Function CompareTo ( _
    other As JET_COLUMNID _
) As Integer
'Usage
Dim instance As JET_COLUMNID
Dim other As JET_COLUMNID
Dim returnValue As Integer

returnValue = instance.CompareTo(other)
```

``` csharp
public int CompareTo(
    JET_COLUMNID other
)
```

#### <a name="parameters"></a><span data-ttu-id="fab25-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fab25-108">Parameters</span></span>

  - <span data-ttu-id="fab25-109">Otros</span><span class="sxs-lookup"><span data-stu-id="fab25-109">other</span></span>  
    <span data-ttu-id="fab25-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fab25-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="fab25-111">Columnid que se va a comparar con la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="fab25-111">The columnid to compare to the current instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="fab25-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fab25-112">Return value</span></span>

<span data-ttu-id="fab25-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fab25-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="fab25-114">Número con signo que indica las posiciones relativas de esta instancia y el parámetro de valor.</span><span class="sxs-lookup"><span data-stu-id="fab25-114">A signed number indicating the relative positions of this instance and the value parameter.</span></span>  

#### <a name="implements"></a><span data-ttu-id="fab25-115">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="fab25-115">Implements</span></span>

[<span data-ttu-id="fab25-116">IComparable \<T\> . CompareTo (T)</span><span class="sxs-lookup"><span data-stu-id="fab25-116">IComparable\<T\>.CompareTo(T)</span></span>](/dotnet/api/system.icomparable-1.compareto#System_IComparable_1_CompareTo__0_)  

## <a name="see-also"></a><span data-ttu-id="fab25-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="fab25-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fab25-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="fab25-118">Reference</span></span>

[<span data-ttu-id="fab25-119">Estructura de JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="fab25-119">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="fab25-120">Miembros de JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="fab25-120">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="fab25-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fab25-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
