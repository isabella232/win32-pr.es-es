---
description: La API de Direct3D 9 funciona en el modelo de controlador de pantalla de Windows XP (XPDM) o en el modelo de controlador de pantalla de Windows Vista (WDDM), dependiendo del sistema operativo instalado.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM frente a WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12c7d811850c953eb53c346b628363a2642dda9
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343540"
---
# <a name="xpdm-vs-wddm"></a><span data-ttu-id="45d64-103">XPDM frente a WDDM</span><span class="sxs-lookup"><span data-stu-id="45d64-103">XPDM vs. WDDM</span></span>

<span data-ttu-id="45d64-104">La API de Direct3D 9 funciona en el modelo de controlador de pantalla de Windows XP (XPDM) o en el modelo de controlador de pantalla de Windows Vista (WDDM), dependiendo del sistema operativo instalado.</span><span class="sxs-lookup"><span data-stu-id="45d64-104">The Direct3D 9 API operates on either the Windows XP display driver model (XPDM) or the Windows Vista display driver model (WDDM), depending on the operating system installed.</span></span> <span data-ttu-id="45d64-105">Hay algunas diferencias en el comportamiento de la API de Direct3D en los dos modelos de controlador.</span><span class="sxs-lookup"><span data-stu-id="45d64-105">There are some differences in the way the Direct3D API behaves on the two driver models.</span></span>

