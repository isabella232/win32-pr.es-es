---
description: Representa información sobre un marco en la pila de llamadas.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructura CallStackFrame
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fbe527c59a64e91f46a390344ea576c7560ef1f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696074"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span data-ttu-id="30a80-103"><span id="vspixengine.callstackframe"></span>Estructura CallStackFrame</span><span class="sxs-lookup"><span data-stu-id="30a80-103"><span id="vspixengine.callstackframe"></span>CallStackFrame structure</span></span>

<span data-ttu-id="30a80-104">Representa información sobre un marco en la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="30a80-104">Represents information about a frame on the callstack.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a80-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30a80-105">Syntax</span></span>


```C++
} CallStackFrame;
```

## <a name="members"></a><span data-ttu-id="30a80-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="30a80-106">Members</span></span>

<span data-ttu-id="30a80-107">**nombrefunción**</span><span class="sxs-lookup"><span data-stu-id="30a80-107">**functionName**</span></span>  
<span data-ttu-id="30a80-108">Cadena COM que contiene el nombre de la función asociada.</span><span class="sxs-lookup"><span data-stu-id="30a80-108">A COM string containing the name of the associated function.</span></span>

<span data-ttu-id="30a80-109">**sourceFile**</span><span class="sxs-lookup"><span data-stu-id="30a80-109">**sourceFile**</span></span>  
<span data-ttu-id="30a80-110">Cadena COM que contiene la ruta de acceso del archivo de código fuente asociado.</span><span class="sxs-lookup"><span data-stu-id="30a80-110">A COM string containing the filepath of the associated source file.</span></span>

<span data-ttu-id="30a80-111">**moduleName**</span><span class="sxs-lookup"><span data-stu-id="30a80-111">**moduleName**</span></span>  
<span data-ttu-id="30a80-112">Cadena COM que contiene el nombre del módulo de código asociado.</span><span class="sxs-lookup"><span data-stu-id="30a80-112">A COM string containing the name of the associated code module.</span></span>

<span data-ttu-id="30a80-113">**lineNumber**</span><span class="sxs-lookup"><span data-stu-id="30a80-113">**lineNumber**</span></span>  
<span data-ttu-id="30a80-114">Número de línea asociado.</span><span class="sxs-lookup"><span data-stu-id="30a80-114">The associated line number.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a80-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30a80-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="30a80-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30a80-116">Header</span></span></p></td><td><span data-ttu-id="30a80-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="30a80-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



