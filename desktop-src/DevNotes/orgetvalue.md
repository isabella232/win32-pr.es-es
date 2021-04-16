---
description: Recupera el tipo y los datos para el valor del registro especificado en un subárbol del registro sin conexión.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: Función ORGetValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649850"
---
# <a name="orgetvalue-function"></a><span data-ttu-id="4f4ba-103">ORGetValue función)</span><span class="sxs-lookup"><span data-stu-id="4f4ba-103">ORGetValue function</span></span>

<span data-ttu-id="4f4ba-104">Recupera el tipo y los datos para el valor del registro especificado en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-104">Retrieves the type and data for the specified registry value in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f4ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f4ba-105">Syntax</span></span>


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="4f4ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4f4ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f4ba-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4f4ba-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f4ba-108">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="4f4ba-109">*lpSubKey* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f4ba-109">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f4ba-110">Nombre de la clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-110">The name of the registry key.</span></span> <span data-ttu-id="4f4ba-111">Esta clave debe ser una subclave de la clave especificada por el parámetro *Handle* .</span><span class="sxs-lookup"><span data-stu-id="4f4ba-111">This key must be a subkey of the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="4f4ba-112">Este parámetro puede ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="4f4ba-113">Los nombres de clave no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-113">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="4f4ba-114">*lpValue* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f4ba-114">*lpValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f4ba-115">Nombre del valor del registro.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-115">The name of the registry value.</span></span> <span data-ttu-id="4f4ba-116">Si este parámetro es **null** o una cadena vacía, "", la función recupera el tipo y los datos para el valor sin nombre o predeterminado de la clave, si existe.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-116">If this parameter is **NULL** or an empty string, "", the function retrieves the type and data for the key's unnamed or default value, if any.</span></span> <span data-ttu-id="4f4ba-117">Para obtener más información, vea [límites de tamaño de elementos del registro](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-117">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="4f4ba-118">Las claves no tienen un valor predeterminado o sin nombre.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-118">Keys do not automatically have an unnamed or default value.</span></span> <span data-ttu-id="4f4ba-119">Los valores sin nombre pueden ser de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-119">Unnamed values can be of any type.</span></span>

<span data-ttu-id="4f4ba-120">Los nombres de valor no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-120">Value names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="4f4ba-121">*pdwType* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f4ba-121">*pdwType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f4ba-122">Puntero a una variable que recibe un código que indica el tipo de datos almacenados en el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-122">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="4f4ba-123">Para obtener una lista de los códigos de tipo posibles, vea [Registry Value Types](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="4f4ba-123">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="4f4ba-124">Este parámetro puede ser **null** si el tipo no es necesario.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-124">This parameter can be **NULL** if the type is not required.</span></span>

</dd> <dt>

<span data-ttu-id="4f4ba-125">*pvData* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f4ba-125">*pvData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f4ba-126">Un puntero a un búfer que recibe los datos del valor.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-126">A pointer to a buffer that receives the value's data.</span></span> <span data-ttu-id="4f4ba-127">Este parámetro puede ser **null** si los datos no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-127">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="4f4ba-128">Si los datos son una cadena, la función comprueba si hay un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-128">If the data is a string, the function checks for a terminating null character.</span></span> <span data-ttu-id="4f4ba-129">Si no se encuentra ninguno, la cadena se almacena con un terminador nulo si el búfer es lo suficientemente grande como para alojar el carácter adicional.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-129">If one is not found, the string is stored with a null terminator if the buffer is large enough to accommodate the extra character.</span></span> <span data-ttu-id="4f4ba-130">De lo contrario, se produce un error en la función y se devuelven \_ más \_ datos.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-130">Otherwise, the function fails and returns ERROR\_MORE\_DATA.</span></span>

</dd> <dt>

<span data-ttu-id="4f4ba-131">*pcbData* \[ in, out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4f4ba-131">*pcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4f4ba-132">Puntero a una variable que especifica el tamaño del búfer al que apunta el parámetro *pvData* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-132">A pointer to a variable that specifies the size of the buffer pointed to by the *pvData* parameter, in bytes.</span></span> <span data-ttu-id="4f4ba-133">Cuando la función devuelve, esta variable contiene el tamaño de los datos copiados en *pvData*.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-133">When the function returns, this variable contains the size of the data copied to *pvData*.</span></span>

<span data-ttu-id="4f4ba-134">El parámetro *pcbData* solo puede ser **null** si *pvData* es **null**.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-134">The *pcbData* parameter can be **NULL** only if *pvData* is **NULL**.</span></span>

<span data-ttu-id="4f4ba-135">Si los datos tienen el \_ tipo REG SZ, REG \_ multi \_ SZ o REG \_ Expand \_ SZ, este tamaño incluye el carácter o caracteres nulos de terminación.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-135">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="4f4ba-136">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-136">For more information, see Remarks.</span></span>

<span data-ttu-id="4f4ba-137">Si el búfer especificado por el parámetro *pvData* no es lo suficientemente grande como para contener los datos, la función devuelve el error \_ más \_ datos y almacena el tamaño de búfer necesario en la variable a la que apunta *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-137">If the buffer specified by *pvData* parameter is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="4f4ba-138">En este caso, el contenido del búfer *pvData* no está definido.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-138">In this case, the contents of the *pvData* buffer are undefined.</span></span>

<span data-ttu-id="4f4ba-139">Si *pvData* es **null** y *pcbData* no es **null**, la función devuelve el error \_ Success y almacena el tamaño de los datos, en bytes, en la variable a la que apunta *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-139">If *pvData* is **NULL**, and *pcbData* is non-**NULL**, the function returns ERROR\_SUCCESS and stores the size of the data, in bytes, in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="4f4ba-140">Esto permite que una aplicación determine la mejor manera de asignar un búfer para los datos del valor.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-140">This enables an application to determine the best way to allocate a buffer for the value's data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f4ba-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f4ba-141">Return value</span></span>

<span data-ttu-id="4f4ba-142">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-142">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="4f4ba-143">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-143">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="4f4ba-144">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-144">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f4ba-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f4ba-145">Remarks</span></span>

<span data-ttu-id="4f4ba-146">Una aplicación normalmente llama a la función [**OREnumValue**](orenumvalue.md) para determinar los nombres de valor y, después, llama a la función **ORGetValue** para recuperar los datos de los nombres.</span><span class="sxs-lookup"><span data-stu-id="4f4ba-146">An application typically calls the [**OREnumValue**](orenumvalue.md) function to determine the value names and then calls the **ORGetValue** function to retrieve the data for the names.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f4ba-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f4ba-147">Requirements</span></span>



| <span data-ttu-id="4f4ba-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f4ba-148">Requirement</span></span> | <span data-ttu-id="4f4ba-149">Value</span><span class="sxs-lookup"><span data-stu-id="4f4ba-149">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4ba-150">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4f4ba-150">Redistributable</span></span><br/> | <span data-ttu-id="4f4ba-151">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4f4ba-151">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="4f4ba-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4f4ba-152">Header</span></span><br/>          | <dl> <span data-ttu-id="4f4ba-153"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f4ba-153"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f4ba-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f4ba-154">DLL</span></span><br/>             | <dl> <span data-ttu-id="4f4ba-155"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f4ba-155"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f4ba-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f4ba-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4ba-157">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-157">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="4f4ba-158">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-158">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="4f4ba-159">**OREnumValue**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-159">**OREnumValue**</span></span>](orenumvalue.md)
</dt> <dt>

[<span data-ttu-id="4f4ba-160">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-160">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="4f4ba-161">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="4f4ba-161">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
