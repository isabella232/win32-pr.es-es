---
description: Preguntas más frecuentes sobre DirectShow
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: Preguntas más frecuentes sobre DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537498"
---
# <a name="directshow-faq"></a><span data-ttu-id="ee4da-103">Preguntas más frecuentes sobre DirectShow</span><span class="sxs-lookup"><span data-stu-id="ee4da-103">DirectShow FAQ</span></span>

<span data-ttu-id="ee4da-104">En este artículo se responden muchas de las preguntas más frecuentes sobre Microsoft DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ee4da-104">This article answers many frequently asked questions about Microsoft DirectShow.</span></span>

<span data-ttu-id="ee4da-105">**¿Qué sistemas operativos admite DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-105">**What operating systems does DirectShow support?**</span></span>

<span data-ttu-id="ee4da-106">DirectShow está disponible en todas las versiones compatibles de Windows.</span><span class="sxs-lookup"><span data-stu-id="ee4da-106">DirectShow is available in all supported versions of Windows.</span></span>

<span data-ttu-id="ee4da-107">**¿Cuántos conocimientos de COM necesito programar con DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-107">**How much COM knowledge do I need to program with DirectShow?**</span></span>

<span data-ttu-id="ee4da-108">Para el desarrollo de aplicaciones, debe comprender los aspectos básicos del trabajo con objetos COM: Cómo crear una instancia de ellos, acceder a las interfaces que exponen y administrar los recuentos de referencias en esas interfaces.</span><span class="sxs-lookup"><span data-stu-id="ee4da-108">For application development, you need to understand the basics of working with COM objects: how to instantiate them, access the interfaces they expose, and manage reference counts on those interfaces.</span></span> <span data-ttu-id="ee4da-109">El desarrollo de filtros requiere más información sobre COM.</span><span class="sxs-lookup"><span data-stu-id="ee4da-109">Filter development requires more COM knowledge.</span></span>

<span data-ttu-id="ee4da-110">**¿Qué formatos admite DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-110">**What formats does DirectShow support?**</span></span>

