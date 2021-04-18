---
description: Valores HRESULT personalizados para la interfaz de captura de diagnóstico de gráficos.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración HRESULT
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3d5419feb0acb5967132fbb804a9bbc11bfa4248
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537329"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span data-ttu-id="5fbaf-103"><span id="vspixengine.hresult"></span>Enumeración HRESULT</span><span class="sxs-lookup"><span data-stu-id="5fbaf-103"><span id="vspixengine.hresult"></span>Hresult enumeration</span></span>

<span data-ttu-id="5fbaf-104">Valores HRESULT personalizados para la interfaz de captura de diagnóstico de gráficos.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-104">Custom HRESULT values for the graphics diagnostics capture interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fbaf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5fbaf-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="5fbaf-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="5fbaf-106">Constants</span></span>

<span data-ttu-id="5fbaf-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX\_S\_OK**</span></span>  
<span data-ttu-id="5fbaf-108">HRESULT común que indica que la operación se realizó correctamente según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-108">A common HRESULT which indicates that the operation succeeded as expected.</span></span>

<span data-ttu-id="5fbaf-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ false**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX\_S\_FALSE**</span></span>  
<span data-ttu-id="5fbaf-110">HRESULT común que indica que la operación se realizó correctamente, pero de forma diferente a lo esperado.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-110">A common HRESULT which indicates that the operation succeeded, but in a different way than was expected.</span></span>

<span data-ttu-id="5fbaf-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**\_ \_ \_ no \_ se encontró el archivo de error PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**PIX\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="5fbaf-112">Un valor HRESULT personalizado que \_ \_ no se encontró el archivo de error transmite \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-112">A custom HRESULT that echos ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="5fbaf-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**ERROR de PIX en el \_ \_ \_ entorno incorrecto**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**PIX\_ERROR\_BAD\_ENVIRONMENT**</span></span>  
<span data-ttu-id="5fbaf-114">Un valor HRESULT personalizado que transmite un ERROR de \_ \_ entorno incorrecto.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-114">A custom HRESULT that echos ERROR\_BAD\_ENVIRONMENT.</span></span>

<span data-ttu-id="5fbaf-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**\_error de \_ PIX \_ formato incorrecto**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**PIX\_ERROR\_BAD\_FORMAT**</span></span>  
<span data-ttu-id="5fbaf-116">Un valor HRESULT personalizado que transmite el formato de ERROR no es \_ correcto \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-116">A custom HRESULT that echos ERROR\_BAD\_FORMAT.</span></span>

<span data-ttu-id="5fbaf-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**infracción de \_ \_ uso compartido de errores de PIX \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**PIX\_ERROR\_SHARING\_VIOLATION**</span></span>  
<span data-ttu-id="5fbaf-118">Un valor HRESULT personalizado que transmite \_ infracción de uso compartido de errores \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-118">A custom HRESULT that echos ERROR\_SHARING\_VIOLATION.</span></span>

<span data-ttu-id="5fbaf-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**ERROR de PIX en el \_ \_ disco \_ lleno**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**PIX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="5fbaf-120">Un valor HRESULT personalizado que transmite el disco de ERROR \_ \_ completo.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-120">A custom HRESULT that echos ERROR\_DISK\_FULL.</span></span>

<span data-ttu-id="5fbaf-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**ERROR de PIX \_ : \_ más \_ datos**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**PIX\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="5fbaf-122">Un valor HRESULT personalizado que transmite errores \_ más \_ datos.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-122">A custom HRESULT that echos ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="5fbaf-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**\_no se \_ encuentra \_ la \_ Directiva del kit de depuración \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**PIX\_E\_MISSING\_DEBUG\_KITS\_POLICY**</span></span>  
<span data-ttu-id="5fbaf-124">Un valor HRESULT personalizado que indica que falta la Directiva del kit de depuración.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-124">A custom HRESULT which indicates that the Debug Kits policy is missing.</span></span>

<span data-ttu-id="5fbaf-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX \_ E \_ versión no válida \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX\_E\_INVALID\_VERSION**</span></span>  
<span data-ttu-id="5fbaf-126">Un valor HRESULT personalizado que indica que se está usando una versión no válida.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-126">A custom HRESULT which indicates that an invalid version is being used.</span></span>

