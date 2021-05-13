---
description: Crea una nueva lista usada más recientemente (MRU).
title: Función CreateMRUListW
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
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843386"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="90ef3-103">Función CreateMRUListW</span><span class="sxs-lookup"><span data-stu-id="90ef3-103">CreateMRUListW function</span></span>

<span data-ttu-id="90ef3-104">Crea una nueva lista usada más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="90ef3-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ef3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90ef3-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="90ef3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90ef3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90ef3-107">*lpmi* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="90ef3-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90ef3-108">Tipo: **LPMRUINFO**</span><span class="sxs-lookup"><span data-stu-id="90ef3-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="90ef3-109">Puntero a una estructura [**MRUINFO que**](mruinfo.md) define la lista de MRU.</span><span class="sxs-lookup"><span data-stu-id="90ef3-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90ef3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90ef3-110">Return value</span></span>

<span data-ttu-id="90ef3-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="90ef3-111">Type: **int**</span></span>

<span data-ttu-id="90ef3-112">Devuelve un identificador a la nueva lista de MRU o 0 en caso de error.</span><span class="sxs-lookup"><span data-stu-id="90ef3-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ef3-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90ef3-113">Remarks</span></span>

<span data-ttu-id="90ef3-114">Esta función no se incluye en un encabezado o biblioteca públicos.</span><span class="sxs-lookup"><span data-stu-id="90ef3-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="90ef3-115">Se puede acceder a él a través de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o extraerse de comctl32.dll por su ordinal, que es 400 para **CreateMRUListW**.</span><span class="sxs-lookup"><span data-stu-id="90ef3-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="90ef3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90ef3-116">Requirements</span></span>



| <span data-ttu-id="90ef3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="90ef3-117">Requirement</span></span> | <span data-ttu-id="90ef3-118">Value</span><span class="sxs-lookup"><span data-stu-id="90ef3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90ef3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90ef3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="90ef3-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="90ef3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="90ef3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90ef3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="90ef3-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="90ef3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="90ef3-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="90ef3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90ef3-124"><dt>Comctl32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="90ef3-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="90ef3-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="90ef3-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="90ef3-126">**CreateMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="90ef3-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
