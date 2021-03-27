---
description: Convierte una cadena en un GUID.
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: GUIDFromString (función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909557"
---
# <a name="guidfromstring-function"></a><span data-ttu-id="b2a5d-103">GUIDFromString (función)</span><span class="sxs-lookup"><span data-stu-id="b2a5d-103">GUIDFromString function</span></span>

<span data-ttu-id="b2a5d-104">\[**GUIDFromString** está disponible a través de Windows XP con Service Pack 2 (SP2) o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-104">\[**GUIDFromString** is available through Windows XP with Service Pack 2 (SP2) or Windows Vista.</span></span> <span data-ttu-id="b2a5d-105">Podría modificarse o no estar disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-105">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="b2a5d-106">Las aplicaciones deben usar [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) o [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) en lugar de esta función.\]</span><span class="sxs-lookup"><span data-stu-id="b2a5d-106">Applications should use [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) or [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) in place of this function.\]</span></span>

<span data-ttu-id="b2a5d-107">Convierte una cadena en un GUID.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-107">Converts a string to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2a5d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2a5d-108">Syntax</span></span>


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a><span data-ttu-id="b2a5d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2a5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2a5d-110">*PSZ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2a5d-110">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2a5d-111">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="b2a5d-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="b2a5d-112">Puntero a la cadena terminada en null que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-112">A pointer to the null-terminated string to convert.</span></span> <span data-ttu-id="b2a5d-113">La cadena debe tener el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="b2a5d-113">The string should be in the following form:</span></span>

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

<span data-ttu-id="b2a5d-114">*pguid* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b2a5d-114">*pguid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2a5d-115">Tipo: **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="b2a5d-115">Type: **LPGUID**</span></span>

<span data-ttu-id="b2a5d-116">Puntero a un búfer para recibir el GUID cuando este método devuelve.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-116">Pointer to a buffer to receive the GUID when this method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2a5d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2a5d-117">Return value</span></span>

<span data-ttu-id="b2a5d-118">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="b2a5d-118">Type: **BOOL**</span></span>

<span data-ttu-id="b2a5d-119">**True** si el GUID se creó correctamente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-119">**TRUE** if the GUID was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2a5d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2a5d-120">Remarks</span></span>

<span data-ttu-id="b2a5d-121">Esta función no está declarada en un encabezado o exportada por el nombre de un archivo. dll.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-121">This function is not declared in a header or exported by name from a .dll file.</span></span> <span data-ttu-id="b2a5d-122">Se debe cargar desde Shell32.dll como ordinal 703 para **GUIDFromStringA** y el ordinal 704 para **GUIDFromStringW**.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-122">It must be loaded from Shell32.dll as ordinal 703 for **GUIDFromStringA** and ordinal 704 for **GUIDFromStringW**.</span></span>

<span data-ttu-id="b2a5d-123">También se puede acceder a él desde Shlwapi.dll como ordinal 269 para **GUIDFromStringA** y el ordinal 270 para **GUIDFromStringW**.</span><span class="sxs-lookup"><span data-stu-id="b2a5d-123">It can also be accessed from Shlwapi.dll as ordinal 269 for **GUIDFromStringA** and ordinal 270 for **GUIDFromStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2a5d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2a5d-124">Requirements</span></span>



| <span data-ttu-id="b2a5d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2a5d-125">Requirement</span></span> | <span data-ttu-id="b2a5d-126">Value</span><span class="sxs-lookup"><span data-stu-id="b2a5d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a5d-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2a5d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b2a5d-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b2a5d-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b2a5d-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2a5d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b2a5d-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b2a5d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b2a5d-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2a5d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2a5d-132"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2a5d-132"><dt>Shell32.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2a5d-133">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="b2a5d-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b2a5d-134">**GUIDFromStringW** (Unicode) y **GUIDFromStringA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b2a5d-134">**GUIDFromStringW** (Unicode) and **GUIDFromStringA** (ANSI)</span></span><br/>                |



 

 
