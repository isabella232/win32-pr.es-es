---
description: Define los niveles de muestreo múltiple de la escena completa que el dispositivo puede aplicar.
ms.assetid: 1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8
title: Enumeración D3DMULTISAMPLE_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMULTISAMPLE_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: da8f9c1c8bb3aa74c0ab22a5cc701e7d835898de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362612"
---
# <a name="d3dmultisample_type-enumeration"></a><span data-ttu-id="20c20-103">\_Enumeración de tipo D3DMULTISAMPLE</span><span class="sxs-lookup"><span data-stu-id="20c20-103">D3DMULTISAMPLE\_TYPE enumeration</span></span>

<span data-ttu-id="20c20-104">Define los niveles de muestreo múltiple de la escena completa que el dispositivo puede aplicar.</span><span class="sxs-lookup"><span data-stu-id="20c20-104">Defines the levels of full-scene multisampling that the device can apply.</span></span>

## <a name="syntax"></a><span data-ttu-id="20c20-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20c20-105">Syntax</span></span>


```C++
typedef enum D3DMULTISAMPLE_TYPE { 
  D3DMULTISAMPLE_NONE          = 0,
  D3DMULTISAMPLE_NONMASKABLE   = 1,
  D3DMULTISAMPLE_2_SAMPLES     = 2,
  D3DMULTISAMPLE_3_SAMPLES     = 3,
  D3DMULTISAMPLE_4_SAMPLES     = 4,
  D3DMULTISAMPLE_5_SAMPLES     = 5,
  D3DMULTISAMPLE_6_SAMPLES     = 6,
  D3DMULTISAMPLE_7_SAMPLES     = 7,
  D3DMULTISAMPLE_8_SAMPLES     = 8,
  D3DMULTISAMPLE_9_SAMPLES     = 9,
  D3DMULTISAMPLE_10_SAMPLES    = 10,
  D3DMULTISAMPLE_11_SAMPLES    = 11,
  D3DMULTISAMPLE_12_SAMPLES    = 12,
  D3DMULTISAMPLE_13_SAMPLES    = 13,
  D3DMULTISAMPLE_14_SAMPLES    = 14,
  D3DMULTISAMPLE_15_SAMPLES    = 15,
  D3DMULTISAMPLE_16_SAMPLES    = 16,
  D3DMULTISAMPLE_FORCE_DWORD   = 0xffffffff
} D3DMULTISAMPLE_TYPE, *LPD3DMULTISAMPLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="20c20-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="20c20-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="20c20-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="20c20-107"><span id="D3DMULTISAMPLE_NONE"></span><span id="d3dmultisample_none"></span>**D3DMULTISAMPLE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-108">No hay disponible ningún nivel de muestreo múltiple de escenas completas.</span><span class="sxs-lookup"><span data-stu-id="20c20-108">No level of full-scene multisampling is available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE no \_ enmascarable**</span><span class="sxs-lookup"><span data-stu-id="20c20-109"><span id="D3DMULTISAMPLE_NONMASKABLE_"></span><span id="d3dmultisample_nonmaskable_"></span>**D3DMULTISAMPLE\_NONMASKABLE**</span></span> 
</dt> <dd>

<span data-ttu-id="20c20-110">Habilita el valor de calidad Multimuestra.</span><span class="sxs-lookup"><span data-stu-id="20c20-110">Enables the multisample quality value.</span></span> <span data-ttu-id="20c20-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="20c20-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 2 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-112"><span id="D3DMULTISAMPLE_2_SAMPLES"></span><span id="d3dmultisample_2_samples"></span>**D3DMULTISAMPLE\_2\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-113">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-113">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 3 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-114"><span id="D3DMULTISAMPLE_3_SAMPLES"></span><span id="d3dmultisample_3_samples"></span>**D3DMULTISAMPLE\_3\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-115">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-115">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 4 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-116"><span id="D3DMULTISAMPLE_4_SAMPLES"></span><span id="d3dmultisample_4_samples"></span>**D3DMULTISAMPLE\_4\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-117">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-117">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 5 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-118"><span id="D3DMULTISAMPLE_5_SAMPLES"></span><span id="d3dmultisample_5_samples"></span>**D3DMULTISAMPLE\_5\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-119">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-119">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 6 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-120"><span id="D3DMULTISAMPLE_6_SAMPLES"></span><span id="d3dmultisample_6_samples"></span>**D3DMULTISAMPLE\_6\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-121">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-121">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 7 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-122"><span id="D3DMULTISAMPLE_7_SAMPLES"></span><span id="d3dmultisample_7_samples"></span>**D3DMULTISAMPLE\_7\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-123">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-123">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 8 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-124"><span id="D3DMULTISAMPLE_8_SAMPLES"></span><span id="d3dmultisample_8_samples"></span>**D3DMULTISAMPLE\_8\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-125">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-125">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 9 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-126"><span id="D3DMULTISAMPLE_9_SAMPLES"></span><span id="d3dmultisample_9_samples"></span>**D3DMULTISAMPLE\_9\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-127">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-127">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 10 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-128"><span id="D3DMULTISAMPLE_10_SAMPLES"></span><span id="d3dmultisample_10_samples"></span>**D3DMULTISAMPLE\_10\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-129">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-129">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 11 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-130"><span id="D3DMULTISAMPLE_11_SAMPLES"></span><span id="d3dmultisample_11_samples"></span>**D3DMULTISAMPLE\_11\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-131">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-131">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 12 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-132"><span id="D3DMULTISAMPLE_12_SAMPLES"></span><span id="d3dmultisample_12_samples"></span>**D3DMULTISAMPLE\_12\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-133">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-133">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 13 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-134"><span id="D3DMULTISAMPLE_13_SAMPLES"></span><span id="d3dmultisample_13_samples"></span>**D3DMULTISAMPLE\_13\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-135">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-135">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 14 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-136"><span id="D3DMULTISAMPLE_14_SAMPLES"></span><span id="d3dmultisample_14_samples"></span>**D3DMULTISAMPLE\_14\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-137">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-137">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 15 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-138"><span id="D3DMULTISAMPLE_15_SAMPLES"></span><span id="d3dmultisample_15_samples"></span>**D3DMULTISAMPLE\_15\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-139">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-139">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**Ejemplos de D3DMULTISAMPLE \_ 16 \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-140"><span id="D3DMULTISAMPLE_16_SAMPLES"></span><span id="d3dmultisample_16_samples"></span>**D3DMULTISAMPLE\_16\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-141">Nivel de muestreo múltiple de la escena completa disponible.</span><span class="sxs-lookup"><span data-stu-id="20c20-141">Level of full-scene multisampling available.</span></span>

</dd> <dt>

<span data-ttu-id="20c20-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="20c20-142"><span id="D3DMULTISAMPLE_FORCE_DWORD"></span><span id="d3dmultisample_force_dword"></span>**D3DMULTISAMPLE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="20c20-143">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="20c20-143">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="20c20-144">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="20c20-144">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="20c20-145">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="20c20-145">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20c20-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20c20-146">Remarks</span></span>

<span data-ttu-id="20c20-147">Además de habilitar el muestreo múltiple de escena completa en [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) Time, habrá Estados de representación que activan y desactivan varios aspectos en los niveles específicos.</span><span class="sxs-lookup"><span data-stu-id="20c20-147">In addition to enabling full-scene multisampling at [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) time, there will be render states that turn various aspects on and off at fine-grained levels.</span></span>

<span data-ttu-id="20c20-148">El muestreo múltiple solo es válido en una cadena de intercambio que se va a crear o restablecer con el \_ efecto de intercambio descartar D3DSWAPEFFECT.</span><span class="sxs-lookup"><span data-stu-id="20c20-148">Multisampling is valid only on a swap chain that is being created or reset with the D3DSWAPEFFECT\_DISCARD swap effect.</span></span>

<span data-ttu-id="20c20-149">El valor de suavizado de contorno de muestreo múltiple se puede establecer con los parámetros (o subparámetros) en los métodos siguientes.</span><span class="sxs-lookup"><span data-stu-id="20c20-149">The multisample antialiasing value can be set with the parameters (or sub-parameters) in the following methods.</span></span>



| <span data-ttu-id="20c20-150">Método</span><span class="sxs-lookup"><span data-stu-id="20c20-150">Method</span></span>                                                                                             | <span data-ttu-id="20c20-151">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20c20-151">Parameters</span></span>                         | <span data-ttu-id="20c20-152">Subparámetros</span><span class="sxs-lookup"><span data-stu-id="20c20-152">Sub-parameters</span></span>                     |
|----------------------------------------------------------------------------------------------------|------------------------------------|------------------------------------|
| [<span data-ttu-id="20c20-153">**IDirect3D9::CheckDeviceMultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="20c20-153">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)           | <span data-ttu-id="20c20-154">MultiSampleType y pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="20c20-154">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="20c20-155">**IDirect3D9::CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="20c20-155">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)                                       | <span data-ttu-id="20c20-156">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="20c20-156">pPresentationParameters</span></span>            | <span data-ttu-id="20c20-157">MultiSampleType y pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="20c20-157">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="20c20-158">**IDirect3DDevice9::CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="20c20-158">**IDirect3DDevice9::CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) | <span data-ttu-id="20c20-159">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="20c20-159">pPresentationParameters</span></span>            | <span data-ttu-id="20c20-160">MultiSampleType y pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="20c20-160">MultiSampleType and pQualityLevels</span></span> |
| [<span data-ttu-id="20c20-161">**IDirect3DDevice9::CreateDepthStencilSurface**</span><span class="sxs-lookup"><span data-stu-id="20c20-161">**IDirect3DDevice9::CreateDepthStencilSurface**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) | <span data-ttu-id="20c20-162">MultiSampleType y pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="20c20-162">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="20c20-163">**IDirect3DDevice9::CreateRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="20c20-163">**IDirect3DDevice9::CreateRenderTarget**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)               | <span data-ttu-id="20c20-164">MultiSampleType y pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="20c20-164">MultiSampleType and pQualityLevels</span></span> |                                    |
| [<span data-ttu-id="20c20-165">**IDirect3DDevice9:: RESET**</span><span class="sxs-lookup"><span data-stu-id="20c20-165">**IDirect3DDevice9::Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)                                         | <span data-ttu-id="20c20-166">pPresentationParameters</span><span class="sxs-lookup"><span data-stu-id="20c20-166">pPresentationParameters</span></span>            | <span data-ttu-id="20c20-167">MultiSampleType y pQualityLevels</span><span class="sxs-lookup"><span data-stu-id="20c20-167">MultiSampleType and pQualityLevels</span></span> |



 

<span data-ttu-id="20c20-168">No es recomendable cambiar de un tipo Multimuestra a otro para aumentar la calidad del suavizado de contorno.</span><span class="sxs-lookup"><span data-stu-id="20c20-168">It is not good practice to switch from one multisample type to another to raise the quality of the antialiasing.</span></span>

<span data-ttu-id="20c20-169">D3DMULTISAMPLE \_ None habilita efectos de intercambio distintos de descartar, bloquear, etc.</span><span class="sxs-lookup"><span data-stu-id="20c20-169">D3DMULTISAMPLE\_NONE enables swap effects other than discarding, locking, and so on.</span></span>

<span data-ttu-id="20c20-170">Si el dispositivo de pantalla admite el muestreo múltiple enmascarable (más de un ejemplo para un formato de destino de representación de varios muestras más la compatibilidad con antialias) o simplemente un multimuestreo no enmascarable (solo compatibilidad con antialias), el controlador del dispositivo proporciona el número de niveles de calidad para el \_ tipo de muestra múltiple no enmascarable de D3DMULTISAMPLE.</span><span class="sxs-lookup"><span data-stu-id="20c20-170">Whether the display device supports maskable multisampling (more than one sample for a multiple-sample render-target format plus antialias support) or just non-maskable multisampling (only antialias support), the driver for the device provides the number of quality levels for the D3DMULTISAMPLE\_NONMASKABLE multiple-sample type.</span></span> <span data-ttu-id="20c20-171">Las aplicaciones que solo usan el multimuestreo para el suavizado de contorno solo necesitan consultar el número de niveles de calidad de muestreo múltiple no enmascarable que admite el controlador.</span><span class="sxs-lookup"><span data-stu-id="20c20-171">Applications that just use multisampling for antialiasing purposes only need to query for the number of non-maskable multiple-sample quality levels that the driver supports.</span></span>

<span data-ttu-id="20c20-172">Los niveles de calidad admitidos por el dispositivo se pueden obtener con el parámetro pQualityLevels de [**IDirect3D9:: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span><span class="sxs-lookup"><span data-stu-id="20c20-172">The quality levels supported by the device can be obtained with the pQualityLevels parameter of [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="20c20-173">Los niveles de calidad usados por la aplicación se establecen con el parámetro MultiSampleQuality de [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) y [**IDirect3DDevice9:: CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span><span class="sxs-lookup"><span data-stu-id="20c20-173">Quality levels used by the application are set with the MultiSampleQuality parameter of [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) and [**IDirect3DDevice9::CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget).</span></span>

<span data-ttu-id="20c20-174">Consulte D3DRS \_ MULTISAMPLEMASK para obtener información sobre el muestreo múltiple enmascarable.</span><span class="sxs-lookup"><span data-stu-id="20c20-174">See D3DRS\_MULTISAMPLEMASK for discussion of maskable multisampling.</span></span>

## <a name="requirements"></a><span data-ttu-id="20c20-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20c20-175">Requirements</span></span>



| <span data-ttu-id="20c20-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="20c20-176">Requirement</span></span> | <span data-ttu-id="20c20-177">Value</span><span class="sxs-lookup"><span data-stu-id="20c20-177">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20c20-178">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20c20-178">Header</span></span><br/> | <dl> <span data-ttu-id="20c20-179"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="20c20-179"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20c20-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="20c20-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20c20-181">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="20c20-181">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="20c20-182">**Parámetros de D3DPRESENT \_**</span><span class="sxs-lookup"><span data-stu-id="20c20-182">**D3DPRESENT\_PARAMETERS**</span></span>](d3dpresent-parameters.md)
</dt> <dt>

[<span data-ttu-id="20c20-183">**D3DSURFACE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="20c20-183">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> </dl>

 

 
