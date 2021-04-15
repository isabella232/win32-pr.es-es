---
description: Abre un objeto de directorio existente.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: NtOpenDirectoryObject función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649585"
---
# <a name="ntopendirectoryobject-function"></a><span data-ttu-id="fb3bc-103">NtOpenDirectoryObject función)</span><span class="sxs-lookup"><span data-stu-id="fb3bc-103">NtOpenDirectoryObject function</span></span>

<span data-ttu-id="fb3bc-104">\[Esta función puede modificarse o no estar disponible en el futuro.\]</span><span class="sxs-lookup"><span data-stu-id="fb3bc-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="fb3bc-105">Abre un objeto de directorio existente.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-105">Opens an existing directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3bc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb3bc-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="fb3bc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb3bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb3bc-108">*DirectoryHandle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fb3bc-108">*DirectoryHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3bc-109">Identificador del objeto de directorio recién abierto.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-109">A handle to the newly opened directory object.</span></span>

</dd> <dt>

<span data-ttu-id="fb3bc-110">*DesiredAccess* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb3bc-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3bc-111">Una [**\_ máscara de acceso**](../secauthz/access-mask.md) que especifica el acceso solicitado al objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="fb3bc-112">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="fb3bc-113">Value</span><span class="sxs-lookup"><span data-stu-id="fb3bc-113">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="fb3bc-114">Significado</span><span class="sxs-lookup"><span data-stu-id="fb3bc-114">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <span data-ttu-id="fb3bc-115"><dt>**Directorio \_ de CONSULTA**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-115"><dt>**DIRECTORY\_QUERY**</dt> <dt>0x0001</dt></span></span> </dl>                                            | <span data-ttu-id="fb3bc-116">Consultar el acceso al objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-116">Query access to the directory object.</span></span><br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <span data-ttu-id="fb3bc-117"><dt>**Directorio \_ de ATRAVESAR**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-117"><dt>**DIRECTORY\_TRAVERSE**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="fb3bc-118">Nombre: acceso de búsqueda al objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-118">Name-lookup access to the directory object.</span></span><br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <span data-ttu-id="fb3bc-119"><dt>**Directorio \_ de CREAR \_ objeto**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-119"><dt>**DIRECTORY\_CREATE\_OBJECT**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="fb3bc-120">Acceso de creación de nombre al objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-120">Name-creation access to the directory object.</span></span><br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <span data-ttu-id="fb3bc-121"><dt>**Directorio \_ de CREAR \_ SUBdirectorio**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-121"><dt>**DIRECTORY\_CREATE\_SUBDIRECTORY**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="fb3bc-122">Subdirectorio: acceso de creación al objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-122">Subdirectory-creation access to the directory object.</span></span><br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <span data-ttu-id="fb3bc-123"><dt>**Directorio \_ de Todos \_ los**</dt> derechos de acceso <dt>estándar \_ \_ requeridos \| 0xF</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-123"><dt>**DIRECTORY\_ALL\_ACCESS**</dt> <dt>STANDARD\_RIGHTS\_REQUIRED \| 0xF</dt></span></span> </dl> | <span data-ttu-id="fb3bc-124">Todos los derechos anteriores y los **\_ derechos estándar \_ necesarios**.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-124">All of the preceding rights plus **STANDARD\_RIGHTS\_REQUIRED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fb3bc-125">*ObjectAttributes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fb3bc-125">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3bc-126">Atributos del objeto de directorio.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-126">The attributes for the directory object.</span></span> <span data-ttu-id="fb3bc-127">Para inicializar la estructura de **\_ atributos de objeto** , use la macro **InitializeObjectAttributes** .</span><span class="sxs-lookup"><span data-stu-id="fb3bc-127">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="fb3bc-128">Para obtener más información, consulte la documentación de estos elementos en la documentación del WDK.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-128">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb3bc-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb3bc-129">Return value</span></span>

<span data-ttu-id="fb3bc-130">La función devuelve el estado \_ correcto o un estado de error.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-130">The function returns STATUS\_SUCCESS or an error status.</span></span> <span data-ttu-id="fb3bc-131">Los códigos de estado posibles son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-131">The possible status codes include the following.</span></span>



