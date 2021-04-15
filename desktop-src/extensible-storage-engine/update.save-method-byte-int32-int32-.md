---
description: 'Más información sobre: método Update. Save (byte, Int32, Int32)'
title: Método Update. Save (byte, Int32, Int32)
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2c798f22039ced1bab30ecaa9c3f650079be0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497620"
---
# <a name="updatesave-method-byte--int32-int32"></a><span data-ttu-id="5420d-103">Método Update. Save (byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="5420d-103">Update.Save method (Byte , Int32, Int32)</span></span>

<span data-ttu-id="5420d-104">Actualice el ID. de la.</span><span class="sxs-lookup"><span data-stu-id="5420d-104">Update the tableid.</span></span>

<span data-ttu-id="5420d-105">**Espacio de nombres:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5420d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5420d-106">**Ensamblado:**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5420d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5420d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5420d-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="5420d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5420d-108">Parameters</span></span>

  - <span data-ttu-id="5420d-109">marcador</span><span class="sxs-lookup"><span data-stu-id="5420d-109">bookmark</span></span>  
    <span data-ttu-id="5420d-110">Automáticamente \[\]</span><span class="sxs-lookup"><span data-stu-id="5420d-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="5420d-111">Devuelve el marcador del registro actualizado.</span><span class="sxs-lookup"><span data-stu-id="5420d-111">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="5420d-112">Puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="5420d-112">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="5420d-113">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="5420d-113">bookmarkSize</span></span>  
    <span data-ttu-id="5420d-114">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5420d-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5420d-115">Tamaño del búfer del marcador.</span><span class="sxs-lookup"><span data-stu-id="5420d-115">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="5420d-116">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="5420d-116">actualBookmarkSize</span></span>  
    <span data-ttu-id="5420d-117">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5420d-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="5420d-118">Devuelve el tamaño real del marcador.</span><span class="sxs-lookup"><span data-stu-id="5420d-118">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="5420d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5420d-119">Remarks</span></span>

<span data-ttu-id="5420d-120">Guardar es el último paso para realizar una inserción o una actualización.</span><span class="sxs-lookup"><span data-stu-id="5420d-120">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="5420d-121">La actualización se inicia llamando a crear un objeto Update y llamando a JetSetColumn o JetSetColumns una o varias veces para establecer el estado del registro.</span><span class="sxs-lookup"><span data-stu-id="5420d-121">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="5420d-122">Por último, se llama a Update para completar la operación de actualización.</span><span class="sxs-lookup"><span data-stu-id="5420d-122">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="5420d-123">Los índices solo se actualizan mediante Update o y no durante JetSetColumn ni JetSetColumns.</span><span class="sxs-lookup"><span data-stu-id="5420d-123">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="5420d-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5420d-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5420d-125">Referencia</span><span class="sxs-lookup"><span data-stu-id="5420d-125">Reference</span></span>

[<span data-ttu-id="5420d-126">Update (clase)</span><span class="sxs-lookup"><span data-stu-id="5420d-126">Update class</span></span>](./update-class.md)

[<span data-ttu-id="5420d-127">Actualizar miembros</span><span class="sxs-lookup"><span data-stu-id="5420d-127">Update members</span></span>](./update-members.md)

[<span data-ttu-id="5420d-128">Guardar sobrecarga</span><span class="sxs-lookup"><span data-stu-id="5420d-128">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="5420d-129">Espacio de nombres Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5420d-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
