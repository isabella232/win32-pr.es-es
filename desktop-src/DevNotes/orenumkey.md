---
description: Enumera las subclaves de la clave del registro abierta especificada en un subárbol del registro sin conexión. La función recupera información sobre una subclave cada vez que se llama.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Función OREnumKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649982"
---
# <a name="orenumkey-function"></a><span data-ttu-id="f74b1-104">OREnumKey función)</span><span class="sxs-lookup"><span data-stu-id="f74b1-104">OREnumKey function</span></span>

<span data-ttu-id="f74b1-105">Enumera las subclaves de la clave del registro abierta especificada en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f74b1-105">Enumerates the subkeys of the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="f74b1-106">La función recupera información sobre una subclave cada vez que se llama.</span><span class="sxs-lookup"><span data-stu-id="f74b1-106">The function retrieves information about one subkey each time it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="f74b1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f74b1-107">Syntax</span></span>


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="f74b1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f74b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f74b1-109">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f74b1-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f74b1-110">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f74b1-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="f74b1-111">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f74b1-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f74b1-112">Índice de la subclave que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="f74b1-112">The index of the subkey to retrieve.</span></span> <span data-ttu-id="f74b1-113">Este parámetro debe ser cero para la primera llamada a la función y, a continuación, incrementarse en las llamadas posteriores.</span><span class="sxs-lookup"><span data-stu-id="f74b1-113">This parameter should be zero for the first call to the function and then incremented for subsequent calls.</span></span>

<span data-ttu-id="f74b1-114">Dado que las subclaves no están ordenadas, cualquier subclave nueva tendrá un índice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f74b1-114">Because subkeys are not ordered, any new subkey will have an arbitrary index.</span></span> <span data-ttu-id="f74b1-115">Esto significa que la función puede devolver subclaves en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="f74b1-115">This means that the function may return subkeys in any order.</span></span>

</dd> <dt>

<span data-ttu-id="f74b1-116">*lpName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f74b1-116">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f74b1-117">Un puntero a un búfer que recibe el nombre de la subclave, incluido el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="f74b1-117">A pointer to a buffer that receives the name of the subkey, including the terminating null character.</span></span> <span data-ttu-id="f74b1-118">La función copia solo el nombre de la subclave, no la jerarquía de claves completa, en el búfer.</span><span class="sxs-lookup"><span data-stu-id="f74b1-118">The function copies only the name of the subkey, not the full key hierarchy, to the buffer.</span></span> <span data-ttu-id="f74b1-119">Si se produce un error en la función, no se copia ninguna información en este búfer.</span><span class="sxs-lookup"><span data-stu-id="f74b1-119">If the function fails, no information is copied to this buffer.</span></span>