<span data-ttu-id="5fbaf-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX \_ E \_ mediante \_ DCOMP**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX\_E\_USING\_DCOMP**</span></span>  
<span data-ttu-id="5fbaf-128">Un HRESULT personalizado que indica que DirectComposition está en uso (no se admite la captura de DirectComposition).</span><span class="sxs-lookup"><span data-stu-id="5fbaf-128">A custom HRESULT which indicates that DirectComposition is in use (capture of DirectComposition is not supported.)</span></span>

<span data-ttu-id="5fbaf-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX \_ E \_ con \_ DIRECTWRITE**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX\_E\_USING\_DIRECTWRITE**</span></span>  
<span data-ttu-id="5fbaf-130">Un valor HRESULT personalizado que indica que se está usando DirectWrite (no se admite la captura de DirectWrite).</span><span class="sxs-lookup"><span data-stu-id="5fbaf-130">A custom HRESULT which indicates that DirectWrite is in use (capture of DirectWrite is not supported.)</span></span>

<span data-ttu-id="5fbaf-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX \_ E \_ mediante \_ D3D9**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX\_E\_USING\_D3D9**</span></span>  
<span data-ttu-id="5fbaf-132">Un HRESULT personalizado que indica que Direct3D9 está en uso (la captura de Direct3D9 no se admite en Windows 10).</span><span class="sxs-lookup"><span data-stu-id="5fbaf-132">A custom HRESULT which indicates that Direct3D9 is in use (capture of Direct3D9 is not supported in Windows 10.)</span></span>

<span data-ttu-id="5fbaf-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX \_ E no se \_ \_ crean \_ sombreador**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX\_E\_CANT\_CREATE\_SHADER**</span></span>  
<span data-ttu-id="5fbaf-134">Un valor HRESULT personalizado que indica que no se puede crear un sombreador especificado.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-134">A custom HRESULT which indicates that a specified shader can't be created.</span></span>

<span data-ttu-id="5fbaf-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX \_ E \_ mediante \_ D2D**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX\_E\_USING\_D2D**</span></span>  
<span data-ttu-id="5fbaf-136">Un HRESULT personalizado que indica que Direct2D está en uso (no se admite la captura de Direct2D).</span><span class="sxs-lookup"><span data-stu-id="5fbaf-136">A custom HRESULT which indicates that Direct2D is in use (capture of Direct2D is not supported.)</span></span>

<span data-ttu-id="5fbaf-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**fotogramas de foto \_ E \_ no \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX\_E\_NO\_FRAMES**</span></span>  
<span data-ttu-id="5fbaf-138">Un valor HRESULT personalizado que indica que no se ha capturado ningún fotograma.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-138">A custom HRESULT which indicates that no frames have been captured.</span></span>

<span data-ttu-id="5fbaf-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ deshabilitar \_ Spy**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX\_E\_DISABLE\_SPY**</span></span>  

<span data-ttu-id="5fbaf-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX \_ E \_ WIN8LOG \_ en \_ win7**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX\_E\_WIN8LOG\_ON\_WIN7**</span></span>  
<span data-ttu-id="5fbaf-141">Un HRESULT personalizado que indica que no se puede reproducir un vsglog de Windows 8 en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-141">A custom HRESULT which indicates that a Windows 8 vsglog cannot be played back on Windows 7.</span></span>

<span data-ttu-id="5fbaf-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**\_seguimiento del \_ \_ sombreador de \_ compilación de PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**PIX\_E\_BUILD\_SHADER\_TRACE**</span></span>  
<span data-ttu-id="5fbaf-143">Un valor HRESULT personalizado que indica que se produjo un error al generar el seguimiento del sombreador.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-143">A custom HRESULT which indicates that there was an error building the shader trace.</span></span>

<span data-ttu-id="5fbaf-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**visualización de datos de PIX \_ E \_ no \_ CS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX\_E\_NO\_CS\_DATA\_VISUALIZATION**</span></span>  
<span data-ttu-id="5fbaf-145">Un HRESULT personalizado que indica que no hay ninguna visualización de datos del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-145">A custom HRESULT which indicates that there is no compute shader data visualization.</span></span>

<span data-ttu-id="5fbaf-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**\_SDK de \_ no coincidencia \_ de PIX E**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**PIX\_E\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="5fbaf-147">Un valor HRESULT personalizado que indica que hay una falta de coincidencia con el SDK actual.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-147">A custom HRESULT which indicates that there is a mismatch with the current SDK.</span></span>

