---
description: Enumera el contenido de la lista de elementos usados más recientemente (MRU). Opcionalmente, recupera un elemento de la enumeración.
title: EnumMRUListW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912366"
---
# <a name="enummrulistw-function"></a><span data-ttu-id="4b66a-104">EnumMRUListW función)</span><span class="sxs-lookup"><span data-stu-id="4b66a-104">EnumMRUListW function</span></span>

<span data-ttu-id="4b66a-105">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4b66a-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="4b66a-106">Podría modificarse o no estar disponible en versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="4b66a-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="4b66a-107">\]</span><span class="sxs-lookup"><span data-stu-id="4b66a-107">\]</span></span>

<span data-ttu-id="4b66a-108">Enumera el contenido de la lista de elementos usados más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="4b66a-108">Enumerates the contents of the most recently used (MRU) list.</span></span> <span data-ttu-id="4b66a-109">Opcionalmente, recupera un elemento de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="4b66a-109">Optionally retrieves an item from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b66a-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b66a-110">Syntax</span></span>


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a><span data-ttu-id="4b66a-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b66a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b66a-112">*hMRU* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b66a-112">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b66a-113">Tipo: **Handle**</span><span class="sxs-lookup"><span data-stu-id="4b66a-113">Type: **HANDLE**</span></span>

<span data-ttu-id="4b66a-114">Identificador de la lista MRU, obtenida cuando se creó la lista.</span><span class="sxs-lookup"><span data-stu-id="4b66a-114">The handle of the MRU list, obtained when the list was created.</span></span>

</dd> <dt>

<span data-ttu-id="4b66a-115">*nItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b66a-115">*nItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b66a-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="4b66a-116">Type: **int**</span></span>

<span data-ttu-id="4b66a-117">Elemento que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="4b66a-117">The item to return.</span></span> <span data-ttu-id="4b66a-118">Si este valor es menor que 0, la función devuelve el número de elementos de la lista MRU.</span><span class="sxs-lookup"><span data-stu-id="4b66a-118">If this value is less than 0, the function returns the number of items in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="4b66a-119">*lpData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4b66a-119">*lpData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b66a-120">Tipo: \**void \** _</span><span class="sxs-lookup"><span data-stu-id="4b66a-120">Type: \**void\** _</span></span>

<span data-ttu-id="4b66a-121">Un puntero a un búfer que recibe el elemento solicitado en _nItem \*.</span><span class="sxs-lookup"><span data-stu-id="4b66a-121">A pointer to a buffer that receives the item requested in _nItem\*.</span></span> <span data-ttu-id="4b66a-122">Si *nItem* es menor que 0, el contenido de este búfer no cambia.</span><span class="sxs-lookup"><span data-stu-id="4b66a-122">If *nItem* is less than 0, the contents of this buffer are unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="4b66a-123">*uLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b66a-123">*uLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b66a-124">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="4b66a-124">Type: **UINT**</span></span>

<span data-ttu-id="4b66a-125">Tamaño del búfer, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="4b66a-125">The size of the buffer, including the terminating null character.</span></span> <span data-ttu-id="4b66a-126">Si la lista MRU se creó con la **marca \_ binaria MRU** , este es el tamaño en bytes.</span><span class="sxs-lookup"><span data-stu-id="4b66a-126">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="4b66a-127">De lo contrario, es el tamaño en caracteres.</span><span class="sxs-lookup"><span data-stu-id="4b66a-127">Otherwise, it is the size in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b66a-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b66a-128">Return value</span></span>

<span data-ttu-id="4b66a-129">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="4b66a-129">Type: **int**</span></span>

<span data-ttu-id="4b66a-130">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4b66a-130">Returns one of the following values.</span></span>

-   <span data-ttu-id="4b66a-131">Devuelve el número de elementos de la enumeración, si *nItem* es menor que 0.</span><span class="sxs-lookup"><span data-stu-id="4b66a-131">Returns the number of items in the enumeration, if *nItem* is less than 0.</span></span>
-   <span data-ttu-id="4b66a-132">Devuelve-1 si se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="4b66a-132">Returns -1 if an error occurred.</span></span>
-   <span data-ttu-id="4b66a-133">De lo contrario, devuelve el tamaño de la cadena devuelta en *lpData*, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="4b66a-133">Otherwise, returns the size of the string returned in *lpData*, including the terminating null character.</span></span> <span data-ttu-id="4b66a-134">Si la lista MRU se creó con la **marca \_ binaria MRU** , este es el tamaño en bytes.</span><span class="sxs-lookup"><span data-stu-id="4b66a-134">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="4b66a-135">De lo contrario, es el tamaño en caracteres.</span><span class="sxs-lookup"><span data-stu-id="4b66a-135">Otherwise, it is the size in characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b66a-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b66a-136">Remarks</span></span>

<span data-ttu-id="4b66a-137">Esta función no está incluida en un encabezado público o una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="4b66a-137">This function is not included in a public header or library.</span></span> <span data-ttu-id="4b66a-138">Se puede tener acceso a ella a través de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) o extraer de comctl32.dll por su ordinal, que es 403 para **EnumMRUListW**.</span><span class="sxs-lookup"><span data-stu-id="4b66a-138">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 403 for **EnumMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b66a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b66a-139">Requirements</span></span>



| <span data-ttu-id="4b66a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b66a-140">Requirement</span></span> | <span data-ttu-id="4b66a-141">Value</span><span class="sxs-lookup"><span data-stu-id="4b66a-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b66a-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b66a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4b66a-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4b66a-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4b66a-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b66a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4b66a-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b66a-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4b66a-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b66a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b66a-147"><dt>Comctl32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4b66a-147"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="4b66a-148">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="4b66a-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4b66a-149">**EnumMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="4b66a-149">**EnumMRUListW** (Unicode)</span></span><br/>                                                                          |



## <a name="see-also"></a><span data-ttu-id="4b66a-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b66a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b66a-151">**CreateMRUListW**</span><span class="sxs-lookup"><span data-stu-id="4b66a-151">**CreateMRUListW**</span></span>](createmrulist.md)
</dt> <dt>

[<span data-ttu-id="4b66a-152">**MRUINFO**</span><span class="sxs-lookup"><span data-stu-id="4b66a-152">**MRUINFO**</span></span>](mruinfo.md)
</dt> </dl>

 

 
