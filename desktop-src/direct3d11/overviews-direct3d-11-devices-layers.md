---
title: Capas de software
description: El tiempo de ejecución de Direct3D 11 se construye con capas, comenzando con la funcionalidad básica en el núcleo y creando funcionalidad opcional y de ayuda para desarrolladores en capas externas. En esta sección se describe la funcionalidad de cada capa.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb05658860e678e8020392cb046a634e3b03c7c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533190"
---
# <a name="software-layers"></a><span data-ttu-id="bc12d-104">Capas de software</span><span class="sxs-lookup"><span data-stu-id="bc12d-104">Software Layers</span></span>

<span data-ttu-id="bc12d-105">El tiempo de ejecución de Direct3D 11 se construye con capas, comenzando con la funcionalidad básica en el núcleo y creando funcionalidad opcional y de ayuda para desarrolladores en capas externas.</span><span class="sxs-lookup"><span data-stu-id="bc12d-105">The Direct3D 11 runtime is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality in outer layers.</span></span> <span data-ttu-id="bc12d-106">En esta sección se describe la funcionalidad de cada capa.</span><span class="sxs-lookup"><span data-stu-id="bc12d-106">This section describes the functionality of each layer.</span></span>

<span data-ttu-id="bc12d-107">Como norma general, las capas agregan funcionalidad, pero no modifican el comportamiento existente.</span><span class="sxs-lookup"><span data-stu-id="bc12d-107">As a general rule, layers add functionality, but do not modify existing behavior.</span></span> <span data-ttu-id="bc12d-108">Por ejemplo, las funciones principales tendrán los mismos valores devueltos independientemente de la capa de depuración de la que se crea una instancia, aunque se puede proporcionar una salida de depuración adicional si se crea una instancia de la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="bc12d-108">For example, core functions will have the same return values independent of the debug layer being instantiated, although additional debug output may be provided if the debug layer is instantiated.</span></span>

<span data-ttu-id="bc12d-109">Para crear capas cuando se crea un dispositivo, llame a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) y proporcione uno o varios valores de [**\_ marca de dispositivo D3D11 Create \_ \_ Device**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) .</span><span class="sxs-lookup"><span data-stu-id="bc12d-109">To create layers when a device is created, call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) and supply one or more [**D3D11\_CREATE\_DEVICE\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) values.</span></span>

<span data-ttu-id="bc12d-110">Direct3D 11 proporciona las siguientes capas de tiempo de ejecución:</span><span class="sxs-lookup"><span data-stu-id="bc12d-110">Direct3D 11 provides the following runtime layers:</span></span>

