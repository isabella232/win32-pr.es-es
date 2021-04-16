---
description: Recupera información acerca de la clave del registro especificada en un subárbol del registro sin conexión.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: Función ORQueryInfoKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671276"
---
# <a name="orqueryinfokey-function"></a><span data-ttu-id="dfa54-103">ORQueryInfoKey función)</span><span class="sxs-lookup"><span data-stu-id="dfa54-103">ORQueryInfoKey function</span></span>

<span data-ttu-id="dfa54-104">Recupera información acerca de la clave del registro especificada en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="dfa54-104">Retrieves information about the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa54-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfa54-105">Syntax</span></span>


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="dfa54-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dfa54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa54-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="dfa54-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa54-108">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="dfa54-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="dfa54-109">*lpClass* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfa54-109">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa54-110">Un puntero a un búfer que recibe la clase clave.</span><span class="sxs-lookup"><span data-stu-id="dfa54-110">A pointer to a buffer that receives the key class.</span></span> <span data-ttu-id="dfa54-111">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfa54-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfa54-112">*lpcClass* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfa54-112">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa54-113">Puntero a una variable que especifica el tamaño del búfer al que apunta el parámetro *lpClass* , en caracteres.</span><span class="sxs-lookup"><span data-stu-id="dfa54-113">A pointer to a variable that specifies the size of the buffer pointed to by the *lpClass* parameter, in characters.</span></span>

<span data-ttu-id="dfa54-114">El tamaño debe incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="dfa54-114">The size should include the terminating null character.</span></span> <span data-ttu-id="dfa54-115">Cuando la función devuelve, esta variable contiene el tamaño de la cadena de clase que se almacena en el búfer.</span><span class="sxs-lookup"><span data-stu-id="dfa54-115">When the function returns, this variable contains the size of the class string that is stored in the buffer.</span></span> <span data-ttu-id="dfa54-116">El recuento devuelto no incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="dfa54-116">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="dfa54-117">Si el búfer no es suficientemente grande, la función devuelve un ERROR \_ más \_ datos y la variable contiene el tamaño de la cadena, en caracteres, sin contar el carácter null de terminación.</span><span class="sxs-lookup"><span data-stu-id="dfa54-117">If the buffer is not big enough, the function returns ERROR\_MORE\_DATA, and the variable contains the size of the string, in characters, without counting the terminating null character.</span></span>

<span data-ttu-id="dfa54-118">Si *lpClass* es **null**, *lpcClass* puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="dfa54-118">If *lpClass* is **NULL**, *lpcClass* can be **NULL**.</span></span>