<span data-ttu-id="ee4da-111">Vea [formatos admitidos en DirectShow](supported-formats-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="ee4da-111">See [Supported Formats in DirectShow](supported-formats-in-directshow.md).</span></span>

<span data-ttu-id="ee4da-112">**¿Hay una lista de compatibilidad de hardware (HCL) de DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-112">**Is there a DirectShow Hardware Compatibility List (HCL)?**</span></span>

<span data-ttu-id="ee4da-113">No.</span><span class="sxs-lookup"><span data-stu-id="ee4da-113">No.</span></span> <span data-ttu-id="ee4da-114">DirectShow usa las capacidades de hardware de Microsoft DirectDraw y Microsoft DirectSound si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="ee4da-114">DirectShow uses Microsoft DirectDraw and Microsoft DirectSound hardware capabilities if they are available.</span></span> <span data-ttu-id="ee4da-115">Cuando no hay ningún hardware especial disponible, DirectShow usa GDI para dibujar el vídeo  y las \* API multimedia WaveOut para reproducir audio.</span><span class="sxs-lookup"><span data-stu-id="ee4da-115">When no special hardware is available, DirectShow uses GDI to draw video and the **waveOut** \* multimedia APIs to play audio.</span></span>

<span data-ttu-id="ee4da-116">**¿Qué lenguajes puedo usar para escribir una aplicación de DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-116">**What languages can I use to write a DirectShow application?**</span></span>

<span data-ttu-id="ee4da-117">DirectShow está diseñado principalmente para el desarrollo en C++.</span><span class="sxs-lookup"><span data-stu-id="ee4da-117">DirectShow is designed primarily for C++ development.</span></span> <span data-ttu-id="ee4da-118">Un pequeño subconjunto de la API de DirectShow se expone a través de Visual Basic 6,0; sin embargo, esta característica está en desuso.</span><span class="sxs-lookup"><span data-stu-id="ee4da-118">A small sub-set of the DirectShow API is exposed through Visual Basic 6.0; however, this feature is deprecated.</span></span>

<span data-ttu-id="ee4da-119">**¿Se puede acceder a DirectShow a través de código administrado?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-119">**Will DirectShow ever be accessible through managed code?**</span></span>

<span data-ttu-id="ee4da-120">Microsoft no tiene planes actuales para implementar una API de DirectShow administrada.</span><span class="sxs-lookup"><span data-stu-id="ee4da-120">Microsoft has no current plans to implement a managed DirectShow API.</span></span>

<span data-ttu-id="ee4da-121">**¿Qué compilador necesito para el desarrollo de DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-121">**What compiler do I need for DirectShow development?**</span></span>

<span data-ttu-id="ee4da-122">Cualquier compilador capaz de generar objetos del modelo de objetos componentes (COM) debería funcionar una vez que el entorno del compilador se haya configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ee4da-122">Any compiler capable of generating Component Object Model (COM) objects should work once the compiler's environment has been configured correctly.</span></span>

<span data-ttu-id="ee4da-123">**¿Cómo se relaciona DirectShow con Microsoft DirectX?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-123">**How does DirectShow relate to Microsoft DirectX?**</span></span>

<span data-ttu-id="ee4da-124">Internamente, DirectShow usa DirectSound y DirectDraw cuando el hardware lo admite.</span><span class="sxs-lookup"><span data-stu-id="ee4da-124">Internally, DirectShow uses DirectSound and DirectDraw when the hardware supports it.</span></span> <span data-ttu-id="ee4da-125">Los filtros de representador de vídeo y mezclador de superposición usan las superficies DirectDraw 3 y DirectDraw 5.</span><span class="sxs-lookup"><span data-stu-id="ee4da-125">The Video Renderer and Overlay Mixer filters use DirectDraw 3 and DirectDraw 5 surfaces.</span></span> <span data-ttu-id="ee4da-126">El representador de mezcla de vídeo 7 (solo en Windows XP) usa superficies de DirectDraw 7.</span><span class="sxs-lookup"><span data-stu-id="ee4da-126">The Video Mixing Renderer 7 (Windows XP only) uses DirectDraw 7 surfaces.</span></span> <span data-ttu-id="ee4da-127">El representador de vídeo mezclador 9 y el representador de vídeo mejorado usan las API de Microsoft Direct3D más recientes.</span><span class="sxs-lookup"><span data-stu-id="ee4da-127">The Video Mixing Renderer 9 and the Enhanced Video Renderer use the latest Microsoft Direct3D APIs.</span></span> <span data-ttu-id="ee4da-128">No es necesario usar las otras API de DirectX para escribir una aplicación de DirectShow, aunque es posible combinarlas.</span><span class="sxs-lookup"><span data-stu-id="ee4da-128">You do not need to use the other DirectX APIs to write a DirectShow application, although it is possible to combine them.</span></span>

<span data-ttu-id="ee4da-129">**¿Cómo se relaciona DirectShow con Microsoft ActiveMovie?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-129">**How does DirectShow relate to Microsoft ActiveMovie?**</span></span>

<span data-ttu-id="ee4da-130">ActiveMovie era el nombre original de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ee4da-130">ActiveMovie was the original name for DirectShow.</span></span> <span data-ttu-id="ee4da-131">El término ActiveMovie ya no se usa.</span><span class="sxs-lookup"><span data-stu-id="ee4da-131">The term ActiveMovie is no longer used.</span></span>

<span data-ttu-id="ee4da-132">**¿Está disponible el código fuente para la utilidad GraphEdit? ¿Se puede redistribuir GraphEdit?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-132">**Is the source code to the GraphEdit utility available? Can GraphEdit be redistributed?**</span></span>

<span data-ttu-id="ee4da-133">No, el origen no está disponible y Graphedt.exe no es redistribuible.</span><span class="sxs-lookup"><span data-stu-id="ee4da-133">No, the source is not available, and Graphedt.exe is not redistributable.</span></span>

<span data-ttu-id="ee4da-134">**¿Reemplazar DMOs los filtros de DirectShow?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-134">**Do DMOs replace DirectShow filters?**</span></span>

<span data-ttu-id="ee4da-135">Microsoft DirectX media Objects (DMOs) se puede usar en una aplicación de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ee4da-135">Microsoft DirectX Media Objects (DMOs) can be used in a DirectShow application.</span></span> <span data-ttu-id="ee4da-136">En el caso de los codificadores, descodificadores y efectos, se recomienda escribir un DMO en lugar de un filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ee4da-136">For encoders, decoders, and effects, you are encouraged to write a DMO instead of a DirectShow filter.</span></span> <span data-ttu-id="ee4da-137">(Nota: Si desea utilizar la aceleración de vídeo de DirectX en el descodificador, debe implementarla como filtro). Para otros propósitos, es posible que un filtro DirectShow sea más adecuado.</span><span class="sxs-lookup"><span data-stu-id="ee4da-137">(Note: If you want to use DirectX Video Acceleration in your decoder, you must implement it as a filter.) For other purposes, a DirectShow filter might be more appropriate.</span></span> <span data-ttu-id="ee4da-138">Para obtener más información sobre DMOs, vea [objetos multimedia de DirectX](directx-media-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ee4da-138">For more information about DMOs, see [DirectX Media Objects](directx-media-objects.md).</span></span>

<span data-ttu-id="ee4da-139">**Voy a reproducir un archivo de formato AVI con Windows Media Player. Puedo oír el audio, pero no parece que ningún vídeo, sino que solo veo negro. ¿Qué pasa?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-139">**I'm playing an AVI format file with Windows Media Player. I can hear the audio, but there doesn't seem to be any video-instead, I just see black. What's wrong?**</span></span>

<span data-ttu-id="ee4da-140">Probablemente el archivo se ha codificado con un códec que no está presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="ee4da-140">Probably the file was encoded with a codec that is not present on your system.</span></span> <span data-ttu-id="ee4da-141">Aunque el formato de archivo AVI es común, los archivos AVI se pueden crear con muchos formatos de compresión diferentes (códecs).</span><span class="sxs-lookup"><span data-stu-id="ee4da-141">Although the AVI file format is common, AVI files can be created with many different compression formats (codecs).</span></span> <span data-ttu-id="ee4da-142">Si intenta reproducir un archivo AVI que usa un códec no compatible, puede oír el componente de audio, pero el vídeo se mostrará como una pantalla en negro o el contenido de la pantalla permanecerá sin cambios.</span><span class="sxs-lookup"><span data-stu-id="ee4da-142">If you try to play an AVI file that uses an unsupported codec, you might hear the audio component, but the video will display as a black screen or the screen contents will remain unchanged.</span></span>

> [!Note]  
> <span data-ttu-id="ee4da-143">Windows Media Player a menudo intenta descargar e instalar un códec si no está presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="ee4da-143">Windows Media Player often attempts to download and install a codec if it is not present on your system.</span></span>

 

<span data-ttu-id="ee4da-144">**¿Cómo compilar mi aplicación? ¿Qué bibliotecas y archivos de encabezado necesito?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-144">**How do I build my application? What libraries and header files do I need?**</span></span>

<span data-ttu-id="ee4da-145">Vea [configurar el entorno de compilación](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ee4da-145">See [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

<span data-ttu-id="ee4da-146">**GraphEdit muestra muchos filtros que no están documentados. ¿Cuáles son estos filtros?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-146">**GraphEdit displays a lot of filters that aren't documented. What are these filters?**</span></span>

<span data-ttu-id="ee4da-147">GraphEdit enumera todos los filtros que están registrados en el sistema en una categoría de filtro.</span><span class="sxs-lookup"><span data-stu-id="ee4da-147">GraphEdit enumerates all of the filters that are registered on your system in a filter category.</span></span> <span data-ttu-id="ee4da-148">Esto puede incluir filtros instalados por aplicaciones de terceros o instalados por otras tecnologías de Microsoft, como Windows Media o NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="ee4da-148">This might include filters installed by third-party applications, or installed by other Microsoft technologies, such as Windows Media or NetMeeting.</span></span> <span data-ttu-id="ee4da-149">Además, algunos filtros de DirectShow actúan como contenedores para códecs o dispositivos de hardware, donde cada códec o dispositivo aparece como un filtro distinto.</span><span class="sxs-lookup"><span data-stu-id="ee4da-149">Also, some DirectShow filters act as wrappers for codecs or hardware devices, with each codec or device appearing as a distinct filter.</span></span> <span data-ttu-id="ee4da-150">NetMeeting usa el códec de vídeo Microsoft H. 263 y ya no se admite en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ee4da-150">The Microsoft H.263 Video Codec is used by NetMeeting and is no longer supported in DirectShow.</span></span> <span data-ttu-id="ee4da-151">Para obtener más información, vea [enumerar dispositivos y filtros](enumerating-devices-and-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ee4da-151">For more information, see [Enumerating Devices and Filters](enumerating-devices-and-filters.md).</span></span>

<span data-ttu-id="ee4da-152">**Tengo problemas para compilar el gráfico personalizado mediante programación.**</span><span class="sxs-lookup"><span data-stu-id="ee4da-152">**I'm having trouble building my custom graph programmatically.**</span></span>

<span data-ttu-id="ee4da-153">En primer lugar, intente compilar el gráfico de filtro con GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="ee4da-153">First try building the filter graph with GraphEdit.</span></span> <span data-ttu-id="ee4da-154">Esta herramienta le permite simular muchas posibilidades rápidamente.</span><span class="sxs-lookup"><span data-stu-id="ee4da-154">This tool enables you to simulate lots of possibilities quickly.</span></span> <span data-ttu-id="ee4da-155">GraphEdit es siempre un excelente lugar para probar el gráfico antes de intentar compilarlo con el código fuente.</span><span class="sxs-lookup"><span data-stu-id="ee4da-155">GraphEdit is always a great place to test out the graph before attempting to build it with source code.</span></span>

<span data-ttu-id="ee4da-156">Para obtener más información sobre la creación de gráficos, consulte los siguientes artículos:</span><span class="sxs-lookup"><span data-stu-id="ee4da-156">For more information about graph building, see the following articles:</span></span>

-   [<span data-ttu-id="ee4da-157">Compilar el gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="ee4da-157">Building the Filter Graph</span></span>](building-the-filter-graph.md)
-   [<span data-ttu-id="ee4da-158">Enumerar objetos en un gráfico de filtros</span><span class="sxs-lookup"><span data-stu-id="ee4da-158">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)

<span data-ttu-id="ee4da-159">**¿Cómo puedo detectar si DirectShow está instalado en un equipo determinado?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-159">**How can I detect whether DirectShow is installed on a given machine?**</span></span>

<span data-ttu-id="ee4da-160">Llame a **CoCreateInstance** para crear una instancia del administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="ee4da-160">Call **CoCreateInstance** to create an instance of the Filter Graph Manager.</span></span> <span data-ttu-id="ee4da-161">Si la llamada se realiza correctamente, DirectShow se instala en la máquina.</span><span class="sxs-lookup"><span data-stu-id="ee4da-161">If this call succeeds, DirectShow is installed on the machine.</span></span> <span data-ttu-id="ee4da-162">El código siguiente muestra cómo hacerlo:</span><span class="sxs-lookup"><span data-stu-id="ee4da-162">The following code shows how to do this:</span></span>


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



<span data-ttu-id="ee4da-163">**Cómo cambiar la configuración de un filtro sin mostrar la página de propiedades**</span><span class="sxs-lookup"><span data-stu-id="ee4da-163">**How do I change a filter's settings without displaying the property page?**</span></span>

<span data-ttu-id="ee4da-164">La mayoría de los filtros exponen una o más interfaces para establecer las propiedades del filtro.</span><span class="sxs-lookup"><span data-stu-id="ee4da-164">Most filters expose one or more interfaces for setting properties on the filter.</span></span> <span data-ttu-id="ee4da-165">Consulte la página de referencia del filtro en cuestión.</span><span class="sxs-lookup"><span data-stu-id="ee4da-165">Consult the reference page for the filter in question.</span></span> <span data-ttu-id="ee4da-166">(Consulte [filtros de DirectShow](directshow-filters.md)).</span><span class="sxs-lookup"><span data-stu-id="ee4da-166">(See [DirectShow Filters](directshow-filters.md).)</span></span>

<span data-ttu-id="ee4da-167">**¿Puedo probar el filtro con GraphEdit?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-167">**Can I test my filter with GraphEdit?**</span></span>

<span data-ttu-id="ee4da-168">Mientras desarrolla un filtro, GraphEdit puede ayudarle a visualizar las conexiones entre los filtros.</span><span class="sxs-lookup"><span data-stu-id="ee4da-168">While you are developing a filter, GraphEdit can help you to visualize the connections between filters.</span></span> <span data-ttu-id="ee4da-169">También puede proporcionar una prueba rápida de la funcionalidad de un filtro.</span><span class="sxs-lookup"><span data-stu-id="ee4da-169">It can also provide a quick test of a filter's functionality.</span></span> <span data-ttu-id="ee4da-170">Sin embargo, no está pensada como una plataforma de prueba sólida.</span><span class="sxs-lookup"><span data-stu-id="ee4da-170">However, it is not meant as a robust test platform.</span></span>

<span data-ttu-id="ee4da-171">**¿Dónde se ejecutan los filtros de timbre de privilegios?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-171">**At what privilege ring do filters run?**</span></span>

<span data-ttu-id="ee4da-172">Los filtros se ejecutan en el anillo 3, aunque algunos filtros controlan los dispositivos de streaming que se ejecutan en anillo 0.</span><span class="sxs-lookup"><span data-stu-id="ee4da-172">Filters run at ring 3, although some filters control streaming devices that run at ring 0.</span></span> <span data-ttu-id="ee4da-173">Para obtener más información, vea [Cómo participan los dispositivos de hardware en el gráfico de filtro](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="ee4da-173">For more information, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>

<span data-ttu-id="ee4da-174">**¿Es necesario usar un depurador de kernel?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-174">**Do I need to use a kernel debugger?**</span></span>

<span data-ttu-id="ee4da-175">Depende de su proyecto específico.</span><span class="sxs-lookup"><span data-stu-id="ee4da-175">That depends on your specific project.</span></span> <span data-ttu-id="ee4da-176">La instalación de las bibliotecas en tiempo de ejecución de depuración de DirectX significa que está instalando controladores de depuración y otros componentes de modo kernel, y que si la aplicación provoca una aserción de depuración en uno de estos componentes, el equipo se reiniciará automáticamente a menos que tenga un depurador de kernel asociado al proceso.</span><span class="sxs-lookup"><span data-stu-id="ee4da-176">Installing the DirectX debug runtime libraries means that you are installing debug drivers and other kernel mode components, and that if your application causes a debug assert in one of these components, your machine will automatically reboot unless you have a kernel debugger attached to your process.</span></span>

<span data-ttu-id="ee4da-177">**Cuando ejecuto mi aplicación en el depurador, se bloquea.**</span><span class="sxs-lookup"><span data-stu-id="ee4da-177">**When I run my application in the debugger, it crashes.**</span></span>

<span data-ttu-id="ee4da-178">Algunos descodificadores están diseñados para no funcionar mientras la aplicación está asociada al depurador.</span><span class="sxs-lookup"><span data-stu-id="ee4da-178">Some decoders are designed not to work while the application is attached to the debugger.</span></span> <span data-ttu-id="ee4da-179">Intente ejecutar la aplicación fuera del depurador.</span><span class="sxs-lookup"><span data-stu-id="ee4da-179">Try running the application outside the debugger.</span></span>

<span data-ttu-id="ee4da-180">**¿Cómo funciona la macro de definición de \_ GUID?**</span><span class="sxs-lookup"><span data-stu-id="ee4da-180">**How does the DEFINE\_GUID macro work?**</span></span>

<span data-ttu-id="ee4da-181">La macro **definir \_ GUID** resuelve el problema de declarar `extern` referencias a valores GUID en el código fuente.</span><span class="sxs-lookup"><span data-stu-id="ee4da-181">The **DEFINE\_GUID** macro solves the problem of declaring `extern` references to GUID values in your source code.</span></span> <span data-ttu-id="ee4da-182">Por ejemplo, supongamos que el proyecto tiene tres archivos de código fuente, Src1. cpp, Src2. cpp y Src3. cpp, y los tres archivos usan un determinado valor de GUID que ha definido.</span><span class="sxs-lookup"><span data-stu-id="ee4da-182">For example, suppose that your project has three source files, Src1.cpp, Src2.cpp, and Src3.cpp, and all three files use a certain GUID value that you have defined.</span></span> <span data-ttu-id="ee4da-183">El valor GUID debe definirse exactamente una vez en el proyecto y los otros archivos de código fuente deben declarar `extern` referencias a él.</span><span class="sxs-lookup"><span data-stu-id="ee4da-183">The GUID value must be defined exactly once in your project, and the other source files must declare `extern` references to it.</span></span> <span data-ttu-id="ee4da-184">Con la macro **definir \_ GUID** , puede usar el mismo archivo de encabezado para ambos propósitos.</span><span class="sxs-lookup"><span data-stu-id="ee4da-184">With the **DEFINE\_GUID** macro, you can use the same header file for both purposes.</span></span> <span data-ttu-id="ee4da-185">En el archivo de encabezado, declare el GUID de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ee4da-185">In your header file, declare the GUID as follows:</span></span>


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



<span data-ttu-id="ee4da-186">(Si este ejemplo tiene ceros, coloque los valores reales de GUID). Puede usar la utilidad Guidgen.exe para crear un nuevo GUID y pegarlo en el archivo de encabezado en el formato de **\_ GUID de definición** .</span><span class="sxs-lookup"><span data-stu-id="ee4da-186">(Where this example has zeroes, put the actual GUID values.) You can use the Guidgen.exe utility to create a new GUID and paste it into the header file in the **DEFINE\_GUID** format.</span></span> <span data-ttu-id="ee4da-187">Incluya este archivo de encabezado en cada archivo de código fuente que haga referencia al GUID.</span><span class="sxs-lookup"><span data-stu-id="ee4da-187">Include this header file in every source file that references the GUID.</span></span> <span data-ttu-id="ee4da-188">En exactamente uno de los archivos de código fuente, incluya el archivo de encabezado Initguid. h delante del archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="ee4da-188">In exactly one of the source files, include the header file Initguid.h before your header file.</span></span> <span data-ttu-id="ee4da-189">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="ee4da-189">For example:</span></span>


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



<span data-ttu-id="ee4da-190">Siempre que no se incluya el archivo de encabezado Initguid. h, la macro **definir \_ GUID** crea una `extern` referencia al valor GUID.</span><span class="sxs-lookup"><span data-stu-id="ee4da-190">Wherever the Initguid.h header file is not included, the **DEFINE\_GUID** macro creates an `extern` reference to the GUID value.</span></span> <span data-ttu-id="ee4da-191">Cuando se incluye el archivo de encabezado Initguid. h, se vuelve a definir la macro **definir \_ GUID** para que **definir \_ GUID** cree una declaración de definición del GUID.</span><span class="sxs-lookup"><span data-stu-id="ee4da-191">When the Initguid.h header file is included, it redefines the **DEFINE\_GUID** macro so that **DEFINE\_GUID** creates a defining declaration of the GUID.</span></span>

<span data-ttu-id="ee4da-192">Si no incluye Initguid. h en ninguno de los archivos de código fuente, obtendrá un error de vínculo "símbolo externo sin resolver".</span><span class="sxs-lookup"><span data-stu-id="ee4da-192">If you do not include Initguid.h in any of the source files, you will get a link error "unresolved external symbol."</span></span> <span data-ttu-id="ee4da-193">Si incluye dos veces Initguid. h para el mismo GUID, obtendrá un error de compilación "redefinición; inicialización múltiple ".</span><span class="sxs-lookup"><span data-stu-id="ee4da-193">If you include Initguid.h twice for the same GUID, you will get a compile error "redefinition; multiple initialization."</span></span> <span data-ttu-id="ee4da-194">Para resolver estos errores, asegúrese de que Initguid. h se incluye exactamente una vez.</span><span class="sxs-lookup"><span data-stu-id="ee4da-194">To resolve these errors, make sure that Initguid.h is included exactly once.</span></span> <span data-ttu-id="ee4da-195">Además, no incluya Initguid. h dentro de un archivo de encabezado precompilado, porque en efecto el encabezado precompilado se incluye en todos los archivos de código fuente.</span><span class="sxs-lookup"><span data-stu-id="ee4da-195">Also, do not include Initguid.h inside a precompiled header file, because in effect the precompiled header is included in every source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee4da-196">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee4da-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee4da-197">Introducción a DirectShow</span><span class="sxs-lookup"><span data-stu-id="ee4da-197">Introduction to DirectShow</span></span>](introduction-to-directshow.md)
</dt> </dl>

 

 



