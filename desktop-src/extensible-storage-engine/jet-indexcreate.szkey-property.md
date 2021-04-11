---
description: 'Más información acerca de: propiedad JET_INDEXCREATE. szKey'
title: Propiedad JET_INDEXCREATE. szKey
TOCTitle: 'szKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.szkey(v=EXCHG.10)
ms:contentKeyID: 55103656
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86ade65ee28eef6314d31653772b0c22657476d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361359"
---
# <a name="jet_indexcreateszkey-property"></a><span data-ttu-id="de779-103">Propiedad JET_INDEXCREATE. szKey</span><span class="sxs-lookup"><span data-stu-id="de779-103">JET_INDEXCREATE.szKey property</span></span>

<span data-ttu-id="de779-104">Obtiene o establece la descripción de la clave de índice.</span><span class="sxs-lookup"><span data-stu-id="de779-104">Gets or sets the description of the index key.</span></span> <span data-ttu-id="de779-105">Se trata de una cadena doble terminada en NULL de tokens delimitados por null.</span><span class="sxs-lookup"><span data-stu-id="de779-105">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="de779-106">Cada token tiene el formato \[ Direction-Specifier \] \[ Column-name \] , donde Direction-Specification es "+" o "-".</span><span class="sxs-lookup"><span data-stu-id="de779-106">Each token is of the form \[direction-specifier\]\[column-name\], where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="de779-107">por ejemplo, un szKey de "+ ABC \\ 0-Def \\ 0 + GHI \\ 0" indexará las tres columnas "ABC" (en orden ascendente), "def" (en orden descendente) y "GHI" (en orden ascendente).</span><span class="sxs-lookup"><span data-stu-id="de779-107">for example, a szKey of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span>

<span data-ttu-id="de779-108">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="de779-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="de779-109">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="de779-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="de779-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de779-110">Syntax</span></span>

``` vb
'Declaration
Public Property szKey As String
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As String

value = instance.szKey

instance.szKey = value
```

``` csharp
public string szKey { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="de779-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="de779-111">Property value</span></span>

<span data-ttu-id="de779-112">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="de779-112">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="de779-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="de779-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="de779-114">Referencia</span><span class="sxs-lookup"><span data-stu-id="de779-114">Reference</span></span>

[<span data-ttu-id="de779-115">JET_INDEXCREATE (clase)</span><span class="sxs-lookup"><span data-stu-id="de779-115">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="de779-116">Miembros de JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="de779-116">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="de779-117">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="de779-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
