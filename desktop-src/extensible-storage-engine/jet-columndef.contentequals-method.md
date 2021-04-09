---
description: 'Más información acerca de: JET_COLUMNDEF. Método ContentEquals'
title: JET_COLUMNDEF. Método ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals(Microsoft.Isam.Esent.Interop.JET_COLUMNDEF)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103479
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f4527edef1fd8567ec3f4973dddc67548e79946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155028"
---
# <a name="jet_columndefcontentequals-method"></a><span data-ttu-id="ad2b7-103">JET_COLUMNDEF. Método ContentEquals</span><span class="sxs-lookup"><span data-stu-id="ad2b7-103">JET_COLUMNDEF.ContentEquals method</span></span>

<span data-ttu-id="ad2b7-104">Devuelve un valor que indica si esta instancia es igual a otra instancia de.</span><span class="sxs-lookup"><span data-stu-id="ad2b7-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="ad2b7-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ad2b7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ad2b7-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ad2b7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ad2b7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad2b7-107">Syntax</span></span>

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_COLUMNDEF _
) As Boolean
'Usage
Dim instance As JET_COLUMNDEF
Dim other As JET_COLUMNDEF
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_COLUMNDEF other
)
```

#### <a name="parameters"></a><span data-ttu-id="ad2b7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad2b7-108">Parameters</span></span>

  - <span data-ttu-id="ad2b7-109">Otros</span><span class="sxs-lookup"><span data-stu-id="ad2b7-109">other</span></span>  
    <span data-ttu-id="ad2b7-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span><span class="sxs-lookup"><span data-stu-id="ad2b7-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)</span></span>  
    
    <span data-ttu-id="ad2b7-111">Instancia de que se va a comparar con esta instancia.</span><span class="sxs-lookup"><span data-stu-id="ad2b7-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ad2b7-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad2b7-112">Return value</span></span>

<span data-ttu-id="ad2b7-113">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ad2b7-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="ad2b7-114">True si las dos instancias son iguales.</span><span class="sxs-lookup"><span data-stu-id="ad2b7-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="ad2b7-115">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="ad2b7-115">Implements</span></span>

[<span data-ttu-id="ad2b7-116">IContentEquatable \<T\> . ContentEquals (T)</span><span class="sxs-lookup"><span data-stu-id="ad2b7-116">IContentEquatable\<T\>.ContentEquals(T)</span></span>](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a><span data-ttu-id="ad2b7-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad2b7-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ad2b7-118">Referencia</span><span class="sxs-lookup"><span data-stu-id="ad2b7-118">Reference</span></span>

[<span data-ttu-id="ad2b7-119">JET_COLUMNDEF (clase)</span><span class="sxs-lookup"><span data-stu-id="ad2b7-119">JET_COLUMNDEF class</span></span>](./jet-columndef-class.md)

[<span data-ttu-id="ad2b7-120">Miembros de JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="ad2b7-120">JET_COLUMNDEF members</span></span>](./jet-columndef-members.md)

[<span data-ttu-id="ad2b7-121">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ad2b7-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
