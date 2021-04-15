---
description: 'Más información acerca de: JET_HANDLE. Equals (método JET_HANDLE)'
title: JET_HANDLE. Equals (método JET_HANDLE)
TOCTitle: Equals method (JET_HANDLE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals(Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.equals(v=EXCHG.10)
ms:contentKeyID: 39515292
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ab4ea5df734b626e54a70bc690301e755013ae59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649245"
---
# <a name="jet_handleequals-method-jet_handle"></a><span data-ttu-id="6e3de-103">JET_HANDLE. Equals (método JET_HANDLE)</span><span class="sxs-lookup"><span data-stu-id="6e3de-103">JET_HANDLE.Equals method (JET_HANDLE)</span></span>

<span data-ttu-id="6e3de-104">Devuelve un valor que indica si esta instancia es igual a otra instancia de.</span><span class="sxs-lookup"><span data-stu-id="6e3de-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="6e3de-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6e3de-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6e3de-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6e3de-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6e3de-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e3de-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_HANDLE _
) As Boolean
'Usage
Dim instance As JET_HANDLE
Dim other As JET_HANDLE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_HANDLE other
)
```

#### <a name="parameters"></a><span data-ttu-id="6e3de-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e3de-108">Parameters</span></span>

  - <span data-ttu-id="6e3de-109">Otros</span><span class="sxs-lookup"><span data-stu-id="6e3de-109">other</span></span>  
    <span data-ttu-id="6e3de-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6e3de-110">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="6e3de-111">Instancia de que se va a comparar con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="6e3de-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6e3de-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e3de-112">Return value</span></span>

<span data-ttu-id="6e3de-113">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="6e3de-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="6e3de-114">True si las dos instancias son iguales.</span><span class="sxs-lookup"><span data-stu-id="6e3de-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="6e3de-115">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="6e3de-115">Implements</span></span>

[<span data-ttu-id="6e3de-116">IEquatable \<T\> . Es igual a (T)</span><span class="sxs-lookup"><span data-stu-id="6e3de-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="6e3de-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e3de-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6e3de-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="6e3de-118">Reference</span></span>

[<span data-ttu-id="6e3de-119">Estructura de JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="6e3de-119">JET_HANDLE structure</span></span>](./jet-handle-structure.md)

[<span data-ttu-id="6e3de-120">Miembros de JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="6e3de-120">JET_HANDLE members</span></span>](./jet-handle-members.md)

[<span data-ttu-id="6e3de-121">Equals (sobrecarga)</span><span class="sxs-lookup"><span data-stu-id="6e3de-121">Equals overload</span></span>](./jet-handle.equals-method.md)

[<span data-ttu-id="6e3de-122">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6e3de-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
