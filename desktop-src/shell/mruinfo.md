---
description: Contiene información que define una nueva lista de elementos usados más recientemente (MRU). Usado por CreateMRUListW.
title: Estructura MRUINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 91c0b1a2c10f4ac77afa5f8af2380b3d14ced8f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997261"
---
# <a name="mruinfo-structure"></a><span data-ttu-id="d8471-104">Estructura MRUINFO</span><span class="sxs-lookup"><span data-stu-id="d8471-104">MRUINFO structure</span></span>

<span data-ttu-id="d8471-105">Contiene información que define una nueva lista de elementos usados más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="d8471-105">Contains information that defines a new most recently used (MRU) list.</span></span> <span data-ttu-id="d8471-106">Usado por [**CreateMRUListW**](createmrulist.md).</span><span class="sxs-lookup"><span data-stu-id="d8471-106">Used by [**CreateMRUListW**](createmrulist.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8471-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8471-107">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a><span data-ttu-id="d8471-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d8471-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d8471-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d8471-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d8471-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8471-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d8471-111">Tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="d8471-111">The size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="d8471-112">**Escáner**</span><span class="sxs-lookup"><span data-stu-id="d8471-112">**uMax**</span></span>
</dt> <dd>

<span data-ttu-id="d8471-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d8471-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="d8471-114">Número máximo de entradas en la lista MRU.</span><span class="sxs-lookup"><span data-stu-id="d8471-114">The maximum number of entries in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="d8471-115">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="d8471-115">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d8471-116">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="d8471-116">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="d8471-117">Una o varias de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="d8471-117">One or more of the following flags.</span></span>

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span data-ttu-id="d8471-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ BINARIo** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="d8471-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU\_BINARY** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="d8471-119">Los datos se almacenan en el registro como datos binarios en lugar de datos de cadena.</span><span class="sxs-lookup"><span data-stu-id="d8471-119">Data is stored in the registry as binary data rather than string data.</span></span>

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span data-ttu-id="d8471-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ CACHEWRITE** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="d8471-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU\_CACHEWRITE** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="d8471-121">Escriba los cambios en la versión de MRU almacenada en el registro solo cuando se agregue un nuevo elemento o se liberen los recursos de la lista MRU de la memoria.</span><span class="sxs-lookup"><span data-stu-id="d8471-121">Write changes to the version of the MRU stored in the registry only when a new item is added or the MRU list's resources are freed from memory.</span></span> <span data-ttu-id="d8471-122">Tenga en cuenta que la versión activa de las MRU en memoria se actualiza inmediatamente en respuesta a cualquier cambio en el contenido o la ordenación.</span><span class="sxs-lookup"><span data-stu-id="d8471-122">Note that the active version of the MRU in memory is updated immediately in response to any change in contents or ordering.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d8471-123">**hKey**</span><span class="sxs-lookup"><span data-stu-id="d8471-123">**hKey**</span></span>
</dt> <dd>

<span data-ttu-id="d8471-124">Tipo: **HKEY**</span><span class="sxs-lookup"><span data-stu-id="d8471-124">Type: **HKEY**</span></span>

</dd> <dd>

<span data-ttu-id="d8471-125">Identificador de la clave abierta actualmente o uno de los siguientes valores predefinidos en los que se van a almacenar los datos de la MRU.</span><span class="sxs-lookup"><span data-stu-id="d8471-125">A handle to the currently open key, or one of the following predefined values under which to store the MRU data.</span></span>

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

<span data-ttu-id="d8471-126">**HKEY \_ Current \_ User**</span><span class="sxs-lookup"><span data-stu-id="d8471-126">**HKEY\_CURRENT\_USER**</span></span>
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

<span data-ttu-id="d8471-127">**HKEY \_ local \_ Machine**</span><span class="sxs-lookup"><span data-stu-id="d8471-127">**HKEY\_LOCAL\_MACHINE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="d8471-128">**lpszSubKey**</span><span class="sxs-lookup"><span data-stu-id="d8471-128">**lpszSubKey**</span></span>
</dt> <dd>

<span data-ttu-id="d8471-129">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="d8471-129">Type: **LPCTSTR**</span></span>

</dd> <dd>

<span data-ttu-id="d8471-130">Subclave en la que se almacenan los datos de MRU.</span><span class="sxs-lookup"><span data-stu-id="d8471-130">The subkey under which to store the MRU data.</span></span>

</dd> <dt>

<span data-ttu-id="d8471-131">**lpfnCompare**</span><span class="sxs-lookup"><span data-stu-id="d8471-131">**lpfnCompare**</span></span>
</dt> <dd>

<span data-ttu-id="d8471-132">Tipo: **[ **MRUCMPPROC**](mrucmpproc.md)**</span><span class="sxs-lookup"><span data-stu-id="d8471-132">Type: **[**MRUCMPPROC**](mrucmpproc.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d8471-133">Puntero a una función de comparación de datos opcional que se puede usar para determinar si un elemento está presente en la lista MRU.</span><span class="sxs-lookup"><span data-stu-id="d8471-133">A pointer to an optional data comparison function that can be used to determine whether an item is present in the MRU list.</span></span> <span data-ttu-id="d8471-134">Esto resulta útil cuando la lista MRU se creó con la **marca \_ binaria MRU** .</span><span class="sxs-lookup"><span data-stu-id="d8471-134">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="d8471-135">Si este miembro es **null**, se usan las funciones de comparación de cadenas estándar; en el caso de los datos binarios, se usa una comparación de memoria directa.</span><span class="sxs-lookup"><span data-stu-id="d8471-135">If this member is **NULL**, standard string comparison functions are used; for binary data, a direct memory comparison is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8471-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8471-136">Remarks</span></span>

<span data-ttu-id="d8471-137">Esta estructura no está definida en un archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="d8471-137">This structure is not defined in a header file.</span></span> <span data-ttu-id="d8471-138">Debe definirlo por sí mismo.</span><span class="sxs-lookup"><span data-stu-id="d8471-138">You must define it yourself.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8471-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8471-139">Requirements</span></span>



| <span data-ttu-id="d8471-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8471-140">Requirement</span></span> | <span data-ttu-id="d8471-141">Value</span><span class="sxs-lookup"><span data-stu-id="d8471-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d8471-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8471-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d8471-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d8471-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d8471-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8471-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d8471-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d8471-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d8471-146">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d8471-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d8471-147">**MRUINFOW** (Unicode) y **MRUINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d8471-147">**MRUINFOW** (Unicode) and **MRUINFOA** (ANSI)</span></span><br/>  |



 

 