<span data-ttu-id="5fbaf-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**\_SDK de \_ \_ coincidencia posible \_ de PIX E**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**PIX\_E\_POSSIBLE\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="5fbaf-149">Un valor HRESULT personalizado que indica que hay una posible falta de coincidencia con el SDK actual.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-149">A custom HRESULT which indicates that there is a possible mismatch with the current SDK.</span></span>

<span data-ttu-id="5fbaf-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**\_ \_ píxel indetectable de \_ PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIX\_E\_UNDETECTABLE\_PIXEL**</span></span>  
<span data-ttu-id="5fbaf-151">Un valor HRESULT personalizado que indica que hay un píxel no detectable.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-151">A custom HRESULT which indicates that there is an undetectable pixel.</span></span>

<span data-ttu-id="5fbaf-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX E no se pudo \_ \_ \_ depurar \_ sombreador \_ mediante la semántica de \_ valores del sistema \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX\_E\_CANT\_DEBUG\_SHADER\_USING\_SYSTEM\_VALUE\_SEMANTICS**</span></span>  
<span data-ttu-id="5fbaf-153">Un HRESULT personalizado que indica que sahder no se puede depurar utilizando la semántica del valor del sistema.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-153">A custom HRESULT which indicates that the sahder can't be debugged using system value semantics.</span></span>

<span data-ttu-id="5fbaf-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX \_ S \_ UPDATEAVAILABLE**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX\_S\_UPDATEAVAILABLE**</span></span>  
<span data-ttu-id="5fbaf-155">Un valor HRESULT personalizado que indica que hay una actualización disponible.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-155">A custom HRESULT which indicates that there is an update available.</span></span>

<span data-ttu-id="5fbaf-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**Estado de DXGI de PIX \_ \_ \_ sin \_ redireccionamiento**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**PIX\_DXGI\_STATUS\_NO\_REDIRECTION**</span></span>  
<span data-ttu-id="5fbaf-157">Un valor HRESULT personalizado que transmite el estado de DXGI \_ \_ no \_ redirección.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-157">A custom HRESULT that echos DXGI\_STATUS\_NO\_REDIRECTION.</span></span>

<span data-ttu-id="5fbaf-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**Estado de foto de PIX \_ \_ \_ no \_ \_ acceso al escritorio**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**PIX\_DXGI\_STATUS\_NO\_DESKTOP\_ACCESS**</span></span>  
<span data-ttu-id="5fbaf-159">Un valor HRESULT personalizado que transmite el estado de DXGI \_ \_ sin \_ \_ acceso al escritorio.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-159">A custom HRESULT that echos DXGI\_STATUS\_NO\_DESKTOP\_ACCESS.</span></span>

<span data-ttu-id="5fbaf-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ \_ código fuente VIDPN \_ de gráficos de estado de \_ la foto**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="5fbaf-161">Un valor HRESULT personalizado que transmite \_ el \_ \_ \_ origen de VIDPN \_ de gráficos de estado de DXGI en \_ uso.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-161">A custom HRESULT that echos DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="5fbaf-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**modo de estado de \_ DXGI \_ \_ \_ cambiado**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGED**</span></span>  
<span data-ttu-id="5fbaf-163">Un valor HRESULT personalizado que cambió el modo de estado de transmite DXGI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-163">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGED.</span></span>

<span data-ttu-id="5fbaf-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ \_ cambio en el modo \_ de estado de DXGI de PIX \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="5fbaf-165">Un valor HRESULT personalizado que \_ cambia el \_ modo \_ de estado de transmite DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-165">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="5fbaf-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**\_UNOCCLUDED de \_ Estado de la foto de PIX \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**PIX\_DXGI\_STATUS\_UNOCCLUDED**</span></span>  
<span data-ttu-id="5fbaf-167">Un valor HRESULT personalizado que transmite \_ UNOCCLUDED de estado de DXGI \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-167">A custom HRESULT that echos DXGI\_STATUS\_UNOCCLUDED.</span></span>

<span data-ttu-id="5fbaf-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**error de la DDA de estado de la \_ \_ imagen de \_ \_ \_ \_ dibujo**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**PIX\_DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="5fbaf-169">Un valor HRESULT personalizado que transmite de estado de DXGI \_ \_ \_ \_ todavía estaba \_ dibujando.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-169">A custom HRESULT that echos DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="5fbaf-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX \_ E \_ NOTIMPL**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX\_E\_NOTIMPL**</span></span>  
<span data-ttu-id="5fbaf-171">Un valor HRESULT personalizado que transmite E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-171">A custom HRESULT that echos E\_NOTIMPL.</span></span>

