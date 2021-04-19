---
title: Control de eventos de individualización
description: Control de eventos de individualización
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- SDK de Windows Media Format, control de eventos de individualización
- SDK de Windows Media Format, eventos de individualización
- Advanced Systems Format (ASF), control de eventos de individualización
- ASF (formato de sistemas avanzados), control de eventos de individualización
- Advanced Systems Format (ASF), eventos de individualización
- ASF (formato de sistemas avanzados), eventos de individualización
- Administración de derechos digitales (DRM), control de eventos de individualización
- DRM (administración de derechos digitales), control de eventos de individualización
- Administración de derechos digitales (DRM), eventos de individualización
- DRM (administración de derechos digitales), eventos de individualización
- eventos de individualización
- eventos, eventos de individualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e74df94bf871ec62ec2acb94658785969812640
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105695543"
---
# <a name="handling-individualization-events"></a><span data-ttu-id="40351-115">Control de eventos de individualización</span><span class="sxs-lookup"><span data-stu-id="40351-115">Handling Individualization Events</span></span>

<span data-ttu-id="40351-116">Cuando una aplicación habilitada para DRM intenta abrir un archivo protegido, el componente DRM examina el atributo [**\_ \_ IndividualizedVersion de DRM DRMHeader**](drm-drmheader-individualizedversion.md) en el archivo, que especifica el nivel de versión mínimo necesario para tener acceso al contenido.</span><span class="sxs-lookup"><span data-stu-id="40351-116">When a DRM-enabled application attempts to open a protected file, the DRM component examines the [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md) attribute in the file, which specifies the minimum version level required to access the content.</span></span> <span data-ttu-id="40351-117">Todos los niveles del componente DRM funcionan con todas las versiones 7,0 y posteriores de Windows Media Player y el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="40351-117">All levels of the DRM component work with all 7.0 and later versions of Windows Media Player and the Windows Media Format SDK.</span></span> <span data-ttu-id="40351-118">Si el nivel de versión individualizado del componente DRM es inferior a la versión requerida, el componente DRM enviará un evento **WMT necesitará un evento de \_ \_ individualización** al método [**IWMStatusCallback:: en status**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="40351-118">If the DRM component's individualized version level is lower than the required version, the DRM component will send a **WMT\_NEEDS\_INDIVIDUALIZATION** event to the application's [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="40351-119">A continuación, la aplicación debe mostrar un mensaje o un cuadro de diálogo que solicite a los usuarios que inicien o cancelen la actualización de seguridad.</span><span class="sxs-lookup"><span data-stu-id="40351-119">The application must then display a message or dialog box prompting users to either start or cancel the security upgrade.</span></span> <span data-ttu-id="40351-120">Este mensaje es necesario porque, por motivos de privacidad, los usuarios deben conceder su permiso antes de instalar una actualización de seguridad en su equipo.</span><span class="sxs-lookup"><span data-stu-id="40351-120">This prompt is necessary because, for privacy reasons, users must give their permission before a security upgrade is installed on their computer.</span></span>

> [!Note]  
> <span data-ttu-id="40351-121">El encabezado del contenido especifica solo los dos primeros dígitos para DRM \_ DRMVersion \_ IndividualizedVersion.</span><span class="sxs-lookup"><span data-stu-id="40351-121">The header of the content specifies only the first two digits for DRM\_DRMVersion\_IndividualizedVersion.</span></span> <span data-ttu-id="40351-122">En otras palabras, para requerir un componente 2.2.0.1 de DRM de nivel, el encabezado contendría "2,2".</span><span class="sxs-lookup"><span data-stu-id="40351-122">In other words, to require a level 2.2.0.1 DRM component, the header would contain "2.2".</span></span>

 

<span data-ttu-id="40351-123">Para iniciar la actualización de seguridad y/o desencadenar la individualización, llame al método [**IWMDRMReader:: individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) con el parámetro *dwFlags* establecido en 1.</span><span class="sxs-lookup"><span data-stu-id="40351-123">To start the security upgrade and/or trigger individualization, call the [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) method with the *dwFlags* parameter set to 1.</span></span>

<span data-ttu-id="40351-124">Debe controlar el evento **WMT \_ individual** en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="40351-124">You must handle the **WMT\_INDIVIDUALIZE** event in your application.</span></span> <span data-ttu-id="40351-125">Este evento se activará varias veces mediante el componente DRM con el estado del proceso de individualización indicado en el parámetro *pValue* , que se convierte en un puntero a una estructura de [**\_ \_ Estado**](wm-individualize-status.md) de la función de la función de la función de usuario.</span><span class="sxs-lookup"><span data-stu-id="40351-125">This event will be fired multiple times by the DRM component with the status of the individualization process indicated in the *pValue* parameter, which is cast to a pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

<span data-ttu-id="40351-126">Una vez que el componente DRM se haya individualizado correctamente, la aplicación recibirá un evento **WMT \_ no \_ Rights \_ ex** , lo que indica que la aplicación ahora puede continuar para adquirir una licencia para el contenido.</span><span class="sxs-lookup"><span data-stu-id="40351-126">After the DRM component is successfully individualized, the application will receive a **WMT\_NO\_RIGHTS\_EX** event, indicating that the application can now proceed to acquire a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="40351-127">DRM no es compatible con la versión basada en x64 de este SDK.</span><span class="sxs-lookup"><span data-stu-id="40351-127">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="40351-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40351-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40351-129">**Control de eventos de adquisición de licencias**</span><span class="sxs-lookup"><span data-stu-id="40351-129">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> <dt>

[<span data-ttu-id="40351-130">**Individualización de aplicaciones DRM**</span><span class="sxs-lookup"><span data-stu-id="40351-130">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> <dt>

[<span data-ttu-id="40351-131">**Interfaz IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="40351-131">**IWMDRMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




