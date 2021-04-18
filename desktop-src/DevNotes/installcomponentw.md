---
description: Instala un paquete de excepciones.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: InstallComponentW función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 4d262322be6084429f03d5725f61c0e0f7140871
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660987"
---
# <a name="installcomponentw-function"></a><span data-ttu-id="5157b-103">InstallComponentW función)</span><span class="sxs-lookup"><span data-stu-id="5157b-103">InstallComponentW function</span></span>

<span data-ttu-id="5157b-104">Instala un paquete de excepciones.</span><span class="sxs-lookup"><span data-stu-id="5157b-104">Installs an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="5157b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5157b-105">Syntax</span></span>


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="5157b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5157b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5157b-107">*InfPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5157b-107">*InfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5157b-108">Ruta de acceso al INF de excepción que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="5157b-108">The path to the exception INF to process.</span></span>

</dd> <dt>

<span data-ttu-id="5157b-109">*CompGuid* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5157b-109">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5157b-110">GUID del componente de excepción que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="5157b-110">The GUID of the exception component being installed.</span></span>

</dd> <dt>

<span data-ttu-id="5157b-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="5157b-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5157b-112">Marcas usadas para controlar los comportamientos de instalación.</span><span class="sxs-lookup"><span data-stu-id="5157b-112">The flags used to control installation behaviors.</span></span> <span data-ttu-id="5157b-113">Este parámetro puede ser una combinación de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5157b-113">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="5157b-114">Value</span><span class="sxs-lookup"><span data-stu-id="5157b-114">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="5157b-115">Significado</span><span class="sxs-lookup"><span data-stu-id="5157b-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <span data-ttu-id="5157b-116"><dt>**COMP \_ . MARCAS \_ fuerzan**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="5157b-116"><dt>**COMP\_FLAGS\_FORCE**</dt> <dt>0x00000020</dt></span></span> </dl>                             | <span data-ttu-id="5157b-117">Omite la comprobación de versión en los reemplazos de archivos.</span><span class="sxs-lookup"><span data-stu-id="5157b-117">Skips the version check on file replacements.</span></span><br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <span data-ttu-id="5157b-118"><dt>**COMP \_ . las marcas \_ requieren \_ desinstalación**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="5157b-118"><dt>**COMP\_FLAGS\_NEEDS\_UNINSTALL**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="5157b-119">Realice una copia de seguridad de los archivos que se han actualizado para que los utilice una desinstalación del componente.</span><span class="sxs-lookup"><span data-stu-id="5157b-119">Back up files that are updated to be used by an uninstall of the component.</span></span><br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <span data-ttu-id="5157b-120"><dt>**COMP \_ . MARCAS \_ sin \_ sobrescritura**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="5157b-120"><dt>**COMP\_FLAGS\_NO\_OVERWRITE**</dt> <dt></dt></span></span> </dl>                 | <span data-ttu-id="5157b-121">Omite la copia de seguridad de archivos si la versión del componente de excepción es igual que un componente instalado.</span><span class="sxs-lookup"><span data-stu-id="5157b-121">Skips backing up files if the Exception component version is the same as an installed component.</span></span> <span data-ttu-id="5157b-122">Esta marca se usa en un escenario de reinstalación.</span><span class="sxs-lookup"><span data-stu-id="5157b-122">This flag is used in a reinstallation scenario.</span></span><br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="5157b-123"><dt>**COMP \_ . FLAGs \_ NOUI**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="5157b-123"><dt>**COMP\_FLAGS\_NOUI**</dt> <dt>0x00000002</dt></span></span> </dl>                                | <span data-ttu-id="5157b-124">Suprime toda la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5157b-124">Suppresses all UI.</span></span><br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="5157b-125"><dt>**COMP \_ . MARCAS de \_ actualización de \_ DLLCACHE**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="5157b-125"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="5157b-126">Fuerza la actualización del directorio DLLCACHE cuando se actualiza un archivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="5157b-126">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="5157b-127"><dt>**COMP \_ . MARCAS \_ usar \_ \_ caché SVCPACK**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="5157b-127"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="5157b-128">Usa los archivos almacenados en memoria caché por una instalación de Windows Service Pack para sustituir los archivos de los que se ha realizado una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5157b-128">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="5157b-129">*VerMajor* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5157b-129">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5157b-130">Versión principal del componente de excepción.</span><span class="sxs-lookup"><span data-stu-id="5157b-130">The major version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="5157b-131">*Parásitos* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5157b-131">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5157b-132">Versión secundaria del componente de excepción.</span><span class="sxs-lookup"><span data-stu-id="5157b-132">The minor version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="5157b-133">*VerBuild* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5157b-133">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5157b-134">Versión de compilación del componente de excepción.</span><span class="sxs-lookup"><span data-stu-id="5157b-134">The build version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="5157b-135">*VerQFE* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5157b-135">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5157b-136">Revisión de la revisión del componente de excepción.</span><span class="sxs-lookup"><span data-stu-id="5157b-136">The hotfix revision of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="5157b-137">*Nombre* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5157b-137">*Name* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5157b-138">Cadena descriptiva del componente que muestra el cuadro de diálogo protección de archivos de Windows si el sistema operativo detecta que un archivo de protección contra archivos de Windows está dañado, alterado o dañado.</span><span class="sxs-lookup"><span data-stu-id="5157b-138">The descriptive string of the component shown by the Windows File Protection dialog box if the operating system detects that a Windows File Protection protect file is damaged, tampered with, or corrupted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5157b-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5157b-139">Return value</span></span>

<span data-ttu-id="5157b-140">Esta función devuelve un valor **HRESULT** (es \_ correcto o un código de error).</span><span class="sxs-lookup"><span data-stu-id="5157b-140">This function returns an **HRESULT** value (S\_OK or a failure code).</span></span> <span data-ttu-id="5157b-141">Un código de error se puede comprobar con un valor de 0x20000100 para determinar si el error se debe a que se requiere un reinicio.</span><span class="sxs-lookup"><span data-stu-id="5157b-141">A failure code can be checked against a value of 0x20000100 to determine whether the failure is because a reboot is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="5157b-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5157b-142">Remarks</span></span>

<span data-ttu-id="5157b-143">Los paquetes de excepción son archivos del sistema de Windows que se publican fuera de una versión completa de Windows y que actualizan los archivos del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5157b-143">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="5157b-144">Los paquetes de excepción solo los pueden crear equipos del sistema operativo a los que se les ha concedido autorización para actualizar archivos del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="5157b-144">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="5157b-145">Para instalar y desinstalar archivos que no están protegidos por protección de archivos de Windows, use las funciones documentadas en [funciones generales de instalación](https://msdn.microsoft.com/library/ms794585.aspx).</span><span class="sxs-lookup"><span data-stu-id="5157b-145">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="5157b-146">Para instalar controladores de dispositivos, los expendedores deben usar funciones documentadas en funciones de [instalación de dispositivos](https://msdn.microsoft.com/library/ms792954.aspx) y [funciones de Configuration Manager PNP](https://msdn.microsoft.com/library/ms790838.aspx).</span><span class="sxs-lookup"><span data-stu-id="5157b-146">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="5157b-147">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="5157b-147">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5157b-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5157b-148">Requirements</span></span>



| <span data-ttu-id="5157b-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="5157b-149">Requirement</span></span> | <span data-ttu-id="5157b-150">Value</span><span class="sxs-lookup"><span data-stu-id="5157b-150">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5157b-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5157b-151">DLL</span></span><br/> | <dl> <span data-ttu-id="5157b-152"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5157b-152"><dt>Msoobci.dll</dt></span></span> </dl> |



 

 
