---
title: Usar el control ActiveX Escritorio remoto
description: Cómo puede utilizar el control ActiveX Escritorio remoto para personalizar la experiencia del usuario Servicios de Escritorio remoto.
ms.assetid: ea80a99a-7bf6-48e2-8bd0-c9a158bcf475
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, usar Escritorio remoto control ActiveX
- Conexión web a Escritorio remoto Servicios de Escritorio remoto, usar
- Protocolo de escritorio remoto Servicios de Escritorio remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b06f575d5cffc16bd19f6bbe5fd4b3237dda7b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685486"
---
# <a name="using-the-remote-desktop-activex-control"></a><span data-ttu-id="cb052-106">Usar el control ActiveX Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="cb052-106">Using the Remote Desktop ActiveX control</span></span>

<span data-ttu-id="cb052-107">Los temas siguientes contienen información sobre cómo puede utilizar el control ActiveX Escritorio remoto para personalizar la experiencia del usuario Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="cb052-107">The following topics contain information about how you can use the Remote Desktop ActiveX control to customize the Remote Desktop Services user experience.</span></span>

<span data-ttu-id="cb052-108">El control ActiveX Escritorio remoto está disponible en los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="cb052-108">The Remote Desktop ActiveX control is available in the following forms:</span></span>

-   <span data-ttu-id="cb052-109">**El control Scriptable**: implementa interfaces que son seguras para el scripting.</span><span class="sxs-lookup"><span data-stu-id="cb052-109">**The scriptable control**—implements interfaces that are safe for scripting.</span></span> <span data-ttu-id="cb052-110">Esta forma de control la pueden usar los clientes Web o los hosts de scripting (como VBScript).</span><span class="sxs-lookup"><span data-stu-id="cb052-110">This form of the control can be used by web clients or scripting (such as VBScript) hosts.</span></span>
-   <span data-ttu-id="cb052-111">**El control que no admite scripts**: ofrece funcionalidad adicional que no es segura para el scripting.</span><span class="sxs-lookup"><span data-stu-id="cb052-111">**The nonscriptable control**—offers additional functionality that is not safe for scripting.</span></span> <span data-ttu-id="cb052-112">Este formulario del control se puede usar desde código nativo o administrado, pero los clientes Web o los hosts de scripting no pueden usar este formulario.</span><span class="sxs-lookup"><span data-stu-id="cb052-112">This form of the control can be used from native or managed code, but this form cannot be used by web clients or scripting-only hosts.</span></span>

<span data-ttu-id="cb052-113">La lista siguiente contiene los **CLSID** para los diferentes controles de diferentes versiones de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cb052-113">The following list contains the **CLSID** s for the different controls for different operating system versions.</span></span> <span data-ttu-id="cb052-114">Cada **CLSID** es compatible con versiones posteriores del sistema.</span><span class="sxs-lookup"><span data-stu-id="cb052-114">Each of the **CLSID** s is compatible with later system versions.</span></span> <span data-ttu-id="cb052-115">Por ejemplo, el **CLSID** para el control con scripts en Windows Vista funcionará en versiones posteriores del sistema, como Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cb052-115">For example, the **CLSID** for the scriptable control on Windows Vista will work on later system versions, such as Windows 7.</span></span>



| <span data-ttu-id="cb052-116">Versión del sistema</span><span class="sxs-lookup"><span data-stu-id="cb052-116">System version</span></span>                          | <span data-ttu-id="cb052-117">CLSID de control que admite scripts</span><span class="sxs-lookup"><span data-stu-id="cb052-117">Scriptable control CLSID</span></span>             | <span data-ttu-id="cb052-118">CLSID de control que no admite scripts</span><span class="sxs-lookup"><span data-stu-id="cb052-118">Nonscriptable control CLSID</span></span>          |
|-----------------------------------------|--------------------------------------|--------------------------------------|
| <span data-ttu-id="cb052-119">Windows 8.1, Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="cb052-119">Windows 8.1, Windows Server 2012 R2</span></span>     | <span data-ttu-id="cb052-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="cb052-120">301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span> | <span data-ttu-id="cb052-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="cb052-121">8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span> |
| <span data-ttu-id="cb052-122">Windows 8, Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cb052-122">Windows 8, Windows Server 2012</span></span>          | <span data-ttu-id="cb052-123">5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="cb052-123">5F681803-2900-4C43-A1CC-CF405404A676</span></span> | <span data-ttu-id="cb052-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="cb052-124">A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span> |
| <span data-ttu-id="cb052-125">Windows 7, Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb052-125">Windows 7, Windows Server 2008</span></span>          | <span data-ttu-id="cb052-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="cb052-126">A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span> | <span data-ttu-id="cb052-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="cb052-127">54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span> |
| <span data-ttu-id="cb052-128">Windows Vista con Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="cb052-128">Windows Vista with Service Pack 1 (SP1)</span></span> | <span data-ttu-id="cb052-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span><span class="sxs-lookup"><span data-stu-id="cb052-129">7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span></span> | <span data-ttu-id="cb052-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span><span class="sxs-lookup"><span data-stu-id="cb052-130">D2EA46A7-C2BF-426B-AF24-E19C44456399</span></span> |
| <span data-ttu-id="cb052-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb052-131">Windows Vista</span></span>                           | <span data-ttu-id="cb052-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span><span class="sxs-lookup"><span data-stu-id="cb052-132">4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span></span> | <span data-ttu-id="cb052-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span><span class="sxs-lookup"><span data-stu-id="cb052-133">4EB2F086-C818-447E-B32C-C51CE2B30D31</span></span> |



 