<span data-ttu-id="5fbaf-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX \_ E \_ nointerface**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX\_E\_NOINTERFACE**</span></span>  
<span data-ttu-id="5fbaf-173">Un valor HRESULT personalizado que transmite E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-173">A custom HRESULT that echos E\_NOINTERFACE.</span></span>

<span data-ttu-id="5fbaf-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**\_cursor PIX E \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**PIX\_E\_POINTER**</span></span>  
<span data-ttu-id="5fbaf-175">Un valor HRESULT personalizado que transmite \_ puntero E.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-175">A custom HRESULT that echos E\_POINTER.</span></span>

<span data-ttu-id="5fbaf-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX \_ E \_ Abort**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX\_E\_ABORT**</span></span>  
<span data-ttu-id="5fbaf-177">Un valor HRESULT personalizado que transmite E \_ anula.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-177">A custom HRESULT that echos E\_ABORT.</span></span>

<span data-ttu-id="5fbaf-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX \_ E \_ FAIL**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX\_E\_FAIL**</span></span>  
<span data-ttu-id="5fbaf-179">Un valor HRESULT personalizado que transmite E \_ produce un error.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-179">A custom HRESULT that echos E\_FAIL.</span></span>

<span data-ttu-id="5fbaf-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX \_ E \_ inesperado**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX\_E\_UNEXPECTED**</span></span>  
<span data-ttu-id="5fbaf-181">Un valor HRESULT personalizado que transmite E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-181">A custom HRESULT that echos E\_UNEXPECTED.</span></span>

<span data-ttu-id="5fbaf-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX \_ E \_ ACCESSDENIED**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX\_E\_ACCESSDENIED**</span></span>  
<span data-ttu-id="5fbaf-183">Un valor HRESULT personalizado que transmite E \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-183">A custom HRESULT that echos E\_ACCESSDENIED.</span></span>

<span data-ttu-id="5fbaf-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**identificador de PIX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**PIX\_E\_HANDLE**</span></span>  
<span data-ttu-id="5fbaf-185">Un valor HRESULT personalizado que transmite \_ identificador E.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-185">A custom HRESULT that echos E\_HANDLE.</span></span>

<span data-ttu-id="5fbaf-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX \_ E \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX\_E\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="5fbaf-187">Un valor HRESULT personalizado que transmite E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-187">A custom HRESULT that echos E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="5fbaf-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX\_E\_INVALIDARG**</span></span>  
<span data-ttu-id="5fbaf-189">Un valor HRESULT personalizado que transmite E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-189">A custom HRESULT that echos E\_INVALIDARG.</span></span>

<span data-ttu-id="5fbaf-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**disco de error de la \_ Xbox PIX \_ \_ \_ lleno**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**PIX\_XBOX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="5fbaf-191">Un valor HRESULT personalizado que indica que el disco está lleno.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-191">A custom HRESULT which indicates that the disk is full.</span></span>

<span data-ttu-id="5fbaf-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_Dirección WS \_ E \_ \_ de PIX en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**PIX\_WS\_E\_ADDRESS\_IN\_USE**</span></span>  
<span data-ttu-id="5fbaf-193">Un valor HRESULT personalizado que indica que la dirección ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-193">A custom HRESULT which indicates that the address is already in use.</span></span>

<span data-ttu-id="5fbaf-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**\_Directiva de \_ \_ kits que faltan de \_ PIX WS E \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**PIX\_WS\_E\_MISSING\_KITS\_POLICY**</span></span>  
<span data-ttu-id="5fbaf-195">Un valor HRESULT personalizado que indica que la dirección no está disponible.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-195">A custom HRESULT which indicates that the address is not available.</span></span>

<span data-ttu-id="5fbaf-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX \_ te \_ FAILEDTOLOADSOFTWAREMODULE**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX\_TE\_FAILEDTOLOADSOFTWAREMODULE**</span></span>  
<span data-ttu-id="5fbaf-197">Un valor HRESULT personalizado que indica que no se pudo cargar un módulo de software necesario.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-197">A custom HRESULT which indicates that a necessary software module failed to load.</span></span>