<span data-ttu-id="f74b1-120">Para obtener más información, vea [límites de tamaño de elementos del registro](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="f74b1-120">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="f74b1-121">*lpcName* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f74b1-121">*lpcName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f74b1-122">Puntero a una variable que especifica el tamaño del búfer especificado por el parámetro *lpName* en **WCHARs**.</span><span class="sxs-lookup"><span data-stu-id="f74b1-122">A pointer to a variable that specifies the size of the buffer specified by the *lpName* parameter, in **WCHARs**.</span></span> <span data-ttu-id="f74b1-123">Este tamaño debe incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="f74b1-123">This size should include the terminating null character.</span></span> <span data-ttu-id="f74b1-124">Si la función se ejecuta correctamente, la variable a la que apunta *lpcName* contiene el número de caracteres almacenados en el búfer, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="f74b1-124">If the function succeeds, the variable pointed to by *lpcName* contains the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="f74b1-125">*lpClass* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f74b1-125">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f74b1-126">Un puntero a un búfer que recibe la cadena de clase terminada en NULL de la subclave enumerada.</span><span class="sxs-lookup"><span data-stu-id="f74b1-126">A pointer to a buffer that receives the null-terminated class string of the enumerated subkey.</span></span> <span data-ttu-id="f74b1-127">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f74b1-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f74b1-128">*lpcClass* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f74b1-128">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f74b1-129">Puntero a una variable que especifica el tamaño del búfer especificado por el parámetro *lpClass* en **WCHARs**.</span><span class="sxs-lookup"><span data-stu-id="f74b1-129">A pointer to a variable that specifies the size of the buffer specified by the *lpClass* parameter, in **WCHARs**.</span></span> <span data-ttu-id="f74b1-130">El tamaño debe incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="f74b1-130">The size should include the terminating null character.</span></span> <span data-ttu-id="f74b1-131">Si la función se ejecuta correctamente, *lpcClass* contiene el número de caracteres almacenados en el búfer, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="f74b1-131">If the function succeeds, *lpcClass* contains the number of characters stored in the buffer, not including the terminating null character.</span></span> <span data-ttu-id="f74b1-132">Este parámetro solo puede ser **null** si *lpClass* es **null**.</span><span class="sxs-lookup"><span data-stu-id="f74b1-132">This parameter can be **NULL** only if *lpClass* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f74b1-133">*lpftLastWriteTime* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f74b1-133">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f74b1-134">Puntero a la estructura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que recibe la hora a la que se escribió por última vez en la subclave enumerada.</span><span class="sxs-lookup"><span data-stu-id="f74b1-134">A pointer to [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the time at which the enumerated subkey was last written.</span></span> <span data-ttu-id="f74b1-135">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="f74b1-135">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f74b1-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f74b1-136">Return value</span></span>

<span data-ttu-id="f74b1-137">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f74b1-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="f74b1-138">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="f74b1-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="f74b1-139">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="f74b1-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="f74b1-140">Entre los posibles códigos de error se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="f74b1-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="f74b1-141">Si el búfer de *lpName* es demasiado pequeño para recibir el nombre de la clave, la función devuelve los datos de error \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f74b1-141">If the *lpName* buffer is too small to receive the name of the key, the function returns ERROR\_MORE\_DATA.</span></span>
-   <span data-ttu-id="f74b1-142">Si no hay más subclaves disponibles, la función devuelve el ERROR \_ no hay \_ más \_ elementos.</span><span class="sxs-lookup"><span data-stu-id="f74b1-142">If there are no more subkeys available, the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="remarks"></a><span data-ttu-id="f74b1-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f74b1-143">Remarks</span></span>

<span data-ttu-id="f74b1-144">Para enumerar las subclaves, una aplicación debe llamar inicialmente a la función **OREnumKey** con el parámetro *dwIndex* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="f74b1-144">To enumerate subkeys, an application should initially call the **OREnumKey** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="f74b1-145">A continuación, la aplicación debe incrementar el parámetro *dwIndex* y llamar a **OREnumKey** hasta que no haya más subclaves (lo que significa que la función devuelve el error \_ no hay \_ más \_ elementos).</span><span class="sxs-lookup"><span data-stu-id="f74b1-145">The application should then increment the *dwIndex* parameter and call **OREnumKey** until there are no more subkeys (meaning the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="f74b1-146">La aplicación también puede establecer *dwIndex* en el índice de la última subclave de la primera llamada a la función y disminuir el índice hasta que se Enumere la subclave con el índice 0.</span><span class="sxs-lookup"><span data-stu-id="f74b1-146">The application can also set *dwIndex* to the index of the last subkey on the first call to the function and decrement the index until the subkey with the index 0 is enumerated.</span></span> <span data-ttu-id="f74b1-147">Para recuperar el índice de la última subclave, utilice la función [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) .</span><span class="sxs-lookup"><span data-stu-id="f74b1-147">To retrieve the index of the last subkey, use the [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) function.</span></span>

<span data-ttu-id="f74b1-148">Mientras una aplicación utiliza la función **OREnumKey** , no debe realizar llamadas a las funciones del registro sin conexión que podrían cambiar la clave que se está enumerando.</span><span class="sxs-lookup"><span data-stu-id="f74b1-148">While an application is using the **OREnumKey** function, it should not make calls to any offline registry functions that might change the key being enumerated.</span></span>

## <a name="requirements"></a><span data-ttu-id="f74b1-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f74b1-149">Requirements</span></span>



| <span data-ttu-id="f74b1-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="f74b1-150">Requirement</span></span> | <span data-ttu-id="f74b1-151">Value</span><span class="sxs-lookup"><span data-stu-id="f74b1-151">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f74b1-152">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f74b1-152">Redistributable</span></span><br/> | <span data-ttu-id="f74b1-153">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f74b1-153">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="f74b1-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f74b1-154">Header</span></span><br/>          | <dl> <span data-ttu-id="f74b1-155"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f74b1-155"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="f74b1-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f74b1-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="f74b1-157"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f74b1-157"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f74b1-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="f74b1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f74b1-159">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="f74b1-159">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="f74b1-160">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="f74b1-160">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="f74b1-161">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="f74b1-161">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="f74b1-162">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="f74b1-162">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
