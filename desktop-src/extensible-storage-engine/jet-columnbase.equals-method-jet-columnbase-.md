---
description: 'Más información acerca de: JET_COLUMNBASE. Equals (método JET_COLUMNBASE)'
title: JET_COLUMNBASE. Equals (método JET_COLUMNBASE)
TOCTitle: Equals method (JET_COLUMNBASE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals(Microsoft.Isam.Esent.Interop.JET_COLUMNBASE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.equals(v=EXCHG.10)
ms:contentKeyID: 55103355
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ada65f03966ebd5f0bf7142d3953117734c2f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913581"
---
# <a name="jet_columnbaseequals-method-jet_columnbase"></a><span data-ttu-id="b5f48-103">JET_COLUMNBASE. Equals (método JET_COLUMNBASE)</span><span class="sxs-lookup"><span data-stu-id="b5f48-103">JET_COLUMNBASE.Equals method (JET_COLUMNBASE)</span></span>

<span data-ttu-id="b5f48-104">Devuelve un valor que indica si esta instancia es igual a otra instancia de.</span><span class="sxs-lookup"><span data-stu-id="b5f48-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="b5f48-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b5f48-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b5f48-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b5f48-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f48-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5f48-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_COLUMNBASE _
) As Boolean
'Usage
Dim instance As JET_COLUMNBASE
Dim other As JET_COLUMNBASE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_COLUMNBASE other
)
```

#### <a name="parameters"></a><span data-ttu-id="b5f48-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5f48-108">Parameters</span></span>

  - <span data-ttu-id="b5f48-109">Otros</span><span class="sxs-lookup"><span data-stu-id="b5f48-109">other</span></span>  
    <span data-ttu-id="b5f48-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="b5f48-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="b5f48-111">Instancia de que se va a comparar con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="b5f48-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b5f48-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5f48-112">Return value</span></span>

<span data-ttu-id="b5f48-113">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b5f48-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b5f48-114">True si las dos instancias son iguales.</span><span class="sxs-lookup"><span data-stu-id="b5f48-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="b5f48-115">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="b5f48-115">Implements</span></span>

[<span data-ttu-id="b5f48-116">IEquatable \<T\> . Es igual a (T)</span><span class="sxs-lookup"><span data-stu-id="b5f48-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="b5f48-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5f48-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b5f48-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="b5f48-118">Reference</span></span>

[<span data-ttu-id="b5f48-119">JET_COLUMNBASE (clase)</span><span class="sxs-lookup"><span data-stu-id="b5f48-119">JET_COLUMNBASE class</span></span>](./jet-columnbase-class.md)

[<span data-ttu-id="b5f48-120">Miembros de JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="b5f48-120">JET_COLUMNBASE members</span></span>](./jet-columnbase-members.md)

[<span data-ttu-id="b5f48-121">Equals (sobrecarga)</span><span class="sxs-lookup"><span data-stu-id="b5f48-121">Equals overload</span></span>](./jet-columnbase.equals-method.md)

[<span data-ttu-id="b5f48-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b5f48-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
