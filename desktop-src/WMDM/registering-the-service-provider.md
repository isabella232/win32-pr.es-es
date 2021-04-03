---
title: Registrar el proveedor de servicios
description: Registrar el proveedor de servicios
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Media Administrador de dispositivos, registrar proveedores de servicios
- Administrador de dispositivos, registrar proveedores de servicios
- Guía de programación, registrar proveedores de servicios
- proveedores de servicios, registrar proveedores de servicios
- creación de proveedores de servicios, registro de proveedores de servicios
- registrando proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075260"
---
# <a name="registering-the-service-provider"></a><span data-ttu-id="705d7-109">Registrar el proveedor de servicios</span><span class="sxs-lookup"><span data-stu-id="705d7-109">Registering the Service Provider</span></span>

<span data-ttu-id="705d7-110">Además de registrarse como un objeto COM, se debe registrar un proveedor de servicios como un complemento de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="705d7-110">In addition to being registered as a COM object, a service provider must be registered as a plug-in to Windows Media Device Manager.</span></span> <span data-ttu-id="705d7-111">Para registrarse, un proveedor de servicios debe crear la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="705d7-111">To register, a service provider must create the following registry key:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

<span data-ttu-id="705d7-112">En esta clave, < *el nombre del proveedor de servicios* > es el nombre del archivo dll; por ejemplo, el proveedor de servicios de ejemplo usa MsHDSP.</span><span class="sxs-lookup"><span data-stu-id="705d7-112">In this key, < *your service provider name* > is the name of your DLL; for example, the sample service provider uses MsHDSP.</span></span> <span data-ttu-id="705d7-113">La clave ProgID debe tener un valor de cadena que se corresponda con el CLSID de su proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="705d7-113">The ProgID key should have a string value that corresponds to the CLSID of your service provider.</span></span> <span data-ttu-id="705d7-114">Por ejemplo, el proveedor de servicios de ejemplo tiene el valor "MDServiceProviderHD. MDServiceProviderHD".</span><span class="sxs-lookup"><span data-stu-id="705d7-114">For instance, the sample service provider has the value "MDServiceProviderHD.MDServiceProviderHD".</span></span>

<span data-ttu-id="705d7-115">La implementación del proveedor de servicios de ejemplo de DLLRegisterServer en Mdsp. cpp agrega esta clave del registro al registrar la DLL del proveedor de servicios de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="705d7-115">The sample service provider's implementation of DLLRegisterServer in Mdsp.cpp adds this registry key when you register the sample service provider DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="705d7-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="705d7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="705d7-117">**Creación de un proveedor de servicios**</span><span class="sxs-lookup"><span data-stu-id="705d7-117">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




