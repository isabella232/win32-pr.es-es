---
description: La API de Direct3D 9 funciona en el modelo de controladores de pantalla de Windows XP (XPDM) o en el modelo de controladores de pantalla (WDDM) de Windows Vista, dependiendo del sistema operativo instalado.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM frente a WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdf4bba28b53959d8e86d8928c786db3b1d0c7f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686284"
---
# <a name="xpdm-vs-wddm"></a><span data-ttu-id="36a8b-103">XPDM frente a WDDM</span><span class="sxs-lookup"><span data-stu-id="36a8b-103">XPDM vs. WDDM</span></span>

<span data-ttu-id="36a8b-104">La API de Direct3D 9 funciona en el modelo de controladores de pantalla de Windows XP (XPDM) o en el modelo de controladores de pantalla (WDDM) de Windows Vista, dependiendo del sistema operativo instalado.</span><span class="sxs-lookup"><span data-stu-id="36a8b-104">The Direct3D 9 API operates on either the Windows XP display driver model (XPDM) or the Windows Vista display driver model (WDDM), depending on the operating system installed.</span></span> <span data-ttu-id="36a8b-105">Hay algunas diferencias en la forma en que la API de Direct3D se comporta en los dos modelos de controladores.</span><span class="sxs-lookup"><span data-stu-id="36a8b-105">There are some differences in the way the Direct3D API behaves on the two driver models.</span></span>