-   [<span data-ttu-id="bc12d-111">Nivel básico</span><span class="sxs-lookup"><span data-stu-id="bc12d-111">Core Layer</span></span>](#core-layer)
-   [<span data-ttu-id="bc12d-112">Nivel de depuración</span><span class="sxs-lookup"><span data-stu-id="bc12d-112">Debug Layer</span></span>](#debug-layer)
-   [<span data-ttu-id="bc12d-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc12d-113">Related topics</span></span>](#related-topics)

## <a name="core-layer"></a><span data-ttu-id="bc12d-114">Nivel básico</span><span class="sxs-lookup"><span data-stu-id="bc12d-114">Core Layer</span></span>

<span data-ttu-id="bc12d-115">La capa principal existe de forma predeterminada; proporcionar una asignación muy fina entre la API y el controlador de dispositivo, lo que minimiza la sobrecarga de llamadas de alta frecuencia.</span><span class="sxs-lookup"><span data-stu-id="bc12d-115">The core layer exists by default; providing a very thin mapping between the API and the device driver, minimizing overhead for high-frequency calls.</span></span> <span data-ttu-id="bc12d-116">Como la capa principal es esencial para el rendimiento, solo realiza una validación crítica.</span><span class="sxs-lookup"><span data-stu-id="bc12d-116">As the core layer is essential for performance, it only performs critical validation.</span></span> <span data-ttu-id="bc12d-117">Las capas restantes son opcionales.</span><span class="sxs-lookup"><span data-stu-id="bc12d-117">The remaining layers are optional.</span></span>

## <a name="debug-layer"></a><span data-ttu-id="bc12d-118">Nivel de depuración</span><span class="sxs-lookup"><span data-stu-id="bc12d-118">Debug Layer</span></span>

<span data-ttu-id="bc12d-119">La capa de depuración proporciona un amplio parámetro adicional y una validación de coherencia (como la validación de la vinculación del sombreador y el enlace de recursos, la validación de la coherencia de los parámetros y la notificación de descripciones</span><span class="sxs-lookup"><span data-stu-id="bc12d-119">The debug layer provides extensive additional parameter and consistency validation (such as validating shader linkage and resource binding, validating parameter consistency, and reporting error descriptions).</span></span>

<span data-ttu-id="bc12d-120">Para crear un dispositivo que admita la capa de depuración, debe instalar el SDK de DirectX (para obtener D3D11SDKLayers.dll) y, a continuación, especificar el indicador de **\_ \_ \_ depuración crear dispositivo de D3D11** al llamar a la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o a la función [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) .</span><span class="sxs-lookup"><span data-stu-id="bc12d-120">To create a device that supports the debug layer, you must install the DirectX SDK (to get D3D11SDKLayers.dll), and then specify the **D3D11\_CREATE\_DEVICE\_DEBUG** flag when calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function.</span></span> <span data-ttu-id="bc12d-121">Si ejecuta la aplicación con la capa de depuración habilitada, la aplicación será mucho más lenta.</span><span class="sxs-lookup"><span data-stu-id="bc12d-121">If you run your application with the debug layer enabled, the application will be substantially slower.</span></span> <span data-ttu-id="bc12d-122">Sin embargo, para asegurarse de que la aplicación está limpiando los errores y las advertencias antes de enviarlo, utilice la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="bc12d-122">But, to ensure that your application is clean of errors and warnings before you ship it, use the debug layer.</span></span> <span data-ttu-id="bc12d-123">Para obtener más información, vea [usar el nivel de depuración para depurar aplicaciones](using-the-debug-layer-to-test-apps.md).</span><span class="sxs-lookup"><span data-stu-id="bc12d-123">For more info, see [Using the debug layer to debug apps](using-the-debug-layer-to-test-apps.md).</span></span>


> [!Note]  
> <span data-ttu-id="bc12d-124">Para Windows 7 con la actualización de plataforma para Windows 7 (KB2670838) o Windows 8. x, para crear un dispositivo que admita la capa de depuración, instale el kit de desarrollo de software (SDK) de Windows para Windows 8. x para obtener D3D11 \_1SDKLayers.dll.</span><span class="sxs-lookup"><span data-stu-id="bc12d-124">For Windows 7 with Platform Update for Windows 7 (KB2670838) or Windows 8.x, to create a device that supports the debug layer, install the Windows Software Development Kit (SDK) for Windows 8.x to get D3D11\_1SDKLayers.dll.</span></span>


> [!Note]  
> <span data-ttu-id="bc12d-125">En Windows 10, para crear un dispositivo que admita la capa de depuración, habilite la característica opcional "herramientas de gráficos".</span><span class="sxs-lookup"><span data-stu-id="bc12d-125">For Windows 10, to create a device that supports the debug layer, enable the "Graphics Tools" optional feature.</span></span> <span data-ttu-id="bc12d-126">Vaya al panel de configuración, en sistema, aplicaciones & características, administrar características opcionales, agregar una característica y, a continuación, busque "herramientas de gráficos".</span><span class="sxs-lookup"><span data-stu-id="bc12d-126">Go to the Settings panel, under System, Apps & features, Manage optional Features, Add a feature, and then look for "Graphics Tools".</span></span>


> [!Note]  
> <span data-ttu-id="bc12d-127">Para obtener información sobre cómo depurar aplicaciones de DirectX de forma remota, consulte [depuración remota de aplicaciones de DirectX](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span><span class="sxs-lookup"><span data-stu-id="bc12d-127">For info about how to debug DirectX apps remotely, see [Debugging DirectX apps remotely](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).</span></span>

 

<span data-ttu-id="bc12d-128">Como alternativa, puede habilitar o deshabilitar la marca de depuración mediante el [Panel de control de DirectX](/previous-versions//bb219725(v=vs.85)) incluido como parte del SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="bc12d-128">Alternately, you can enable/disable the debug flag using the [DirectX Control Panel](/previous-versions//bb219725(v=vs.85)) included as part of the DirectX SDK.</span></span>

<span data-ttu-id="bc12d-129">Cuando la capa de depuración enumera las pérdidas de memoria, genera una lista de punteros de interfaz de objetos junto con sus nombres descriptivos.</span><span class="sxs-lookup"><span data-stu-id="bc12d-129">When the debug layer lists memory leaks, it outputs a list of object interface pointers along with their friendly names.</span></span> <span data-ttu-id="bc12d-130">El nombre descriptivo predeterminado es "sin &lt; nombre &gt; ".</span><span class="sxs-lookup"><span data-stu-id="bc12d-130">The default friendly name is "&lt;unnamed&gt;".</span></span> <span data-ttu-id="bc12d-131">Puede establecer el nombre descriptivo mediante el método [**ID3D11DeviceChild:: SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) y el GUID **WKPDID \_ D3DDebugObjectName** que se encuentra en D3Dcommon. h.</span><span class="sxs-lookup"><span data-stu-id="bc12d-131">You can set the friendly name by using the [**ID3D11DeviceChild::SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) method and the **WKPDID\_D3DDebugObjectName** GUID that is in D3Dcommon.h.</span></span> <span data-ttu-id="bc12d-132">Por ejemplo, para nombrar pTexture con un nombre de SDKLayer de mytexture.jpg, use el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="bc12d-132">For example, to name pTexture with a SDKLayer name of mytexture.jpg, use the following code:</span></span>


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



<span data-ttu-id="bc12d-133">Normalmente, debe compilar estas llamadas fuera de la versión de producción.</span><span class="sxs-lookup"><span data-stu-id="bc12d-133">Typically, you should compile these calls out of your production version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc12d-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc12d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc12d-135">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="bc12d-135">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 