## <a name="in-this-section"></a><span data-ttu-id="cb052-134">En esta sección</span><span class="sxs-lookup"><span data-stu-id="cb052-134">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="cb052-135">Incrustar el control ActiveX Escritorio remoto en una página web</span><span class="sxs-lookup"><span data-stu-id="cb052-135">Embedding the Remote Desktop ActiveX control in a webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dd>

<span data-ttu-id="cb052-136">Ejemplo que muestra el uso de las interfaces que admiten scripts.</span><span class="sxs-lookup"><span data-stu-id="cb052-136">Example that demonstrates the use of the scriptable interfaces.</span></span>

</dd> <dt>

[<span data-ttu-id="cb052-137">Implementación de canales virtuales con scripts mediante Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="cb052-137">Implementing scriptable virtual channels by using Remote Desktop Web Connection</span></span>](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
</dt> <dd>

<span data-ttu-id="cb052-138">Ejemplos de código que muestran los pasos para implementar canales virtuales que admiten scripts con Conexión web a Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="cb052-138">Code examples that show the steps for implementing scriptable virtual channels with Remote Desktop Web Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="cb052-139">Usar el control ActiveX Escritorio remoto con canales virtuales</span><span class="sxs-lookup"><span data-stu-id="cb052-139">Using the Remote Desktop ActiveX control with virtual channels</span></span>](using-the-remote-desktop-activex-control-with-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="cb052-140">Si ha habilitado una aplicación de canales virtuales en la implementación de Servicios de Escritorio remoto, puede hacer que esta aplicación esté disponible para los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="cb052-140">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers.</span></span>

</dd> <dt>

[<span data-ttu-id="cb052-141">Página Web de ejemplo incluida con el control ActiveX Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="cb052-141">Sample webpage included with the Remote Desktop ActiveX control</span></span>](sample-web-page-included-with-the-remote-desktop-activex-control.md)
</dt> <dd>

<span data-ttu-id="cb052-142">Una página web de ejemplo (Default.htm) está en el directorio donde está instalado Conexión web a Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="cb052-142">A sample webpage (Default.htm) is in the directory where Remote Desktop Web Connection is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="cb052-143">Proporcionar seguridad de cliente RDP</span><span class="sxs-lookup"><span data-stu-id="cb052-143">Providing for RDP client security</span></span>](providing-for-rdp-client-security.md)
</dt> <dd>

<span data-ttu-id="cb052-144">Algunas propiedades del objeto de control ActiveX Escritorio remoto están restringidas a zonas de seguridad de direcciones URL específicas de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="cb052-144">Some properties of the Remote Desktop ActiveX control object are restricted to specific Internet Explorer URL security zones.</span></span>

</dd> <dt>

[<span data-ttu-id="cb052-145">Deshabilitar características de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="cb052-145">Disabling Remote Desktop Services features</span></span>](disabling-terminal-services-features.md)
</dt> <dd>

<span data-ttu-id="cb052-146">Para mejorar la seguridad, puede optar por deshabilitar Servicios de Escritorio remoto características.</span><span class="sxs-lookup"><span data-stu-id="cb052-146">For enhanced security, you might choose to disable Remote Desktop Services features.</span></span>

</dd> </dl>

<span data-ttu-id="cb052-147">Para obtener más información acerca de la Página Web de ejemplo que se incluye con la instalación del control ActiveX Escritorio remoto, vea [Página Web de ejemplo que se incluye con el control activex escritorio remoto](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span><span class="sxs-lookup"><span data-stu-id="cb052-147">For more information about the sample webpage that is included with the installation of the Remote Desktop ActiveX control, see [Sample webpage included with the Remote Desktop ActiveX control](sample-web-page-included-with-the-remote-desktop-activex-control.md).</span></span>

 

 