-   [<span data-ttu-id="36a8b-106">Escritorio seguro</span><span class="sxs-lookup"><span data-stu-id="36a8b-106">Secure Desktop</span></span>](#secure-desktop)
-   [<span data-ttu-id="36a8b-107">Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="36a8b-107">Remote Desktop</span></span>](#remote-desktop)
-   [<span data-ttu-id="36a8b-108">Servicio de Windows</span><span class="sxs-lookup"><span data-stu-id="36a8b-108">Windows Service</span></span>](#windows-service)
-   [<span data-ttu-id="36a8b-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36a8b-109">Related topics</span></span>](#related-topics)

## <a name="secure-desktop"></a><span data-ttu-id="36a8b-110">Escritorio seguro</span><span class="sxs-lookup"><span data-stu-id="36a8b-110">Secure Desktop</span></span>

<span data-ttu-id="36a8b-111">El escritorio seguro está activo siempre que se produzca cualquiera de las siguientes situaciones: el usuario bloquea el escritorio (Windows + L), se activa el protector de pantalla (cuando ningún usuario ha iniciado sesión) o de forma predeterminada cuando el control de cuentas de usuario presenta un mensaje.</span><span class="sxs-lookup"><span data-stu-id="36a8b-111">The secure desktop is active whenever any of the following occur: the user locks their desktop (Windows+L), the screen saver activates (when no user is logged in), or by default when User Account Control presents a prompt.</span></span> <span data-ttu-id="36a8b-112">Cuando el escritorio seguro está activo, el dispositivo HAL no es accesible.</span><span class="sxs-lookup"><span data-stu-id="36a8b-112">When the secure desktop is active, the HAL device is not accessible.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36a8b-113">Diferencias entre XPDM y WDDM:</span><span class="sxs-lookup"><span data-stu-id="36a8b-113">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="36a8b-114">Se producirá un error al intentar crear un dispositivo HAL de Direct3D9 (con **D3DERR \_ no \_ disponible**) y cualquier dispositivo de Direct3D 9 existente indicará un código de retorno de dispositivo perdido en este momento.</span><span class="sxs-lookup"><span data-stu-id="36a8b-114">Attempting to create a Direct3D9 HAL device will fail (with **D3DERR\_NOT\_AVAILABLE**), and any existing Direct3D 9 device will indicate a lost device return code on Present.</span></span><br/> <span data-ttu-id="36a8b-115">Las API de Direct3D9Ex y Direct3D 10 pueden crear correctamente un dispositivo mientras el escritorio seguro está activo y las llamadas a Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) o DXGI) devolverán un código de estado que indica que el escritorio no está disponible actualmente.</span><span class="sxs-lookup"><span data-stu-id="36a8b-115">Direct3D9Ex and Direct3D 10 APIs can successfully create a device while the secure desktop is active, and any calls to Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) or DXGI) will return a status code indicating the desktop is currently unavailable.</span></span><br/> |



 

## <a name="remote-desktop"></a><span data-ttu-id="36a8b-116">Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="36a8b-116">Remote Desktop</span></span>

<span data-ttu-id="36a8b-117">Cuando un escritorio remoto está activo, la pantalla se encarga de la visualización con el equipo host enviando información a través de la red.</span><span class="sxs-lookup"><span data-stu-id="36a8b-117">When a remote desktop is active, the display is handled by the viewing machine with the hosting machine sending information via the network.</span></span>



|                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36a8b-118">Diferencias entre XPDM y WDDM:</span><span class="sxs-lookup"><span data-stu-id="36a8b-118">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="36a8b-119">En XPDM, se producirá un error en todos los intentos de crear un dispositivo de Direct3D 9 en un escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="36a8b-119">On XPDM, all attempts to create a Direct3D 9 device on a remote desktop will fail.</span></span><br/> <span data-ttu-id="36a8b-120">En WDDM, escritorio remoto admite la creación de un dispositivo HAL a través de una sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="36a8b-120">On WDDM, remote desktop does support creating a HAL device over a remote desktop session.</span></span><br/> |



 

## <a name="windows-service"></a><span data-ttu-id="36a8b-121">Servicio de Windows</span><span class="sxs-lookup"><span data-stu-id="36a8b-121">Windows Service</span></span>

<span data-ttu-id="36a8b-122">Un servicio de Windows es un proceso que se ejecuta en segundo plano, controlado por el administrador de control de servicios (SCM).</span><span class="sxs-lookup"><span data-stu-id="36a8b-122">A Windows service is a process that runs in the background, controlled by the service-control manager (SCM).</span></span> <span data-ttu-id="36a8b-123">Un servicio se ejecuta de forma independiente del escritorio activo y, por tanto, tiene una capacidad limitada para interactuar con los usuarios.</span><span class="sxs-lookup"><span data-stu-id="36a8b-123">A service runs independent of the active desktop and therefore has limited ability to interact with users.</span></span>



|                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36a8b-124">Diferencias entre XPDM y WDDM:</span><span class="sxs-lookup"><span data-stu-id="36a8b-124">Differences between XPDM and WDDM:</span></span><br/> <span data-ttu-id="36a8b-125">En WDDM, el aislamiento de sesión 0 garantiza que un servicio no tiene acceso a ningún escritorio de usuario como medida de seguridad; por lo tanto, un dispositivo HAL de Direct3D 9 nunca está disponible desde un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="36a8b-125">On WDDM, Session 0 Isolation ensures that a service does not have access to any user desktop as a security measure, therefore, a Direct3D 9 HAL device is never available from a Windows service.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="36a8b-126">No se puede usar Direct3D 9 en un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="36a8b-126">You cannot use Direct3D 9 in a Windows service.</span></span> <span data-ttu-id="36a8b-127">Para obtener más información, vea el [artículo de soporte técnico de Microsoft 978635](https://support.microsoft.com/kb/978635).</span><span class="sxs-lookup"><span data-stu-id="36a8b-127">For more information, see [Microsoft support article 978635](https://support.microsoft.com/kb/978635).</span></span>

 


<span data-ttu-id="36a8b-128">En la tabla siguiente se resumen las diferencias que se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="36a8b-128">The following table summarizes the differences listed here.</span></span>



|                 | <span data-ttu-id="36a8b-129">XPDM</span><span class="sxs-lookup"><span data-stu-id="36a8b-129">XPDM</span></span> | <span data-ttu-id="36a8b-130">WDDM (Direct3D9)</span><span class="sxs-lookup"><span data-stu-id="36a8b-130">WDDM (Direct3D9)</span></span> | <span data-ttu-id="36a8b-131">WDDM (Direct3D9Ex/Direct3D10)</span><span class="sxs-lookup"><span data-stu-id="36a8b-131">WDDM(Direct3D9Ex/Direct3D10)</span></span> |
|-----------------|------|------------------|------------------------------|
| <span data-ttu-id="36a8b-132">Escritorio seguro</span><span class="sxs-lookup"><span data-stu-id="36a8b-132">Secure Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="36a8b-133">NULLREF</span><span class="sxs-lookup"><span data-stu-id="36a8b-133">NULLREF</span></span>         | <span data-ttu-id="36a8b-134">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-134">Yes</span></span>  | <span data-ttu-id="36a8b-135">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-135">Yes</span></span>              | <span data-ttu-id="36a8b-136">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-136">Yes</span></span>                          |
| <span data-ttu-id="36a8b-137">HAL</span><span class="sxs-lookup"><span data-stu-id="36a8b-137">HAL</span></span>             | <span data-ttu-id="36a8b-138">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-138">No</span></span>   | <span data-ttu-id="36a8b-139">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-139">No</span></span>               | <span data-ttu-id="36a8b-140">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-140">Yes</span></span>                          |
| <span data-ttu-id="36a8b-141">REF</span><span class="sxs-lookup"><span data-stu-id="36a8b-141">REF</span></span>             | <span data-ttu-id="36a8b-142">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-142">Yes</span></span>  | <span data-ttu-id="36a8b-143">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-143">Yes</span></span>              | <span data-ttu-id="36a8b-144">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-144">Yes</span></span>                          |
| <span data-ttu-id="36a8b-145">Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="36a8b-145">Remote Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="36a8b-146">NULLREF</span><span class="sxs-lookup"><span data-stu-id="36a8b-146">NULLREF</span></span>         | <span data-ttu-id="36a8b-147">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-147">No</span></span>   | <span data-ttu-id="36a8b-148">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-148">Yes</span></span>              | <span data-ttu-id="36a8b-149">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-149">Yes</span></span>                          |
| <span data-ttu-id="36a8b-150">HAL</span><span class="sxs-lookup"><span data-stu-id="36a8b-150">HAL</span></span>             | <span data-ttu-id="36a8b-151">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-151">No</span></span>   | <span data-ttu-id="36a8b-152">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-152">Yes</span></span>              | <span data-ttu-id="36a8b-153">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-153">Yes</span></span>                          |
| <span data-ttu-id="36a8b-154">REF</span><span class="sxs-lookup"><span data-stu-id="36a8b-154">REF</span></span>             | <span data-ttu-id="36a8b-155">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-155">Yes</span></span>  | <span data-ttu-id="36a8b-156">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-156">Yes</span></span>              | <span data-ttu-id="36a8b-157">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-157">Yes</span></span>                          |
| <span data-ttu-id="36a8b-158">Servicio de Windows</span><span class="sxs-lookup"><span data-stu-id="36a8b-158">Windows Service</span></span> |      |                  |                              |
| <span data-ttu-id="36a8b-159">NULLREF</span><span class="sxs-lookup"><span data-stu-id="36a8b-159">NULLREF</span></span>         | <span data-ttu-id="36a8b-160">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-160">No</span></span>   | <span data-ttu-id="36a8b-161">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-161">No</span></span>               | <span data-ttu-id="36a8b-162">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-162">No</span></span>                           |
| <span data-ttu-id="36a8b-163">HAL</span><span class="sxs-lookup"><span data-stu-id="36a8b-163">HAL</span></span>             | <span data-ttu-id="36a8b-164">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-164">No</span></span>   | <span data-ttu-id="36a8b-165">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-165">No</span></span>               | <span data-ttu-id="36a8b-166">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-166">No</span></span>                           |
| <span data-ttu-id="36a8b-167">REF</span><span class="sxs-lookup"><span data-stu-id="36a8b-167">REF</span></span>             | <span data-ttu-id="36a8b-168">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-168">No</span></span>   | <span data-ttu-id="36a8b-169">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-169">No</span></span>               | <span data-ttu-id="36a8b-170">No</span><span class="sxs-lookup"><span data-stu-id="36a8b-170">No</span></span>                           |
| <span data-ttu-id="36a8b-171">WARP10</span><span class="sxs-lookup"><span data-stu-id="36a8b-171">WARP10</span></span>          | <span data-ttu-id="36a8b-172">N/D</span><span class="sxs-lookup"><span data-stu-id="36a8b-172">N/A</span></span>  | <span data-ttu-id="36a8b-173">N/D</span><span class="sxs-lookup"><span data-stu-id="36a8b-173">N/A</span></span>              | <span data-ttu-id="36a8b-174">Sí</span><span class="sxs-lookup"><span data-stu-id="36a8b-174">Yes</span></span>                          |



 

<span data-ttu-id="36a8b-175">Para obtener más información sobre XPDM, WDDM, Direct3D9Ex y Direct3D 10, vea [API de gráficos en Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="36a8b-175">For more information about XPDM, WDDM, Direct3D9Ex, and Direct3D 10, see [Graphics APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="36a8b-176">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36a8b-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36a8b-177">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="36a8b-177">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
