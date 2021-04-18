---
description: 'Más información acerca de: <T> interfaz IContentEquatable'
title: IContentEquatable (T) (interfaz)
TOCTitle: IContentEquatable(T) interface
ms:assetid: T:Microsoft.Isam.Esent.Interop.IContentEquatable`1
ms:mtpsurl: https://msdn.microsoft.com/library/Hh578046(v=EXCHG.10)
ms:contentKeyID: 39511318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02e237714f020f5bafa3ce8b7465f1c8e2615c01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666785"
---
# <a name="icontentequatablet-interface"></a><span data-ttu-id="08c8d-103">\<T\>Interfaz IContentEquatable</span><span class="sxs-lookup"><span data-stu-id="08c8d-103">IContentEquatable\<T\> interface</span></span>

<span data-ttu-id="08c8d-104">Interfaz para los objetos que pueden tener su contenido comparado entre sí.</span><span class="sxs-lookup"><span data-stu-id="08c8d-104">Interface for objects that can have their contents compared against each other.</span></span> <span data-ttu-id="08c8d-105">Debe usarse para comparaciones de igualdad en objetos de referencia mutable en los que la invalidación de Equals () y GetHashCode () no es una buena idea.</span><span class="sxs-lookup"><span data-stu-id="08c8d-105">This should be used for equality comparisons on mutable reference objects where overriding Equals() and GetHashCode() isn't a good idea.</span></span>

<span data-ttu-id="08c8d-106">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="08c8d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="08c8d-107">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="08c8d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="08c8d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08c8d-108">Syntax</span></span>

``` vb
'Declaration
Public Interface IContentEquatable(Of T)
'Usage
Dim instance As IContentEquatable(Of T)
```

``` csharp
public interface IContentEquatable<T>
```

#### <a name="type-parameters"></a><span data-ttu-id="08c8d-109">Parámetros de tipo</span><span class="sxs-lookup"><span data-stu-id="08c8d-109">Type parameters</span></span>

  - <span data-ttu-id="08c8d-110">T</span><span class="sxs-lookup"><span data-stu-id="08c8d-110">T</span></span>  
    <span data-ttu-id="08c8d-111">Tipo de objetos que se van a comapre.</span><span class="sxs-lookup"><span data-stu-id="08c8d-111">The type of objects to comapre.</span></span>

## <a name="see-also"></a><span data-ttu-id="08c8d-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="08c8d-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="08c8d-113">Referencia</span><span class="sxs-lookup"><span data-stu-id="08c8d-113">Reference</span></span>

[<span data-ttu-id="08c8d-114">Miembros de IContentEquatable \<T\></span><span class="sxs-lookup"><span data-stu-id="08c8d-114">IContentEquatable\<T\> members</span></span>](./icontentequatable-t-members.md)

[<span data-ttu-id="08c8d-115">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="08c8d-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
