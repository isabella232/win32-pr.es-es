---
description: 'Más información acerca de: estructura de JET_ERRINFOBASIC_W'
title: Estructura de JET_ERRINFOBASIC_W
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104003996"
---
# <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="710ed-103">Estructura de JET_ERRINFOBASIC_W</span><span class="sxs-lookup"><span data-stu-id="710ed-103">JET_ERRINFOBASIC_W Structure</span></span>


<span data-ttu-id="710ed-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="710ed-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="710ed-105">Estructura de JET_ERRINFOBASIC_W</span><span class="sxs-lookup"><span data-stu-id="710ed-105">JET_ERRINFOBASIC_W Structure</span></span>

<span data-ttu-id="710ed-106">La estructura **JET_ERRINFOBASIC_W** define los datos que se devuelven desde el método [JetGetErrorInfo ()](./jetgeterrorinfow-function.md) cuando se pasa el JET_ErrorInfoSpecificErr InfoLevel.</span><span class="sxs-lookup"><span data-stu-id="710ed-106">The **JET_ERRINFOBASIC_W** structure defines the data that is returned from the [JetGetErrorInfo()](./jetgeterrorinfow-function.md) method when the JET_ErrorInfoSpecificErr InfoLevel is passed in.</span></span>

<span data-ttu-id="710ed-107">Nota: esta documentación se basa en una versión preliminar del motor de almacenamiento extensible.</span><span class="sxs-lookup"><span data-stu-id="710ed-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="710ed-108">Esta información está sujeta a cambios.</span><span class="sxs-lookup"><span data-stu-id="710ed-108">This information is subject to change.</span></span>

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a><span data-ttu-id="710ed-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="710ed-109">Members</span></span>

<span data-ttu-id="710ed-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="710ed-110">**cbStruct**</span></span>

<span data-ttu-id="710ed-111">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="710ed-111">The size of the structure, in bytes.</span></span> <span data-ttu-id="710ed-112">Debe establecerse en sizeof (JET_ERRINFOBASIC).</span><span class="sxs-lookup"><span data-stu-id="710ed-112">It must be set to sizeof( JET_ERRINFOBASIC ).</span></span>

<span data-ttu-id="710ed-113">**errValue**</span><span class="sxs-lookup"><span data-stu-id="710ed-113">**errValue**</span></span>

<span data-ttu-id="710ed-114">Valor de error que se evaluó, tal y como se pasa para el argumento *pvResult* a [JetGetErrorInfo ()](./jetgeterrorinfow-function.md).</span><span class="sxs-lookup"><span data-stu-id="710ed-114">The error value that was evaluated, as passed in for the *pvResult* argument to [JetGetErrorInfo()](./jetgeterrorinfow-function.md).</span></span>

<span data-ttu-id="710ed-115">**errcatMostSpecific**</span><span class="sxs-lookup"><span data-stu-id="710ed-115">**errcatMostSpecific**</span></span>

<span data-ttu-id="710ed-116">[JET_ERRCAT](./jet-errcat.md) constante de nivel inferior que está asociada al error; es decir, la categoría de nivel de hoja de la jerarquía de categoría documentada en [JET_ERRCAT](./jet-errcat.md).</span><span class="sxs-lookup"><span data-stu-id="710ed-116">The lowest-level [JET_ERRCAT](./jet-errcat.md) constant that is associated with the error; that is, the leaf-level category in the category hierarchy documented in [JET_ERRCAT](./jet-errcat.md).</span></span>

<span data-ttu-id="710ed-117">**rgCategoricalHierarchy \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="710ed-117">**rgCategoricalHierarchy\[8\]**</span></span>

<span data-ttu-id="710ed-118">La jerarquía de categorías de error que está asociada al error.</span><span class="sxs-lookup"><span data-stu-id="710ed-118">The hierarchy of error categories that is associated with the error.</span></span> <span data-ttu-id="710ed-119">La posición 0 es el nivel más alto en la jerarquía de [JET_ERRCAT](./jet-errcat.md)y el resto son subcategorías hasta que se establece la categoría más específica, después de la cual se JET_errcatUnknownn todas las categorías.</span><span class="sxs-lookup"><span data-stu-id="710ed-119">Position 0 is the highest level in the hierarchy of [JET_ERRCAT](./jet-errcat.md), and the rest are subcategories until the most specific category is set, after which all categories are JET_errcatUnknown.</span></span>

<span data-ttu-id="710ed-120">**lSourceLine**</span><span class="sxs-lookup"><span data-stu-id="710ed-120">**lSourceLine**</span></span>

<span data-ttu-id="710ed-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="710ed-121">Reserved.</span></span>

<span data-ttu-id="710ed-122">**rgszSourceFile \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="710ed-122">**rgszSourceFile\[64\]**</span></span>

<span data-ttu-id="710ed-123">Reservado.</span><span class="sxs-lookup"><span data-stu-id="710ed-123">Reserved.</span></span>

### <a name="requirements"></a><span data-ttu-id="710ed-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="710ed-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="710ed-125"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="710ed-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="710ed-126">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="710ed-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="710ed-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="710ed-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="710ed-128">Requiere Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="710ed-128">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="710ed-129"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="710ed-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="710ed-130">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="710ed-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>