<span data-ttu-id="5fbaf-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX \_ te \_ USEDSOFTWAREMODULETHATWASNTWARPORREF**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX\_TE\_USEDSOFTWAREMODULETHATWASNTWARPORREF**</span></span>  
<span data-ttu-id="5fbaf-199">Un valor HRESULT personalizado que indica que el módulo de software usado no era el controlador de ALABEo o REF.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-199">A custom HRESULT which indicates that the used software module was not the WARP or REF driver.</span></span>

<span data-ttu-id="5fbaf-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX \_ te \_ CORRUPTEDFILE**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX\_TE\_CORRUPTEDFILE**</span></span>  
<span data-ttu-id="5fbaf-201">Un valor HRESULT personalizado que indica que el archivo está dañado.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-201">A custom HRESULT which indicates that the file is corrupted.</span></span>

<span data-ttu-id="5fbaf-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX \_ te \_ FAILEDTOOPENFILE**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX\_TE\_FAILEDTOOPENFILE**</span></span>  
<span data-ttu-id="5fbaf-203">Un valor HRESULT personalizado que indica que no se pudo abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-203">A custom HRESULT which indicates that the file failed to open.</span></span>

<span data-ttu-id="5fbaf-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX \_ te \_ CALLFAILEDONPLAYBACK**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX\_TE\_CALLFAILEDONPLAYBACK**</span></span>  
<span data-ttu-id="5fbaf-205">Un HRESULT personalizado que indica que se produjo un error en una llamada durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-205">A custom HRESULT which indicates that a call failed during playback.</span></span>

<span data-ttu-id="5fbaf-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX \_ te \_ UNKNOWNUUID**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX\_TE\_UNKNOWNUUID**</span></span>  
<span data-ttu-id="5fbaf-207">HRESULT personalizado que indica que se encontró un UUID desconocido; nunca se debe producir.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-207">A custom HRESULT which indicates that an unknown UUID was encountered; this should never occur.</span></span>

<span data-ttu-id="5fbaf-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX \_ te \_ NOTCAPTUREFILEORCORRUPTED**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX\_TE\_NOTCAPTUREFILEORCORRUPTED**</span></span>  
<span data-ttu-id="5fbaf-209">Un valor HRESULT personalizado que indica que el archivo no es un archivo de captura o está dañado.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-209">A custom HRESULT which indicates that the file is not a capture file or is corrupted.</span></span>

<span data-ttu-id="5fbaf-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX \_ te \_ NEWERFILE**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX\_TE\_NEWERFILE**</span></span>  

<span data-ttu-id="5fbaf-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX \_ te \_ OLDERFILE**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX\_TE\_OLDERFILE**</span></span>  

<span data-ttu-id="5fbaf-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX \_ te \_ INVALIDMOMENT**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX\_TE\_INVALIDMOMENT**</span></span>  

<span data-ttu-id="5fbaf-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**\_ \_ controlador incorrecto de \_ PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**PIX\_TE\_BAD\_DRIVER**</span></span>  
<span data-ttu-id="5fbaf-214">Un valor HRESULT personalizado que indica que el controlador es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-214">A custom HRESULT which indicates that the driver is bad.</span></span>

<span data-ttu-id="5fbaf-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**ERROR de PIX no se \_ \_ \_ puede acceder a \_ DEPTHSTENCIL \_ en la \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**PIX\_ERROR\_CANT\_ACCESS\_DEPTHSTENCIL\_IN\_CPU**</span></span>  
<span data-ttu-id="5fbaf-216">Un HRESULT personalizado que indica que la CPU intentó tener acceso al búfer de la galería de símbolos de profundidad, lo que produce un error.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-216">A custom HRESULT which indicates that the CPU attempted to access the depth-stencil buffer, resulting in an error.</span></span>

<span data-ttu-id="5fbaf-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**ERROR de PIX no se resuelve la textura de múltiples \_ \_ \_ \_ muestras \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**PIX\_ERROR\_CANT\_RESOLVE\_MULTISAMPLED\_TEXTURE**</span></span>  
<span data-ttu-id="5fbaf-218">Un valor HRESULT personalizado que indica que se ha intentado resolver una textura con varias muestras, lo que produce un error.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-218">A custom HRESULT which indicates that there was an attempt to resolve a multi-sampled texture, resulting in an error.</span></span>

