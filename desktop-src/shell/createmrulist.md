---
description: Crea una nueva lista de elementos usados más recientemente (MRU).
title: CreateMRUListW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 572e52f1461e3d48ab9eba1aa903c7fb690636d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808834"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="1841d-103">CreateMRUListW función)</span><span class="sxs-lookup"><span data-stu-id="1841d-103">CreateMRUListW function</span></span>

<span data-ttu-id="1841d-104">Crea una nueva lista de elementos usados más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="1841d-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1841d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1841d-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="1841d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1841d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1841d-107">*LPMI* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1841d-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1841d-108">Tipo: **LPMRUINFO**</span><span class="sxs-lookup"><span data-stu-id="1841d-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="1841d-109">Puntero a una estructura [**MRUINFO**](mruinfo.md) que define la lista MRU.</span><span class="sxs-lookup"><span data-stu-id="1841d-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1841d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1841d-110">Return value</span></span>

<span data-ttu-id="1841d-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="1841d-111">Type: **int**</span></span>

<span data-ttu-id="1841d-112">Devuelve un identificador para la nueva lista MRU o 0 en caso de error.</span><span class="sxs-lookup"><span data-stu-id="1841d-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="1841d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1841d-113">Remarks</span></span>

<span data-ttu-id="1841d-114">Esta función no está incluida en un encabezado público o una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="1841d-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="1841d-115">Se puede tener acceso a ella a través de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o extraer de comctl32.dll por su ordinal, que es 400 para **CreateMRUListW**.</span><span class="sxs-lookup"><span data-stu-id="1841d-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1841d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1841d-116">Requirements</span></span>



| <span data-ttu-id="1841d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1841d-117">Requirement</span></span> | <span data-ttu-id="1841d-118">Value</span><span class="sxs-lookup"><span data-stu-id="1841d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1841d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1841d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1841d-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1841d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1841d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1841d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1841d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1841d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1841d-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1841d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1841d-124"><dt>Comctl32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1841d-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="1841d-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="1841d-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1841d-126">**CreateMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="1841d-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