| <span data-ttu-id="fb3bc-132">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fb3bc-132">Return code</span></span>                                                                                                       | <span data-ttu-id="fb3bc-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb3bc-133">Description</span></span>                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb3bc-134"><dt>**Estado de \_ recursos insuficientes \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-134"><dt>**STATUS\_INSUFFICIENT\_RESOURCES**</dt></span></span> </dl>    | <span data-ttu-id="fb3bc-135">No se pudo asignar un búfer temporal requerido por esta función.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-135">A temporary buffer required by this function could not be allocated.</span></span><br/>                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="fb3bc-136"><dt>**ESTADO \_ parámetro no válido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-136"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="fb3bc-137">El parámetro ObjectAttributes especificado era un puntero **nulo** , no un puntero válido a una estructura de **\_ atributos de objeto** o algunos de los miembros especificados en la estructura de **\_ atributos de objeto** no eran válidos.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-137">The specified ObjectAttributes parameter was a **NULL** pointer, not a valid pointer to an **OBJECT\_ATTRIBUTES** structure, or some of the members specified in the **OBJECT\_ATTRIBUTES** structure were not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="fb3bc-138"><dt>**nombre del objeto de estado \_ \_ \_ no válido**</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-138"><dt>**STATUS\_OBJECT\_NAME\_INVALID**</dt></span></span> </dl>      | <span data-ttu-id="fb3bc-139">El parámetro *ObjectAttributes* contenía un miembro **objectname** en la estructura de **\_ atributos de objeto** que no era válida porque se encontró una cadena vacía después del carácter **\_ \_ \_ separador de ruta de acceso de nombre de objeto** .</span><span class="sxs-lookup"><span data-stu-id="fb3bc-139">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that was not valid because an empty string was found after the **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="fb3bc-140"><dt>**nombre del objeto de estado \_ \_ \_ no \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-140"><dt>**STATUS\_OBJECT\_NAME\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="fb3bc-141">El parámetro *ObjectAttributes* contenía un miembro **objectname** en la estructura de **\_ atributos de objeto** que no se pudo encontrar.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-141">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that could not be found.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="fb3bc-142"><dt>**Ruta de acceso del objeto de estado \_ \_ \_ no \_ encontrada**</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-142"><dt>**STATUS\_OBJECT\_PATH\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="fb3bc-143">El parámetro *ObjectAttributes* contenía un miembro **objectname** en la estructura de **\_ atributos de objeto** con una ruta de acceso de objeto que no se pudo encontrar.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-143">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure with an object path that could not be found.</span></span> <br/>                                                                                                                                      |
| <dl> <span data-ttu-id="fb3bc-144"><dt>**Estado \_ de Sintaxis de ruta de objeto \_ \_ \_ incorrecta**</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-144"><dt>**STATUS\_OBJECT\_PATH\_SYNTAX\_BAD** </dt></span></span> </dl> | <span data-ttu-id="fb3bc-145">El parámetro *ObjectAttributes* no contenía un miembro **RootDirectory** , pero el miembro **objectname** de la estructura de **\_ atributos de objeto** era una cadena vacía o no contenía un carácter **\_ \_ \_ separador de ruta de acceso de nombre de objeto** .</span><span class="sxs-lookup"><span data-stu-id="fb3bc-145">The *ObjectAttributes* parameter did not contain a **RootDirectory** member, but the **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure was an empty string or did not contain an **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span> <span data-ttu-id="fb3bc-146">Esto indica una sintaxis incorrecta para la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="fb3bc-146">This indicates incorrect syntax for the object path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb3bc-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb3bc-147">Remarks</span></span>

<span data-ttu-id="fb3bc-148">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="fb3bc-148">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb3bc-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb3bc-149">Requirements</span></span>



| <span data-ttu-id="fb3bc-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb3bc-150">Requirement</span></span> | <span data-ttu-id="fb3bc-151">Value</span><span class="sxs-lookup"><span data-stu-id="fb3bc-151">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3bc-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb3bc-152">DLL</span></span><br/> | <dl> <span data-ttu-id="fb3bc-153"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bc-153"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb3bc-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb3bc-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3bc-155">**NtQueryDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="fb3bc-155">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