<span data-ttu-id="5fbaf-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**\_error de \_ la \_ llamada no válida \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**PIX\_DXGI\_ERROR\_INVALID\_CALL**</span></span>  
<span data-ttu-id="5fbaf-220">Un valor HRESULT personalizado que transmite \_ DXGI \_ no pudo \_ llamar a.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-220">A custom HRESULT that echos DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="5fbaf-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**\_error de \_ fotostat de PIX \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**PIX\_DXGI\_ERROR\_NOT\_FOUND**</span></span>  
<span data-ttu-id="5fbaf-222">Un valor HRESULT personalizado que \_ \_ no \_ se encontró transmite DXGI.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-222">A custom HRESULT that echos DXGI\_ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="5fbaf-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**\_ \_ \_ más datos de error de DXGI de PIX \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**PIX\_DXGI\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="5fbaf-224">Un valor HRESULT personalizado que transmite DXGI tiene \_ \_ más \_ datos.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-224">A custom HRESULT that echos DXGI\_ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="5fbaf-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**ERROR de la DXGI de PIX \_ \_ \_ no compatible**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**PIX\_DXGI\_ERROR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="5fbaf-226">Un valor HRESULT personalizado que \_ no es \_ compatible con transmite DXGI.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-226">A custom HRESULT that echos DXGI\_ERROR\_UNSUPPORTED.</span></span>

<span data-ttu-id="5fbaf-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**se \_ \_ \_ quitó el dispositivo de error de de PIX \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**PIX\_DXGI\_ERROR\_DEVICE\_REMOVED**</span></span>  
<span data-ttu-id="5fbaf-228">Un valor HRESULT personalizado que el dispositivo de error de transmite DXGI \_ \_ \_ quitó.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-228">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_REMOVED.</span></span>

<span data-ttu-id="5fbaf-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**\_error de \_ dispositivo de error de DXGI de PIX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**PIX\_DXGI\_ERROR\_DEVICE\_HUNG**</span></span>  
<span data-ttu-id="5fbaf-230">Un valor HRESULT personalizado que el dispositivo de error de transmite DXGI ha dejado de estar \_ \_ \_ bloqueado.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-230">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_HUNG.</span></span>

<span data-ttu-id="5fbaf-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**\_restablecimiento del \_ dispositivo de error de DXGI de PIX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**PIX\_DXGI\_ERROR\_DEVICE\_RESET**</span></span>  
<span data-ttu-id="5fbaf-232">Un valor HRESULT personalizado que transmite el dispositivo de error de DXGI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-232">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_RESET.</span></span>

<span data-ttu-id="5fbaf-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**el \_ error de DXGI de PIX \_ \_ todavía se está \_ \_ dibujando**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**PIX\_DXGI\_ERROR\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="5fbaf-234">Un valor HRESULT personalizado que el error de transmite DXGI \_ \_ \_ todavía estaba \_ dibujando.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-234">A custom HRESULT that echos DXGI\_ERROR\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="5fbaf-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**\_estadísticas de \_ \_ fotogramas de error de fotogramas de \_ \_ PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**PIX\_DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT**</span></span>  
<span data-ttu-id="5fbaf-236">HRESULT personalizado que transmite las \_ estadísticas de \_ fotogramas de errores de DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-236">A custom HRESULT that echos DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT.</span></span>

<span data-ttu-id="5fbaf-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ gráficos de errores de fotográficos \_ VIDPN \_ de PIX \_ en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="5fbaf-238">Un valor HRESULT personalizado que transmite \_ el \_ \_ \_ origen de VIDPN \_ de gráficos de error de DXGI en \_ uso.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-238">A custom HRESULT that echos DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="5fbaf-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_ \_ \_ error interno del controlador de errores \_ de \_ PIX de PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**PIX\_DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR**</span></span>  
<span data-ttu-id="5fbaf-240">Un valor HRESULT personalizado que transmite error interno del controlador de errores de DXGI \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-240">A custom HRESULT that echos DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR.</span></span>

<span data-ttu-id="5fbaf-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**ERROR de DXGI de PIX no \_ \_ \_ exclusivo**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**PIX\_DXGI\_ERROR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="5fbaf-242">Un valor HRESULT personalizado que transmite DXGI no es \_ \_ exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-242">A custom HRESULT that echos DXGI\_ERROR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="5fbaf-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**ERROR de DXGI de PIX \_ \_ \_ no \_ \_ disponible actualmente**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**PIX\_DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE**</span></span>  
<span data-ttu-id="5fbaf-244">Un valor HRESULT personalizado que transmite \_ DXGI \_ no \_ tiene \_ disponible actualmente.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-244">A custom HRESULT that echos DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE.</span></span>

