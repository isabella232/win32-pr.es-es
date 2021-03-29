---
description: Representa información sobre una única entrada en el diseño de búfer de una malla.
MS-HAID: vspixengine.MeshDataBufferLayoutEntry
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura MeshDataBufferLayoutEntry
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FE1D796C-DFD8-4C6E-9914-3063408FE565
api_name:
- MeshDataBufferLayoutEntry
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bce67b8316e9eb9b96e641e2a90260fab6bfdaad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806830"
---
# <a name="span-idvspixenginemeshdatabufferlayoutentryspanmeshdatabufferlayoutentry-structure"></a><span data-ttu-id="c7700-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>Estructura MeshDataBufferLayoutEntry</span><span class="sxs-lookup"><span data-stu-id="c7700-103"><span id="vspixengine.meshdatabufferlayoutentry"></span>MeshDataBufferLayoutEntry structure</span></span>

<span data-ttu-id="c7700-104">Representa información sobre una única entrada en el diseño de búfer de una malla.</span><span class="sxs-lookup"><span data-stu-id="c7700-104">Represents information about a single entry in the buffer layout of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7700-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7700-105">Syntax</span></span>


```C++
} MeshDataBufferLayoutEntry;
```

## <a name="members"></a><span data-ttu-id="c7700-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c7700-106">Members</span></span>

<span data-ttu-id="c7700-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="c7700-107">**pName**</span></span>  
<span data-ttu-id="c7700-108">Cadena COM que contiene el nombre de la entrada.</span><span class="sxs-lookup"><span data-stu-id="c7700-108">A COM string containing the name of the entry.</span></span>

<span data-ttu-id="c7700-109">**numComponents**</span><span class="sxs-lookup"><span data-stu-id="c7700-109">**numComponents**</span></span>  
<span data-ttu-id="c7700-110">El número de componentes homogéneos (valores) que componen esta entrada.</span><span class="sxs-lookup"><span data-stu-id="c7700-110">The number of homogenous components (values) that make up this entry.</span></span>

<span data-ttu-id="c7700-111">**isPosition**</span><span class="sxs-lookup"><span data-stu-id="c7700-111">**isPosition**</span></span>  
<span data-ttu-id="c7700-112">True si la entrada es una posición; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="c7700-112">true if the entry is a position; otherwise, false.</span></span>

<span data-ttu-id="c7700-113">**format**</span><span class="sxs-lookup"><span data-stu-id="c7700-113">**format**</span></span>  
<span data-ttu-id="c7700-114">El formato de datos de la entrada (registro).</span><span class="sxs-lookup"><span data-stu-id="c7700-114">The data format of the entry (register).</span></span> <span data-ttu-id="c7700-115">Para obtener más información, consulte la \_ enumeración de formato de registro.</span><span class="sxs-lookup"><span data-stu-id="c7700-115">For more information, see the REGISTER\_FORMAT enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7700-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7700-116">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c7700-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7700-117">Header</span></span></p></td><td><span data-ttu-id="c7700-118">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c7700-118">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



