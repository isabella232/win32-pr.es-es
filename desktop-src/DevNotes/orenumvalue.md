---
description: Enumera los valores de la clave del registro abierta especificada en un subárbol del registro sin conexión. La función recupera información de un valor en la clave especificada cada vez que se llama a la función.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Función OREnumValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670891"
---
# <a name="orenumvalue-function"></a><span data-ttu-id="820f9-104">OREnumValue función)</span><span class="sxs-lookup"><span data-stu-id="820f9-104">OREnumValue function</span></span>

<span data-ttu-id="820f9-105">Enumera los valores de la clave del registro abierta especificada en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="820f9-105">Enumerates the values for the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="820f9-106">La función recupera información de un valor en la clave especificada cada vez que se llama a la función.</span><span class="sxs-lookup"><span data-stu-id="820f9-106">The function retrieves information for one value under the specified key each time the function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="820f9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="820f9-107">Syntax</span></span>


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
);
```



## <a name="parameters"></a><span data-ttu-id="820f9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="820f9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="820f9-109">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="820f9-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="820f9-110">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="820f9-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="820f9-111">*dwIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="820f9-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="820f9-112">Índice del valor que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="820f9-112">The index of the value to be retrieved.</span></span> <span data-ttu-id="820f9-113">Este parámetro debe ser cero para la primera llamada a la función y, a continuación, incrementarse en las llamadas posteriores.</span><span class="sxs-lookup"><span data-stu-id="820f9-113">This parameter should be zero for the first call to the function and then be incremented for subsequent calls.</span></span>

<span data-ttu-id="820f9-114">Dado que los valores no están ordenados, cualquier valor nuevo tendrá un índice arbitrario.</span><span class="sxs-lookup"><span data-stu-id="820f9-114">Because values are not ordered, any new value will have an arbitrary index.</span></span> <span data-ttu-id="820f9-115">Esto significa que la función puede devolver valores en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="820f9-115">This means that the function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="820f9-116">*lpValueName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="820f9-116">*lpValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="820f9-117">Un puntero a un búfer que recibe el nombre del valor como una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="820f9-117">A pointer to a buffer that receives the name of the value as a null-terminated string.</span></span> <span data-ttu-id="820f9-118">Este búfer debe ser lo suficientemente grande como para incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="820f9-118">This buffer must be large enough to include the terminating null character.</span></span>

<span data-ttu-id="820f9-119">Para obtener más información, vea [límites de tamaño de elementos del registro](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="820f9-119">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="820f9-120">*lpcValueName* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="820f9-120">*lpcValueName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="820f9-121">Puntero a una variable que especifica el tamaño del búfer al que apunta el parámetro *lpValueName* , en caracteres.</span><span class="sxs-lookup"><span data-stu-id="820f9-121">A pointer to a variable that specifies the size of the buffer pointed to by the *lpValueName* parameter, in characters.</span></span> <span data-ttu-id="820f9-122">Cuando la función devuelve, la variable recibe el número de caracteres almacenados en el búfer, sin incluir el carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="820f9-122">When the function returns, the variable receives the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="820f9-123">*lpType* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="820f9-123">*lpType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="820f9-124">Puntero a una variable que recibe un código que indica el tipo de datos almacenados en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="820f9-124">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="820f9-125">Para obtener una lista de los códigos de tipo posibles, vea [Registry Value Types](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="820f9-125">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="820f9-126">El parámetro *lpType* puede ser **null** si no se requiere el código de tipo.</span><span class="sxs-lookup"><span data-stu-id="820f9-126">The *lpType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="820f9-127">*lpData* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="820f9-127">*lpData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="820f9-128">Un puntero a un búfer que recibe los datos de la entrada de valor.</span><span class="sxs-lookup"><span data-stu-id="820f9-128">A pointer to a buffer that receives the data for the value entry.</span></span> <span data-ttu-id="820f9-129">Este parámetro puede ser **null** si los datos no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="820f9-129">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="820f9-130">Si *lpData* es **null** y *lpcbData* no es **null**, la función almacena el tamaño de los datos, en bytes, en la variable a la que apunta *lpcbData*.</span><span class="sxs-lookup"><span data-stu-id="820f9-130">If *lpData* is **NULL** and *lpcbData* is non-**NULL**, the function stores the size of the data, in bytes, in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="820f9-131">Esto permite que una aplicación determine la mejor manera de asignar un búfer para los datos.</span><span class="sxs-lookup"><span data-stu-id="820f9-131">This enables an application to determine the best way to allocate a buffer for the data.</span></span>

</dd> <dt>

<span data-ttu-id="820f9-132">*lpcbData* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="820f9-132">*lpcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="820f9-133">Puntero a una variable que especifica el tamaño del búfer al que apunta el parámetro *lpData* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="820f9-133">A pointer to a variable that specifies the size of the buffer pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="820f9-134">Cuando la función devuelve, la variable recibe el número de bytes almacenados en el búfer.</span><span class="sxs-lookup"><span data-stu-id="820f9-134">When the function returns, the variable receives the number of bytes stored in the buffer.</span></span>

<span data-ttu-id="820f9-135">Este parámetro solo puede ser **null** si *lpData* es **null**.</span><span class="sxs-lookup"><span data-stu-id="820f9-135">This parameter can be **NULL** only if *lpData* is **NULL**.</span></span>

<span data-ttu-id="820f9-136">Si los datos tienen el \_ tipo REG SZ, REG \_ multi \_ SZ o REG \_ Expand \_ SZ, este tamaño incluye el carácter o caracteres nulos de terminación.</span><span class="sxs-lookup"><span data-stu-id="820f9-136">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="820f9-137">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="820f9-137">For more information, see Remarks.</span></span>

<span data-ttu-id="820f9-138">Si el búfer especificado por *lpData* no es lo suficientemente grande como para contener los datos, la función devuelve el error \_ más \_ datos y almacena el tamaño de búfer necesario en la variable a la que apunta *lpcbData*.</span><span class="sxs-lookup"><span data-stu-id="820f9-138">If the buffer specified by *lpData* is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="820f9-139">En este caso, el contenido de *lpData* no está definido.</span><span class="sxs-lookup"><span data-stu-id="820f9-139">In this case, the contents of *lpData* are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="820f9-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="820f9-140">Return value</span></span>

<span data-ttu-id="820f9-141">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="820f9-141">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="820f9-142">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="820f9-142">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="820f9-143">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="820f9-143">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="820f9-144">Si el búfer de *lpData* es demasiado pequeño para recibir el valor, la función devuelve los datos de error \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="820f9-144">If the *lpData* buffer is too small to receive the value, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="820f9-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="820f9-145">Remarks</span></span>

<span data-ttu-id="820f9-146">Para enumerar los valores, una aplicación debe llamar inicialmente a la función **OREnumValue** con el parámetro *dwIndex* establecido en cero.</span><span class="sxs-lookup"><span data-stu-id="820f9-146">To enumerate values, an application should initially call the **OREnumValue** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="820f9-147">A continuación, la aplicación debe incrementar *dwIndex* y llamar a la función **OREnumValue** hasta que no haya más valores (hasta que la función devuelva el error \_ no \_ más \_ elementos).</span><span class="sxs-lookup"><span data-stu-id="820f9-147">The application should then increment *dwIndex* and call the **OREnumValue** function until there are no more values (until the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="820f9-148">La aplicación también puede establecer *dwIndex* en el índice del último valor de la primera llamada a la función y disminuir el índice hasta que se enumere el valor con el índice 0.</span><span class="sxs-lookup"><span data-stu-id="820f9-148">The application can also set *dwIndex* to the index of the last value on the first call to the function and decrement the index until the value with index 0 is enumerated.</span></span> <span data-ttu-id="820f9-149">Para recuperar el índice del último valor, utilice la función [**ORQueryInfoKey**](orqueryinfokey.md) .</span><span class="sxs-lookup"><span data-stu-id="820f9-149">To retrieve the index of the last value, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

<span data-ttu-id="820f9-150">Al utilizar **OREnumValue**, una aplicación no debe llamar a las funciones del registro sin conexión que puedan cambiar la clave que se consulta.</span><span class="sxs-lookup"><span data-stu-id="820f9-150">While using **OREnumValue**, an application should not call any offline registry functions that might change the key being queried.</span></span>

<span data-ttu-id="820f9-151">Si los datos tienen el \_ tipo REG SZ, REG \_ multi \_ SZ o REG \_ Expand \_ SZ, es posible que la cadena no se haya almacenado con los caracteres correctos de terminación null.</span><span class="sxs-lookup"><span data-stu-id="820f9-151">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, the string may not have been stored with the proper null-terminating characters.</span></span> <span data-ttu-id="820f9-152">Por lo tanto, aunque la función devuelva el ERROR \_ Success, la aplicación debe asegurarse de que la cadena se termina correctamente antes de usarla; de lo contrario, puede sobrescribir un búfer.</span><span class="sxs-lookup"><span data-stu-id="820f9-152">Therefore, even if the function returns ERROR\_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer.</span></span> <span data-ttu-id="820f9-153">(Tenga en cuenta que REG \_ Las \_ cadenas de varios SZ deben tener dos caracteres de terminación null).</span><span class="sxs-lookup"><span data-stu-id="820f9-153">(Note that REG\_MULTI\_SZ strings should have two null-terminating characters.)</span></span>

<span data-ttu-id="820f9-154">Para determinar el tamaño máximo del nombre y los búferes de datos, use la función [**ORQueryInfoKey**](orqueryinfokey.md) .</span><span class="sxs-lookup"><span data-stu-id="820f9-154">To determine the maximum size of the name and data buffers, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="820f9-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="820f9-155">Requirements</span></span>



| <span data-ttu-id="820f9-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="820f9-156">Requirement</span></span> | <span data-ttu-id="820f9-157">Value</span><span class="sxs-lookup"><span data-stu-id="820f9-157">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="820f9-158">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="820f9-158">Redistributable</span></span><br/> | <span data-ttu-id="820f9-159">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="820f9-159">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="820f9-160">Encabezado</span><span class="sxs-lookup"><span data-stu-id="820f9-160">Header</span></span><br/>          | <dl> <span data-ttu-id="820f9-161"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="820f9-161"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="820f9-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="820f9-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="820f9-163"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="820f9-163"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="820f9-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="820f9-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="820f9-165">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="820f9-165">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="820f9-166">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="820f9-166">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="820f9-167">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="820f9-167">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="820f9-168">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="820f9-168">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