<span data-ttu-id="5fbaf-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**mensaje de error de DXGI de PIX \_ \_ \_ \_ \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**PIX\_DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED**</span></span>  
<span data-ttu-id="5fbaf-246">Un valor HRESULT personalizado que transmite de error de DXGI \_ \_ \_ \_ desconectó el cliente.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-246">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED.</span></span>

<span data-ttu-id="5fbaf-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**\_error de \_ \_ OUTOFMEMORY remoto \_ de la de PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**PIX\_DXGI\_ERROR\_REMOTE\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="5fbaf-248">Un valor HRESULT personalizado que transmite de error de DXGI \_ \_ \_ OUTOFMEMORY remoto.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-248">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_OUTOFMEMORY.</span></span>

<span data-ttu-id="5fbaf-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**\_ \_ \_ cambio en el modo \_ de error de DXGI \_ de \_ PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**PIX\_DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="5fbaf-250">Un valor HRESULT personalizado que \_ \_ \_ cambia \_ en curso el modo de error de \_ transmite DXGI.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-250">A custom HRESULT that echos DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="5fbaf-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**\_error de \_ \_ acceso \_ de la DXGI de PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**PIX\_DXGI\_ERROR\_ACCESS\_LOST**</span></span>  
<span data-ttu-id="5fbaf-252">Un valor HRESULT personalizado que ha perdido el acceso de error de transmite DXGI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-252">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_LOST.</span></span>

<span data-ttu-id="5fbaf-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**\_tiempo de \_ espera de error \_ \_ de**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**PIX\_DXGI\_ERROR\_WAIT\_TIMEOUT**</span></span>  
<span data-ttu-id="5fbaf-254">Un valor HRESULT personalizado que transmite el tiempo de espera de error de DXGI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-254">A custom HRESULT that echos DXGI\_ERROR\_WAIT\_TIMEOUT.</span></span>

<span data-ttu-id="5fbaf-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**sesión de errores de DXGI de PIX \_ \_ \_ \_ desconectada**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**PIX\_DXGI\_ERROR\_SESSION\_DISCONNECTED**</span></span>  
<span data-ttu-id="5fbaf-256">Un valor HRESULT personalizado que desconectó la sesión de error de transmite DXGI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-256">A custom HRESULT that echos DXGI\_ERROR\_SESSION\_DISCONNECTED.</span></span>

<span data-ttu-id="5fbaf-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**\_ \_ error de DXGI \_ de PIX restringido \_ a \_ salida \_ obsoleta**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**PIX\_DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE**</span></span>  
<span data-ttu-id="5fbaf-258">Un valor HRESULT personalizado que transmite \_ error \_ de DXGI restringido \_ a la \_ salida \_ obsoleta.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-258">A custom HRESULT that echos DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE.</span></span>

<span data-ttu-id="5fbaf-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**el \_ error de DXGI de PIX \_ \_ no puede \_ proteger el \_ contenido**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**PIX\_DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT**</span></span>  
<span data-ttu-id="5fbaf-260">Un valor HRESULT personalizado que transmite \_ error de DXGI \_ no puede \_ proteger el \_ contenido.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-260">A custom HRESULT that echos DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT.</span></span>

<span data-ttu-id="5fbaf-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**\_error de \_ \_ acceso \_ denegado de DXGI de PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**PIX\_DXGI\_ERROR\_ACCESS\_DENIED**</span></span>  
<span data-ttu-id="5fbaf-262">Un valor HRESULT personalizado que \_ denegó transmite error de acceso de DXGI \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-262">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="5fbaf-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**\_ \_ \_ \_ ya existe un nombre de error de la DXGI de PIX \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**PIX\_DXGI\_ERROR\_NAME\_ALREADY\_EXISTS**</span></span>  
<span data-ttu-id="5fbaf-264">Ya existe un HRESULT personalizado que transmite nombre de error de DXGI \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-264">A custom HRESULT that echos DXGI\_ERROR\_NAME\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="5fbaf-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**\_falta el \_ componente del SDK de errores \_ \_ de PIX \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**PIX\_DXGI\_ERROR\_SDK\_COMPONENT\_MISSING**</span></span>  
<span data-ttu-id="5fbaf-266">Un valor HRESULT personalizado que no transmite el \_ componente SDK de error de DXGI \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-266">A custom HRESULT that echos DXGI\_ERROR\_SDK\_COMPONENT\_MISSING.</span></span>

