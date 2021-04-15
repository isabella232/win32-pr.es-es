---
title: Control del contenido protegido en el proveedor de servicios
description: Control del contenido protegido en el proveedor de servicios
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Windows Media Administrador de dispositivos, certificados
- Administrador de dispositivos, certificados
- Guía de programación, certificados
- proveedores de servicios, certificados
- crear proveedores de servicios, certificados
- certificates
- Windows Media Administrador de dispositivos, contenido protegido con DRM
- Administrador de dispositivos, contenido protegido con DRM
- Guía de programación, contenido protegido con DRM
- proveedores de servicios, contenido protegido con DRM
- creación de proveedores de servicios, contenido protegido con DRM
- Contenido protegido con DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695272"
---
# <a name="handling-protected-content-in-the-service-provider"></a><span data-ttu-id="c016c-115">Control del contenido protegido en el proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="c016c-115">Handling Protected Content in the Service Provider</span></span>

<span data-ttu-id="c016c-116">Puede crear un proveedor de servicios que pueda enviar contenido protegido con DRM a un dispositivo basado en DRM de dispositivo portátil (PDDRM), pero no puede crear un proveedor de servicios que pueda enviar contenido protegido con DRM a dispositivos basados en Windows Media DRM 10 para dispositivos portátiles.</span><span class="sxs-lookup"><span data-stu-id="c016c-116">You can build a service provider that can send DRM-protected content to a device built on Portable Device DRM (PDDRM), but you cannot build a service provider that can send DRM-protected content to devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="c016c-117">Estos dispositivos usan MTP y no puede crear su propio proveedor de servicios MTP.</span><span class="sxs-lookup"><span data-stu-id="c016c-117">These devices use MTP, and you cannot build your own MTP service provider.</span></span>

<span data-ttu-id="c016c-118">El único paso adicional que un proveedor de servicios debe llevar a cabo para enviar material de DRM a un dispositivo PDDRM es obtener un par certificado/clave emitido por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c016c-118">The only extra step that a service provider must take to send DRM material to a PDDRM device is to get a Microsoft-issued certificate/key pair.</span></span> <span data-ttu-id="c016c-119">Consulte [herramientas de desarrollo](tools-for-development.md) para obtener información sobre dónde obtener este certificado o clave.</span><span class="sxs-lookup"><span data-stu-id="c016c-119">See [Tools for Development](tools-for-development.md) to learn where to get this certificate/key.</span></span> <span data-ttu-id="c016c-120">Las licencias emitidas para estos dispositivos serán licencias simplificadas que solo admitan la reproducción simple del contenido adquirido. no admitirán licencias de expiración de tiempo.</span><span class="sxs-lookup"><span data-stu-id="c016c-120">The licenses issued to these devices will be simplified licenses that only support simple playback of purchased content; they will not support time-expiring licenses.</span></span> <span data-ttu-id="c016c-121">Esta licencia la creará el proveedor de contenido seguro (proporcionado por Microsoft para archivos WMA/WMV) y se almacenará en el encabezado del archivo que se envía al proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="c016c-121">This license will be created for you by the secure content provider (provided by Microsoft for WMA/WMV files) and stored in the header of the file sent to the service provider.</span></span> <span data-ttu-id="c016c-122">No tendrá que realizar ningún paso especial para los archivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="c016c-122">You will not have to take any special steps for protected files.</span></span>

<span data-ttu-id="c016c-123">Después de enviar el archivo protegido, Windows Media Administrador de dispositivos llamará al proveedor de servicios para solicitar un archivo de almacenamiento de licencias especial del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c016c-123">After sending the protected file, Windows Media Device Manager will call the service provider to request a special license storage file from the device.</span></span> <span data-ttu-id="c016c-124">Windows Media Administrador de dispositivos agregará una copia de la nueva licencia a este archivo y lo devolverá al proveedor de servicios para devolverlo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c016c-124">Windows Media Device Manager will add a copy of the new license to this file, and return it to the service provider to send back to the device.</span></span> <span data-ttu-id="c016c-125">Sin embargo, aunque el proveedor de servicios no encuentre o devuelva este archivo, el dispositivo todavía debe ser capaz de reproducir el archivo protegido mediante la copia de la licencia en el encabezado del archivo.</span><span class="sxs-lookup"><span data-stu-id="c016c-125">However, even if the service provider fails to find or return this file, the device should still be able to play the protected file by using the license copy in the file header.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c016c-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c016c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c016c-127">**Creación de un proveedor de servicios**</span><span class="sxs-lookup"><span data-stu-id="c016c-127">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="c016c-128">**Control de contenido protegido**</span><span class="sxs-lookup"><span data-stu-id="c016c-128">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 




