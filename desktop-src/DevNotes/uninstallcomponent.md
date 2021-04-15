---
description: Quita un paquete de excepciones.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: UninstallComponent función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: a541f51b030c9be7a26d573794e4df3a7cfc6f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649500"
---
# <a name="uninstallcomponent-function"></a><span data-ttu-id="22a03-103">UninstallComponent función)</span><span class="sxs-lookup"><span data-stu-id="22a03-103">UninstallComponent function</span></span>

<span data-ttu-id="22a03-104">Quita un paquete de excepciones.</span><span class="sxs-lookup"><span data-stu-id="22a03-104">Removes an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="22a03-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22a03-105">Syntax</span></span>


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a><span data-ttu-id="22a03-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22a03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22a03-107">*CompGuid* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="22a03-107">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22a03-108">GUID del componente de excepción que se va a desinstalar.</span><span class="sxs-lookup"><span data-stu-id="22a03-108">The GUID of the exception component being uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="22a03-109">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="22a03-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22a03-110">Marcas usadas para controlar los comportamientos de instalación.</span><span class="sxs-lookup"><span data-stu-id="22a03-110">The flags used to control installation behaviors.</span></span> <span data-ttu-id="22a03-111">Este parámetro puede ser una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="22a03-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="22a03-112">Value</span><span class="sxs-lookup"><span data-stu-id="22a03-112">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="22a03-113">Significado</span><span class="sxs-lookup"><span data-stu-id="22a03-113">Meaning</span></span>                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="22a03-114"><dt>**marcas de COMP \_ \_ NOUI**</dt></span><span class="sxs-lookup"><span data-stu-id="22a03-114"><dt>**COMP\_FLAGS\_NOUI**</dt></span></span> </dl>                                          | <span data-ttu-id="22a03-115">Suprime toda la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="22a03-115">Suppresses all UI.</span></span><br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="22a03-116"><dt>**marcas de COMP \_ \_ actualizar \_ DLLCACHE**</dt></span><span class="sxs-lookup"><span data-stu-id="22a03-116"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt></span></span> </dl>        | <span data-ttu-id="22a03-117">Fuerza la actualización del directorio DLLCACHE cuando se actualiza un archivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="22a03-117">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="22a03-118"><dt>**marcas de COMP \_ \_ usar \_ \_ caché SVCPACK**</dt></span><span class="sxs-lookup"><span data-stu-id="22a03-118"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt></span></span> </dl> | <span data-ttu-id="22a03-119">Usa los archivos almacenados en memoria caché por una instalación de Windows Service Pack para sustituir los archivos de los que se ha realizado una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="22a03-119">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="22a03-120">*VerMajor* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="22a03-120">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22a03-121">Versión principal del componente de excepción que se va a desinstalar.</span><span class="sxs-lookup"><span data-stu-id="22a03-121">The major version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="22a03-122">*Parásitos* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="22a03-122">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22a03-123">Versión secundaria del componente de excepción que se va a desinstalar.</span><span class="sxs-lookup"><span data-stu-id="22a03-123">The minor version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="22a03-124">*VerBuild* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="22a03-124">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22a03-125">Versión de compilación del componente de excepción que se va a desinstalar.</span><span class="sxs-lookup"><span data-stu-id="22a03-125">The build version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="22a03-126">*VerQFE* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="22a03-126">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22a03-127">Revisión de la revisión del componente de excepción que se va a desinstalar.</span><span class="sxs-lookup"><span data-stu-id="22a03-127">The hotfix revision of the Exception component to be uninstalled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22a03-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22a03-128">Return value</span></span>

<span data-ttu-id="22a03-129">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="22a03-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="22a03-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22a03-130">Remarks</span></span>

<span data-ttu-id="22a03-131">Los paquetes de excepción son archivos del sistema de Windows que se publican fuera de una versión completa de Windows y que actualizan los archivos del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="22a03-131">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="22a03-132">Los paquetes de excepción solo los pueden crear equipos del sistema operativo a los que se les ha concedido autorización para actualizar archivos del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="22a03-132">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="22a03-133">Para instalar y desinstalar archivos que no están protegidos por protección de archivos de Windows, use las funciones documentadas en [funciones generales de instalación](https://msdn.microsoft.com/library/ms794585.aspx).</span><span class="sxs-lookup"><span data-stu-id="22a03-133">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="22a03-134">Para instalar controladores de dispositivos, los expendedores deben usar funciones documentadas en funciones de [instalación de dispositivos](https://msdn.microsoft.com/library/ms792954.aspx) y [funciones de Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).</span><span class="sxs-lookup"><span data-stu-id="22a03-134">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="22a03-135">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="22a03-135">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="22a03-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22a03-136">Requirements</span></span>



| <span data-ttu-id="22a03-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="22a03-137">Requirement</span></span> | <span data-ttu-id="22a03-138">Value</span><span class="sxs-lookup"><span data-stu-id="22a03-138">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22a03-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22a03-139">DLL</span></span><br/> | <dl> <span data-ttu-id="22a03-140"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22a03-140"><dt>Msoobci.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22a03-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="22a03-141">See also</span></span>

<dl> <span data-ttu-id="22a03-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="22a03-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="22a03-143">**InstallComponentW**</span><span class="sxs-lookup"><span data-stu-id="22a03-143">**InstallComponentW**</span></span>](installcomponentw.md)
</dt> </dl>

 

 