<span data-ttu-id="5fbaf-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**\_error de \_ DDI \_ \_ WASSTILLDRAWING de PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**PIX\_DXGI\_DDI\_ERR\_WASSTILLDRAWING**</span></span>  
<span data-ttu-id="5fbaf-268">Un valor HRESULT personalizado que transmite DXGI \_ DDI \_ Err \_ WASSTILLDRAWING.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-268">A custom HRESULT that echos DXGI\_DDI\_ERR\_WASSTILLDRAWING.</span></span>

<span data-ttu-id="5fbaf-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**error de DDI de foto de PIX \_ \_ \_ \_ no compatible**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**PIX\_DXGI\_DDI\_ERR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="5fbaf-270">Un valor HRESULT personalizado que transmite DXGI \_ DDI \_ Err no era \_ compatible.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-270">A custom HRESULT that echos DXGI\_DDI\_ERR\_UNSUPPORTED.</span></span>

<span data-ttu-id="5fbaf-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**\_error de \_ DDI \_ de \_ modo de foto de PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**PIX\_DXGI\_DDI\_ERR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="5fbaf-272">Un valor HRESULT personalizado que transmite DXGI \_ DDI \_ Err no \_ exclusivo.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-272">A custom HRESULT that echos DXGI\_DDI\_ERR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="5fbaf-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**PIX \_ D3D10 \_ error \_ demasiados \_ \_ \_ objetos de estado único \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**PIX\_D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="5fbaf-274">Un valor HRESULT personalizado que transmite D3D10 \_ error \_ demasiado \_ numerosos objetos de \_ \_ Estado único \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-274">A custom HRESULT that echos D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="5fbaf-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_ \_ \_ \_ No se encontró el archivo \_ de error D3D10 PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**PIX\_D3D10\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="5fbaf-276">Un valor HRESULT personalizado que \_ \_ \_ no \_ se encontró en el archivo de error de transmite D3D10.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-276">A custom HRESULT that echos D3D10\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="5fbaf-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**PIX \_ D3D11 \_ error \_ demasiados \_ \_ \_ objetos de estado único \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="5fbaf-278">Un valor HRESULT personalizado que transmite D3D11 \_ error \_ demasiado \_ numerosos objetos de \_ \_ Estado único \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-278">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="5fbaf-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_ \_ \_ \_ No se encontró el archivo \_ de error D3D11 PIX**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**PIX\_D3D11\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="5fbaf-280">Un valor HRESULT personalizado que \_ \_ \_ no \_ se encontró en el archivo de error de transmite D3D11.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-280">A custom HRESULT that echos D3D11\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="5fbaf-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**PIX \_ D3D11 \_ error \_ demasiados \_ \_ \_ objetos de vista únicos \_**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS**</span></span>  
<span data-ttu-id="5fbaf-282">Un valor HRESULT personalizado que transmite D3D11 \_ error \_ demasiado \_ numerosos objetos de \_ \_ vista únicos \_ .</span><span class="sxs-lookup"><span data-stu-id="5fbaf-282">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS.</span></span>

<span data-ttu-id="5fbaf-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**ERROR de D3D11 de PIX en la \_ \_ asignación de \_ \_ contexto \_ \_ sin \_ \_ descartar inicial**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**PIX\_D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD**</span></span>  
<span data-ttu-id="5fbaf-284">Un valor HRESULT personalizado que transmite D3D11 \_ error \_ diferido de asignación de \_ contexto \_ \_ sin \_ \_ descartar inicial.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-284">A custom HRESULT that echos D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD.</span></span>

<span data-ttu-id="5fbaf-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**ERROR de PIX \_ \_ ocluidos \_ \_ llamada a Draw**</span><span class="sxs-lookup"><span data-stu-id="5fbaf-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**PIX\_ERROR\_OCCLUDED\_DRAW\_CALL**</span></span>  
<span data-ttu-id="5fbaf-286">Un HRESULT personalizado que indica que una llamada a Draw fue completamente ocluidos, lo que produjo un error.</span><span class="sxs-lookup"><span data-stu-id="5fbaf-286">A custom HRESULT which indicates that a draw call was entirely occluded, resulting in an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fbaf-287">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fbaf-287">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5fbaf-288">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fbaf-288">Header</span></span></p></td><td><span data-ttu-id="5fbaf-289">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5fbaf-289">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



