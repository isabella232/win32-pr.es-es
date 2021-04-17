---
description: 'Más información acerca de: IContentEquatable <T> . Método ContentEquals'
title: IContentEquatable (T). Método ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals(`0)
ms:mtpsurl: https://msdn.microsoft.com/library/Hh538970(v=EXCHG.10)
ms:contentKeyID: 39509953
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IContentEquatable`1.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c3b06307f7c4ebc44242e02ee5ae99a182f9ab3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687176"
---
# <a name="icontentequatabletcontentequals-method"></a><span data-ttu-id="ce7c3-103">IContentEquatable \<T\> . Método ContentEquals</span><span class="sxs-lookup"><span data-stu-id="ce7c3-103">IContentEquatable\<T\>.ContentEquals method</span></span>

<span data-ttu-id="ce7c3-104">Devuelve un valor que indica si esta instancia es igual a otra instancia de.</span><span class="sxs-lookup"><span data-stu-id="ce7c3-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="ce7c3-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ce7c3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ce7c3-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ce7c3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ce7c3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ce7c3-107">Syntax</span></span>

``` vb
'Declaration
Function ContentEquals ( _
    other As T _
) As Boolean
'Usage
Dim instance As IContentEquatable
Dim other As T
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
bool ContentEquals(
    T other
)
```

#### <a name="parameters"></a><span data-ttu-id="ce7c3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ce7c3-108">Parameters</span></span>

  - <span data-ttu-id="ce7c3-109">Otros</span><span class="sxs-lookup"><span data-stu-id="ce7c3-109">other</span></span>  
    <span data-ttu-id="ce7c3-110">Tipo: [T](./icontentequatable-t-interface.md)</span><span class="sxs-lookup"><span data-stu-id="ce7c3-110">Type: [T](./icontentequatable-t-interface.md)</span></span>  
    
    <span data-ttu-id="ce7c3-111">Instancia de que se va a comparar con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="ce7c3-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ce7c3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ce7c3-112">Return value</span></span>

<span data-ttu-id="ce7c3-113">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ce7c3-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="ce7c3-114">True si las dos instancias son iguales.</span><span class="sxs-lookup"><span data-stu-id="ce7c3-114">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce7c3-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce7c3-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ce7c3-116">Referencia</span><span class="sxs-lookup"><span data-stu-id="ce7c3-116">Reference</span></span>

[<span data-ttu-id="ce7c3-117">\<T\>Interfaz IContentEquatable</span><span class="sxs-lookup"><span data-stu-id="ce7c3-117">IContentEquatable\<T\> interface</span></span>](./icontentequatable-t-interface.md)

[<span data-ttu-id="ce7c3-118">Miembros de IContentEquatable \<T\></span><span class="sxs-lookup"><span data-stu-id="ce7c3-118">IContentEquatable\<T\> members</span></span>](./icontentequatable-t-members.md)

[<span data-ttu-id="ce7c3-119">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ce7c3-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
