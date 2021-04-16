---
description: Establece los datos para el valor de una clave del registro especificada en un subárbol del registro sin conexión.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: Función ORSetValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650159"
---
# <a name="orsetvalue-function"></a><span data-ttu-id="07dfa-103">ORSetValue función)</span><span class="sxs-lookup"><span data-stu-id="07dfa-103">ORSetValue function</span></span>

<span data-ttu-id="07dfa-104">Establece los datos para el valor de una clave del registro especificada en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="07dfa-104">Sets the data for the value of a specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="07dfa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="07dfa-105">Syntax</span></span>


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="07dfa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07dfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07dfa-107">*Identificador* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="07dfa-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07dfa-108">Identificador de una clave del registro abierta en un subárbol del registro sin conexión.</span><span class="sxs-lookup"><span data-stu-id="07dfa-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="07dfa-109">*lpValueName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="07dfa-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07dfa-110">Nombre del valor que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="07dfa-110">The name of the value to be set.</span></span> <span data-ttu-id="07dfa-111">Si un valor con este nombre no está ya presente en la clave, la función lo agrega a la clave.</span><span class="sxs-lookup"><span data-stu-id="07dfa-111">If a value with this name is not already present in the key, the function adds it to the key.</span></span>

<span data-ttu-id="07dfa-112">Si *lpValueName* es **null** o una cadena vacía, "", la función establece el tipo y los datos para el valor sin nombre o predeterminado de la clave.</span><span class="sxs-lookup"><span data-stu-id="07dfa-112">If *lpValueName* is **NULL** or an empty string, "", the function sets the type and data for the key's unnamed or default value.</span></span>

<span data-ttu-id="07dfa-113">Para obtener más información, vea [límites de tamaño de elementos del registro](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="07dfa-113">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="07dfa-114">Las claves del registro no tienen valores predeterminados, pero pueden tener un valor sin nombre, que puede ser de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="07dfa-114">Registry keys do not have default values, but they can have one unnamed value, which can be of any type.</span></span>

</dd> <dt>

<span data-ttu-id="07dfa-115">*dwType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="07dfa-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07dfa-116">El tipo de datos al que apunta el parámetro *lpData* .</span><span class="sxs-lookup"><span data-stu-id="07dfa-116">The type of data pointed to by the *lpData* parameter.</span></span> <span data-ttu-id="07dfa-117">Para obtener una lista de los tipos posibles, vea [Registry Value Types](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="07dfa-117">For a list of the possible types, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="07dfa-118">*lpData* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="07dfa-118">*lpData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="07dfa-119">Datos que se van a almacenar.</span><span class="sxs-lookup"><span data-stu-id="07dfa-119">The data to be stored.</span></span>

<span data-ttu-id="07dfa-120">En el caso de los tipos basados en cadena, como REG \_ SZ, la cadena debe terminar en NULL.</span><span class="sxs-lookup"><span data-stu-id="07dfa-120">For string-based types, such as REG\_SZ, the string must be null-terminated.</span></span> <span data-ttu-id="07dfa-121">En el caso del \_ tipo de datos reg multi \_ SZ, la cadena debe terminar con dos caracteres null.</span><span class="sxs-lookup"><span data-stu-id="07dfa-121">For the REG\_MULTI\_SZ data type, the string must be terminated with two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="07dfa-122">*cbData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="07dfa-122">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07dfa-123">Tamaño de la información a la que apunta el parámetro *lpData* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="07dfa-123">The size of the information pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="07dfa-124">Si los datos son del tipo REG \_ SZ, REG \_ Expand \_ SZ o REG \_ multi \_ SZ, *cbData* debe incluir el tamaño del carácter o caracteres nulos de terminación.</span><span class="sxs-lookup"><span data-stu-id="07dfa-124">If the data is of type REG\_SZ, REG\_EXPAND\_SZ, or REG\_MULTI\_SZ, *cbData* must include the size of the terminating null character or characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07dfa-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07dfa-125">Return value</span></span>

<span data-ttu-id="07dfa-126">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="07dfa-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="07dfa-127">Si se produce un error en la función, el valor devuelto es un código de error distinto de cero definido en Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="07dfa-127">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="07dfa-128">Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.</span><span class="sxs-lookup"><span data-stu-id="07dfa-128">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="07dfa-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07dfa-129">Remarks</span></span>

<span data-ttu-id="07dfa-130">Los tamaños de valor están limitados por la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="07dfa-130">Value sizes are limited by available memory.</span></span> <span data-ttu-id="07dfa-131">Los valores largos (más de 2048 bytes) deben almacenarse como archivos con los nombres de archivo almacenados en el registro.</span><span class="sxs-lookup"><span data-stu-id="07dfa-131">Long values (more than 2048 bytes) should be stored as files with the file names stored in the registry.</span></span> <span data-ttu-id="07dfa-132">Esto ayuda a que el registro funcione de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="07dfa-132">This helps the registry perform efficiently.</span></span> <span data-ttu-id="07dfa-133">Los elementos de la aplicación como iconos, mapas de bits y archivos ejecutables deben almacenarse como archivos y no colocarse en el registro.</span><span class="sxs-lookup"><span data-stu-id="07dfa-133">Application elements such as icons, bitmaps, and executable files should be stored as files and not be placed in the registry.</span></span>

## <a name="requirements"></a><span data-ttu-id="07dfa-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07dfa-134">Requirements</span></span>



| <span data-ttu-id="07dfa-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="07dfa-135">Requirement</span></span> | <span data-ttu-id="07dfa-136">Value</span><span class="sxs-lookup"><span data-stu-id="07dfa-136">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07dfa-137">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="07dfa-137">Redistributable</span></span><br/> | <span data-ttu-id="07dfa-138">Windows offline Registry Library versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="07dfa-138">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="07dfa-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07dfa-139">Header</span></span><br/>          | <dl> <span data-ttu-id="07dfa-140"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="07dfa-140"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="07dfa-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="07dfa-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="07dfa-142"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07dfa-142"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07dfa-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="07dfa-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07dfa-144">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="07dfa-144">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="07dfa-145">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="07dfa-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
