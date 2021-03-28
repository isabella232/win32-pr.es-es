---
description: Determina la ubicación de un recurso con el tipo y el nombre especificados, en el módulo especificado.
ms.assetid: d8322430-5064-407e-8b89-b86b75bf139e
title: FindResourceWrapW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindResourceWrapW
- FindResourceWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 8f76d516570725fe6da5e8a21ec5a29699276ee3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276764"
---
# <a name="findresourcewrapw-function"></a><span data-ttu-id="62c6c-103">FindResourceWrapW función)</span><span class="sxs-lookup"><span data-stu-id="62c6c-103">FindResourceWrapW function</span></span>

<span data-ttu-id="62c6c-104">\[**FindResourceWrapW** está disponible para su uso en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="62c6c-104">\[**FindResourceWrapW** is available for use in Windows XP.</span></span> <span data-ttu-id="62c6c-105">Puede que no esté disponible en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="62c6c-105">It may not be available in subsequent versions.</span></span> <span data-ttu-id="62c6c-106">En su lugar, debe usar [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) .\]</span><span class="sxs-lookup"><span data-stu-id="62c6c-106">You should use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) instead.\]</span></span>

<span data-ttu-id="62c6c-107">Determina la ubicación de un recurso con el tipo y el nombre especificados, en el módulo especificado.</span><span class="sxs-lookup"><span data-stu-id="62c6c-107">Determines the location of a resource with the specified type and name, in the specified module.</span></span>

> [!Note]  
> <span data-ttu-id="62c6c-108">**FindResourceWrapW** es un contenedor para la función **FindResourceW** .</span><span class="sxs-lookup"><span data-stu-id="62c6c-108">**FindResourceWrapW** is a wrapper for the **FindResourceW** function.</span></span> <span data-ttu-id="62c6c-109">Consulte [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) para obtener más notas sobre el uso.</span><span class="sxs-lookup"><span data-stu-id="62c6c-109">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) for further usage notes.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="62c6c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62c6c-110">Syntax</span></span>


```C++
HRSRC FindResourceWrapW(
  _In_ HMODULE hModule,
  _In_ LPCWSTR lpName,
  _In_ LPCWSTR lpType
);
```



## <a name="parameters"></a><span data-ttu-id="62c6c-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62c6c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c6c-112">*hModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62c6c-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c6c-113">Tipo: **HMODULE**</span><span class="sxs-lookup"><span data-stu-id="62c6c-113">Type: **HMODULE**</span></span>

<span data-ttu-id="62c6c-114">Identificador del módulo cuyo archivo ejecutable contiene el recurso.</span><span class="sxs-lookup"><span data-stu-id="62c6c-114">A handle to the module whose executable file contains the resource.</span></span> <span data-ttu-id="62c6c-115">Un valor **null** especifica el identificador de módulo asociado al archivo de imagen que el sistema operativo usó para crear el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="62c6c-115">A value of **NULL** specifies the module handle associated with the image file that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="62c6c-116">*lpName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62c6c-116">*lpName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c6c-117">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="62c6c-117">Type: **LPCWSTR**</span></span>

<span data-ttu-id="62c6c-118">Nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="62c6c-118">The name of the resource.</span></span> <span data-ttu-id="62c6c-119">Para obtener más información, vea [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="62c6c-119">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> <dt>

<span data-ttu-id="62c6c-120">*lpType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="62c6c-120">*lpType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c6c-121">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="62c6c-121">Type: **LPCWSTR**</span></span>

<span data-ttu-id="62c6c-122">Puntero a una cadena que especifica el tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="62c6c-122">A pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="62c6c-123">Para obtener más información, vea [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span><span class="sxs-lookup"><span data-stu-id="62c6c-123">For more information, see [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c6c-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62c6c-124">Return value</span></span>

<span data-ttu-id="62c6c-125">Tipo: **HRSRC**</span><span class="sxs-lookup"><span data-stu-id="62c6c-125">Type: **HRSRC**</span></span>

<span data-ttu-id="62c6c-126">Si la función se ejecuta correctamente, el valor devuelto es un identificador del bloque de información del recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="62c6c-126">If the function succeeds, the return value is a handle to the specified resource's information block.</span></span> <span data-ttu-id="62c6c-127">Para obtener un identificador para el recurso, pase este identificador a la función [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .</span><span class="sxs-lookup"><span data-stu-id="62c6c-127">To obtain a handle to the resource, pass this handle to the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

<span data-ttu-id="62c6c-128">Si se produce un error en la función, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="62c6c-128">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="62c6c-129">Para obtener información de error extendida, llame a la función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="62c6c-129">To get extended error information, call the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="62c6c-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62c6c-130">Remarks</span></span>

<span data-ttu-id="62c6c-131">Si necesita especificar una localización determinada, use la función [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) en lugar de **FindResourceWrapW**.</span><span class="sxs-lookup"><span data-stu-id="62c6c-131">If you need to specify a particular localization, use the [**FindResourceEx**](/windows/win32/api/winbase/nf-winbase-findresourceexa) function rather than **FindResourceWrapW**.</span></span>

<span data-ttu-id="62c6c-132">**FindResourceWrapW** ofrece la posibilidad de usar cadenas Unicode en sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="62c6c-132">**FindResourceWrapW** provides the ability to use Unicode strings in older operating systems.</span></span> <span data-ttu-id="62c6c-133">El método preferido es usar [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) junto con la capa de Microsoft para Unicode (MSLU).</span><span class="sxs-lookup"><span data-stu-id="62c6c-133">The preferred method is to use [**FindResourceW**](/windows/win32/api/winbase/nf-winbase-findresourcea) in conjunction with the Microsoft Layer for Unicode (MSLU).</span></span>

<span data-ttu-id="62c6c-134">Se debe llamar a **FindResourceWrapW** directamente desde Shlwapi.dll, mediante el ordinal 66.</span><span class="sxs-lookup"><span data-stu-id="62c6c-134">**FindResourceWrapW** must be called directly from Shlwapi.dll, using ordinal 66.</span></span>

## <a name="requirements"></a><span data-ttu-id="62c6c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62c6c-135">Requirements</span></span>



| <span data-ttu-id="62c6c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="62c6c-136">Requirement</span></span> | <span data-ttu-id="62c6c-137">Value</span><span class="sxs-lookup"><span data-stu-id="62c6c-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62c6c-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62c6c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="62c6c-139">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="62c6c-139">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62c6c-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62c6c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="62c6c-141">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="62c6c-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="62c6c-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62c6c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="62c6c-143"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="62c6c-143"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="62c6c-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62c6c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62c6c-145"><dt>Shlwapi.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="62c6c-145"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="62c6c-146">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="62c6c-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="62c6c-147">**FindResourceWrapW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="62c6c-147">**FindResourceWrapW** (Unicode)</span></span><br/>                                                                    |



## <a name="see-also"></a><span data-ttu-id="62c6c-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="62c6c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c6c-149">**FindResource**</span><span class="sxs-lookup"><span data-stu-id="62c6c-149">**FindResource**</span></span>](/windows/win32/api/winbase/nf-winbase-findresourcea)
</dt> </dl>

 

 