<span data-ttu-id="dfa54-119">Si el parámetro *lpClass* es una dirección válida, pero el parámetro *lpcClass* no es (por ejemplo, si el parámetro *lpcClass* es **null**), la función devuelve un parámetro de error \_ no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="dfa54-119">If the *lpClass* parameter is a valid address, but the *lpcClass* parameter is not (for example, if the *lpcClass* parameter is **NULL**) then the function returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="dfa54-120">*lpcSubKeys* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfa54-120">*lpcSubKeys* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa54-121">Puntero a una variable que recibe el número de subclaves que contiene la clave especificada.</span><span class="sxs-lookup"><span data-stu-id="dfa54-121">A pointer to a variable that receives the number of subkeys that are contained by the specified key.</span></span> <span data-ttu-id="dfa54-122">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfa54-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfa54-123">*lpcMaxSubKeyLen* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfa54-123">*lpcMaxSubKeyLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa54-124">Puntero a una variable que recibe el tamaño de la subclave de la clave con el nombre más largo, en caracteres Unicode, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="dfa54-124">A pointer to a variable that receives the size of the key's subkey with the longest name, in Unicode characters, not including the terminating null character.</span></span> <span data-ttu-id="dfa54-125">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfa54-125">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfa54-126">*lpcMaxClassLen* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfa54-126">*lpcMaxClassLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa54-127">Puntero a una variable que recibe el tamaño de la cadena más larga que especifica una clase de subclave, en caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="dfa54-127">A pointer to a variable that receives the size of the longest string that specifies a subkey class, in Unicode characters.</span></span> <span data-ttu-id="dfa54-128">El recuento devuelto no incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="dfa54-128">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="dfa54-129">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfa54-129">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfa54-130">*lpcValues* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfa54-130">*lpcValues* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa54-131">Puntero a una variable que recibe el número de valores que están asociados a la clave.</span><span class="sxs-lookup"><span data-stu-id="dfa54-131">A pointer to a variable that receives the number of values that are associated with the key.</span></span> <span data-ttu-id="dfa54-132">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfa54-132">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfa54-133">*lpcMaxValueNameLen* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfa54-133">*lpcMaxValueNameLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa54-134">Puntero a una variable que recibe el tamaño del nombre del valor más largo de la clave, en caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="dfa54-134">A pointer to a variable that receives the size of the key's longest value name, in Unicode characters.</span></span> <span data-ttu-id="dfa54-135">El tamaño no incluye el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="dfa54-135">The size does not include the terminating null character.</span></span> <span data-ttu-id="dfa54-136">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfa54-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfa54-137">*lpcMaxValueLen* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfa54-137">*lpcMaxValueLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa54-138">Puntero a una variable que recibe el tamaño del componente de datos más largo entre los valores de la clave, en bytes.</span><span class="sxs-lookup"><span data-stu-id="dfa54-138">A pointer to a variable that receives the size of the longest data component among the key's values, in bytes.</span></span> <span data-ttu-id="dfa54-139">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfa54-139">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfa54-140">*lpcbSecurityDescriptor* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfa54-140">*lpcbSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa54-141">Puntero a una variable que recibe el tamaño del descriptor de seguridad de la clave, en bytes.</span><span class="sxs-lookup"><span data-stu-id="dfa54-141">A pointer to a variable that receives the size of the key's security descriptor, in bytes.</span></span> <span data-ttu-id="dfa54-142">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfa54-142">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfa54-143">*lpftLastWriteTime* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dfa54-143">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa54-144">Puntero a una estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que recibe la hora de la última escritura.</span><span class="sxs-lookup"><span data-stu-id="dfa54-144">A pointer to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the last write time.</span></span> <span data-ttu-id="dfa54-145">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfa54-145">This parameter can be **NULL**.</span></span>

<span data-ttu-id="dfa54-146">La función establece los miembros de la estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para indicar la última vez que se modifica la clave o cualquiera de sus entradas de valor.</span><span class="sxs-lookup"><span data-stu-id="dfa54-146">The function sets the members of the [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to indicate the last time that the key or any of its value entries is modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa54-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfa54-147">Return value</span></span>

<span data-ttu-id="dfa54-148">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="dfa54-148">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="dfa54-149">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="dfa54-149">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="dfa54-150">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="dfa54-150">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="dfa54-151">Si el búfer de *lpClass* es demasiado pequeño para recibir el nombre de la clase, la función devuelve los datos de error \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="dfa54-151">If the *lpClass* buffer is too small to receive the name of the class, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa54-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfa54-152">Requirements</span></span>



| <span data-ttu-id="dfa54-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfa54-153">Requirement</span></span> | <span data-ttu-id="dfa54-154">Value</span><span class="sxs-lookup"><span data-stu-id="dfa54-154">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa54-155">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="dfa54-155">Redistributable</span></span><br/> | <span data-ttu-id="dfa54-156">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="dfa54-156">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="dfa54-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dfa54-157">Header</span></span><br/>          | <dl> <span data-ttu-id="dfa54-158"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa54-158"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfa54-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dfa54-159">DLL</span></span><br/>             | <dl> <span data-ttu-id="dfa54-160"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfa54-160"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfa54-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfa54-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa54-162">FILETIME</span><span class="sxs-lookup"><span data-stu-id="dfa54-162">FILETIME</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="dfa54-163">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="dfa54-163">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="dfa54-164">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="dfa54-164">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="dfa54-165">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="dfa54-165">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> </dl>

 

 