-   [<span data-ttu-id="45d64-106">Escritorio seguro</span><span class="sxs-lookup"><span data-stu-id="45d64-106">Secure Desktop</span></span>](#secure-desktop)
-   [<span data-ttu-id="45d64-107">Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="45d64-107">Remote Desktop</span></span>](#remote-desktop)
-   [<span data-ttu-id="45d64-108">Servicio de Windows</span><span class="sxs-lookup"><span data-stu-id="45d64-108">Windows Service</span></span>](#windows-service)
-   [<span data-ttu-id="45d64-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45d64-109">Related topics</span></span>](#related-topics)

## <a name="secure-desktop"></a><span data-ttu-id="45d64-110">Escritorio seguro</span><span class="sxs-lookup"><span data-stu-id="45d64-110">Secure Desktop</span></span>

<span data-ttu-id="45d64-111">El escritorio seguro está activo siempre que se produzca alguna de las siguientes situaciones: el usuario bloquea su escritorio (Windows+L), el protector de pantalla se activa (cuando no hay ningún usuario conectado) o de forma predeterminada cuando Control de cuentas de usuario presenta un mensaje.</span><span class="sxs-lookup"><span data-stu-id="45d64-111">The secure desktop is active whenever any of the following occur: the user locks their desktop (Windows+L), the screen saver activates (when no user is logged in), or by default when User Account Control presents a prompt.</span></span> <span data-ttu-id="45d64-112">Cuando el escritorio seguro está activo, no se puede acceder al dispositivo DEIMENTE.</span><span class="sxs-lookup"><span data-stu-id="45d64-112">When the secure desktop is active, the HAL device is not accessible.</span></span>

<span data-ttu-id="45d64-113">Diferencias entre XPDM y WDDM:</span><span class="sxs-lookup"><span data-stu-id="45d64-113">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="45d64-114">Se producirá un error al intentar crear un dispositivo DIRECT3D9 SEVERI (con **D3DERR \_ NO \_ DISPONIBLE)** y cualquier dispositivo Direct3D 9 existente indicará un código de retorno de dispositivo perdido en Present.</span><span class="sxs-lookup"><span data-stu-id="45d64-114">Attempting to create a Direct3D9 HAL device will fail (with **D3DERR\_NOT\_AVAILABLE**), and any existing Direct3D 9 device will indicate a lost device return code on Present.</span></span>

- <span data-ttu-id="45d64-115">Las API de Direct3D9Ex y Direct3D 10 pueden crear correctamente un dispositivo mientras el escritorio seguro está activo y las llamadas a Present [**(IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) o DXGI) devolverán un código de estado que indica que el escritorio no está disponible actualmente.</span><span class="sxs-lookup"><span data-stu-id="45d64-115">Direct3D9Ex and Direct3D 10 APIs can successfully create a device while the secure desktop is active, and any calls to Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) or DXGI) will return a status code indicating the desktop is currently unavailable.</span></span>



 

## <a name="remote-desktop"></a><span data-ttu-id="45d64-116">Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="45d64-116">Remote Desktop</span></span>

<span data-ttu-id="45d64-117">Cuando un escritorio remoto está activo, la pantalla la controla el equipo de visualización con el equipo de hospedaje que envía información a través de la red.</span><span class="sxs-lookup"><span data-stu-id="45d64-117">When a remote desktop is active, the display is handled by the viewing machine with the hosting machine sending information via the network.</span></span>

<span data-ttu-id="45d64-118">Diferencias entre XPDM y WDDM:</span><span class="sxs-lookup"><span data-stu-id="45d64-118">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="45d64-119">En XPDM, se producirá un error en todos los intentos de crear un dispositivo Direct3D 9 en un escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="45d64-119">On XPDM, all attempts to create a Direct3D 9 device on a remote desktop will fail.</span></span>

- <span data-ttu-id="45d64-120">En WDDM, el escritorio remoto admite la creación de un dispositivo DESA través de una sesión de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="45d64-120">On WDDM, remote desktop does support creating a HAL device over a remote desktop session.</span></span>



 

## <a name="windows-service"></a><span data-ttu-id="45d64-121">Servicio de Windows</span><span class="sxs-lookup"><span data-stu-id="45d64-121">Windows Service</span></span>

<span data-ttu-id="45d64-122">Un servicio de Windows es un proceso que se ejecuta en segundo plano, controlado por el administrador de control de servicios (SCM).</span><span class="sxs-lookup"><span data-stu-id="45d64-122">A Windows service is a process that runs in the background, controlled by the service-control manager (SCM).</span></span> <span data-ttu-id="45d64-123">Un servicio se ejecuta independientemente del escritorio activo y, por tanto, tiene una capacidad limitada para interactuar con los usuarios.</span><span class="sxs-lookup"><span data-stu-id="45d64-123">A service runs independent of the active desktop and therefore has limited ability to interact with users.</span></span>

<span data-ttu-id="45d64-124">Diferencias entre XPDM y WDDM:</span><span class="sxs-lookup"><span data-stu-id="45d64-124">Differences between XPDM and WDDM:</span></span>

- <span data-ttu-id="45d64-125">En WDDM, el aislamiento de sesión 0 garantiza que un servicio no tiene acceso a ningún escritorio de usuario como medida de seguridad, por lo tanto, un dispositivo DIRECT3D 9 UNO nunca está disponible desde un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="45d64-125">On WDDM, Session 0 Isolation ensures that a service does not have access to any user desktop as a security measure, therefore, a Direct3D 9 HAL device is never available from a Windows service.</span></span>



 

> [!Note]  
> <span data-ttu-id="45d64-126">No se puede usar Direct3D 9 en un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="45d64-126">You cannot use Direct3D 9 in a Windows service.</span></span> <span data-ttu-id="45d64-127">Para más información, consulte el [artículo de soporte técnico de Microsoft 978635.](https://support.microsoft.com/kb/978635)</span><span class="sxs-lookup"><span data-stu-id="45d64-127">For more information, see [Microsoft support article 978635](https://support.microsoft.com/kb/978635).</span></span>

 


<span data-ttu-id="45d64-128">En la tabla siguiente se resumen las diferencias enumeradas aquí.</span><span class="sxs-lookup"><span data-stu-id="45d64-128">The following table summarizes the differences listed here.</span></span>



| <span data-ttu-id="45d64-129">Escritorio seguro</span><span class="sxs-lookup"><span data-stu-id="45d64-129">Secure Desktop</span></span> | <span data-ttu-id="45d64-130">XPDM</span><span class="sxs-lookup"><span data-stu-id="45d64-130">XPDM</span></span> | <span data-ttu-id="45d64-131">WDDM (Direct3D9)</span><span class="sxs-lookup"><span data-stu-id="45d64-131">WDDM (Direct3D9)</span></span> | <span data-ttu-id="45d64-132">WDDM(Direct3D9Ex/Direct3D10)</span><span class="sxs-lookup"><span data-stu-id="45d64-132">WDDM(Direct3D9Ex/Direct3D10)</span></span> |
|-----------------|------|------------------|------------------------------|
| <span data-ttu-id="45d64-133">NULLREF</span><span class="sxs-lookup"><span data-stu-id="45d64-133">NULLREF</span></span>         | <span data-ttu-id="45d64-134">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-134">Yes</span></span>  | <span data-ttu-id="45d64-135">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-135">Yes</span></span>              | <span data-ttu-id="45d64-136">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-136">Yes</span></span>                          |
| <span data-ttu-id="45d64-137">HAL</span><span class="sxs-lookup"><span data-stu-id="45d64-137">HAL</span></span>             | <span data-ttu-id="45d64-138">No</span><span class="sxs-lookup"><span data-stu-id="45d64-138">No</span></span>   | <span data-ttu-id="45d64-139">No</span><span class="sxs-lookup"><span data-stu-id="45d64-139">No</span></span>               | <span data-ttu-id="45d64-140">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-140">Yes</span></span>                          |
| <span data-ttu-id="45d64-141">REF</span><span class="sxs-lookup"><span data-stu-id="45d64-141">REF</span></span>             | <span data-ttu-id="45d64-142">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-142">Yes</span></span>  | <span data-ttu-id="45d64-143">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-143">Yes</span></span>              | <span data-ttu-id="45d64-144">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-144">Yes</span></span>                          |
| <span data-ttu-id="45d64-145">Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="45d64-145">Remote Desktop</span></span>  |      |                  |                              |
| <span data-ttu-id="45d64-146">NULLREF</span><span class="sxs-lookup"><span data-stu-id="45d64-146">NULLREF</span></span>         | <span data-ttu-id="45d64-147">No</span><span class="sxs-lookup"><span data-stu-id="45d64-147">No</span></span>   | <span data-ttu-id="45d64-148">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-148">Yes</span></span>              | <span data-ttu-id="45d64-149">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-149">Yes</span></span>                          |
| <span data-ttu-id="45d64-150">HAL</span><span class="sxs-lookup"><span data-stu-id="45d64-150">HAL</span></span>             | <span data-ttu-id="45d64-151">No</span><span class="sxs-lookup"><span data-stu-id="45d64-151">No</span></span>   | <span data-ttu-id="45d64-152">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-152">Yes</span></span>              | <span data-ttu-id="45d64-153">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-153">Yes</span></span>                          |
| <span data-ttu-id="45d64-154">REF</span><span class="sxs-lookup"><span data-stu-id="45d64-154">REF</span></span>             | <span data-ttu-id="45d64-155">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-155">Yes</span></span>  | <span data-ttu-id="45d64-156">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-156">Yes</span></span>              | <span data-ttu-id="45d64-157">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-157">Yes</span></span>                          |
| <span data-ttu-id="45d64-158">Servicio de Windows</span><span class="sxs-lookup"><span data-stu-id="45d64-158">Windows Service</span></span> |      |                  |                              |
| <span data-ttu-id="45d64-159">NULLREF</span><span class="sxs-lookup"><span data-stu-id="45d64-159">NULLREF</span></span>         | <span data-ttu-id="45d64-160">No</span><span class="sxs-lookup"><span data-stu-id="45d64-160">No</span></span>   | <span data-ttu-id="45d64-161">No</span><span class="sxs-lookup"><span data-stu-id="45d64-161">No</span></span>               | <span data-ttu-id="45d64-162">No</span><span class="sxs-lookup"><span data-stu-id="45d64-162">No</span></span>                           |
| <span data-ttu-id="45d64-163">HAL</span><span class="sxs-lookup"><span data-stu-id="45d64-163">HAL</span></span>             | <span data-ttu-id="45d64-164">No</span><span class="sxs-lookup"><span data-stu-id="45d64-164">No</span></span>   | <span data-ttu-id="45d64-165">No</span><span class="sxs-lookup"><span data-stu-id="45d64-165">No</span></span>               | <span data-ttu-id="45d64-166">No</span><span class="sxs-lookup"><span data-stu-id="45d64-166">No</span></span>                           |
| <span data-ttu-id="45d64-167">REF</span><span class="sxs-lookup"><span data-stu-id="45d64-167">REF</span></span>             | <span data-ttu-id="45d64-168">No</span><span class="sxs-lookup"><span data-stu-id="45d64-168">No</span></span>   | <span data-ttu-id="45d64-169">No</span><span class="sxs-lookup"><span data-stu-id="45d64-169">No</span></span>               | <span data-ttu-id="45d64-170">No</span><span class="sxs-lookup"><span data-stu-id="45d64-170">No</span></span>                           |
| <span data-ttu-id="45d64-171">WARP10</span><span class="sxs-lookup"><span data-stu-id="45d64-171">WARP10</span></span>          | <span data-ttu-id="45d64-172">N/D</span><span class="sxs-lookup"><span data-stu-id="45d64-172">N/A</span></span>  | <span data-ttu-id="45d64-173">N/D</span><span class="sxs-lookup"><span data-stu-id="45d64-173">N/A</span></span>              | <span data-ttu-id="45d64-174">Sí</span><span class="sxs-lookup"><span data-stu-id="45d64-174">Yes</span></span>                          |



 

<span data-ttu-id="45d64-175">Para obtener más información sobre XPDM, WDDM, Direct3D9Ex y Direct3D 10, vea [API de gráficos en Windows.](../direct3darticles/graphics-apis-in-windows-vista.md)</span><span class="sxs-lookup"><span data-stu-id="45d64-175">For more information about XPDM, WDDM, Direct3D9Ex, and Direct3D 10, see [Graphics APIs in Windows](../direct3darticles/graphics-apis-in-windows-vista.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="45d64-176">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="45d64-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45d64-177">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="45d64-177">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
