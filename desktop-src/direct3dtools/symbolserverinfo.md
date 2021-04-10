---
description: Representa información sobre el servidor de símbolos de depuración.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura SymbolServerInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152214"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span data-ttu-id="2616e-103"><span id="vspixengine.symbolserverinfo"></span>Estructura SymbolServerInfo</span><span class="sxs-lookup"><span data-stu-id="2616e-103"><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo structure</span></span>

<span data-ttu-id="2616e-104">Representa información sobre el servidor de símbolos de depuración.</span><span class="sxs-lookup"><span data-stu-id="2616e-104">Represents information about the debug symbol server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2616e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2616e-105">Syntax</span></span>


```C++
} SymbolServerInfo;
```

## <a name="members"></a><span data-ttu-id="2616e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2616e-106">Members</span></span>

<span data-ttu-id="2616e-107">**symbolPath**</span><span class="sxs-lookup"><span data-stu-id="2616e-107">**symbolPath**</span></span>  
<span data-ttu-id="2616e-108">Cadena COM que contiene la ruta de acceso del servidor de símbolos.</span><span class="sxs-lookup"><span data-stu-id="2616e-108">A COM string containing the path of the symbol server.</span></span>

<span data-ttu-id="2616e-109">**symbolCacheDir**</span><span class="sxs-lookup"><span data-stu-id="2616e-109">**symbolCacheDir**</span></span>  
<span data-ttu-id="2616e-110">Cadena COM que contiene el directorio de caché del servidor de símbolos.</span><span class="sxs-lookup"><span data-stu-id="2616e-110">A COM string containing the cache directory of the symbol server.</span></span>

<span data-ttu-id="2616e-111">**publicSymbolServerName**</span><span class="sxs-lookup"><span data-stu-id="2616e-111">**publicSymbolServerName**</span></span>  
<span data-ttu-id="2616e-112">Cadena COM que contiene el nombre público del servidor de símbolos.</span><span class="sxs-lookup"><span data-stu-id="2616e-112">A COM string containing the public name of the symbol server.</span></span>

<span data-ttu-id="2616e-113">**symbolExcludeList**</span><span class="sxs-lookup"><span data-stu-id="2616e-113">**symbolExcludeList**</span></span>  
<span data-ttu-id="2616e-114">Cadena COM que especifica la lista de símbolos que se van a excluir.</span><span class="sxs-lookup"><span data-stu-id="2616e-114">A COM string that specifies the list of symbols to exclude.</span></span>

<span data-ttu-id="2616e-115">**symbolIncludeList**</span><span class="sxs-lookup"><span data-stu-id="2616e-115">**symbolIncludeList**</span></span>  
<span data-ttu-id="2616e-116">Cadena COM que especifica la lista de símbolos que se van a incluir.</span><span class="sxs-lookup"><span data-stu-id="2616e-116">A COM string that specifies the list of symbols to include.</span></span>

<span data-ttu-id="2616e-117">**useExcludeList**</span><span class="sxs-lookup"><span data-stu-id="2616e-117">**useExcludeList**</span></span>  
<span data-ttu-id="2616e-118">True si se omite la lista de exclusión; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="2616e-118">true if the exclude list is ignored; otherwise, false.</span></span>

<span data-ttu-id="2616e-119">**useMSSymbolServer**</span><span class="sxs-lookup"><span data-stu-id="2616e-119">**useMSSymbolServer**</span></span>  
<span data-ttu-id="2616e-120">True si se usa el servidor de símbolos de Microsoft; en caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="2616e-120">true if using Microsoft symbol server; otherwise, false.</span></span>

## <a name="requirements"></a><span data-ttu-id="2616e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2616e-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="2616e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2616e-122">Header</span></span></p></td><td><span data-ttu-id="2616e-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="2616e-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



