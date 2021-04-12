---
title: Usar Direct2D para la representación de Server-Side
description: Describe el uso de Direct2D para la representación del lado servidor.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, representación del lado servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420835"
---
# <a name="using-direct2d-for-server-side-rendering"></a><span data-ttu-id="59ba7-104">Usar Direct2D para la representación de Server-Side</span><span class="sxs-lookup"><span data-stu-id="59ba7-104">Using Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="59ba7-105">Direct2D es adecuado para aplicaciones gráficas que requieren la representación del lado servidor en Windows Server.</span><span class="sxs-lookup"><span data-stu-id="59ba7-105">Direct2D is well-suited for graphics applications that require server-side rendering on Windows Server.</span></span> <span data-ttu-id="59ba7-106">En esta información general se describen los aspectos básicos del uso de Direct2D para la representación del lado servidor.</span><span class="sxs-lookup"><span data-stu-id="59ba7-106">This overview describes the basics of using Direct2D for server-side rendering.</span></span> <span data-ttu-id="59ba7-107">Contiene las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="59ba7-107">It contains the following sections:</span></span>

-   [<span data-ttu-id="59ba7-108">Requisitos para la representación de Server-Side</span><span class="sxs-lookup"><span data-stu-id="59ba7-108">Requirements for Server-Side Rendering</span></span>](#requirements-for-server-side-rendering)
-   [<span data-ttu-id="59ba7-109">Opciones para las API disponibles</span><span class="sxs-lookup"><span data-stu-id="59ba7-109">Options for Available APIs</span></span>](#options-for-available-apis)
    -   [<span data-ttu-id="59ba7-110">GDI</span><span class="sxs-lookup"><span data-stu-id="59ba7-110">GDI</span></span>](#gdi)
    -   [<span data-ttu-id="59ba7-111">GDI+</span><span class="sxs-lookup"><span data-stu-id="59ba7-111">GDI+</span></span>](#gdi)
    -   [<span data-ttu-id="59ba7-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="59ba7-112">Direct2D</span></span>](#using-direct2d-for-server-side-rendering)
-   [<span data-ttu-id="59ba7-113">Cómo usar Direct2D para la representación de Server-Side</span><span class="sxs-lookup"><span data-stu-id="59ba7-113">How to Use Direct2D for Server-Side Rendering</span></span>](#how-to-use-direct2d-for-server-side-rendering)
    -   [<span data-ttu-id="59ba7-114">Representación de software</span><span class="sxs-lookup"><span data-stu-id="59ba7-114">Software Rendering</span></span>](#software-rendering)
    -   [<span data-ttu-id="59ba7-115">Multithreading</span><span class="sxs-lookup"><span data-stu-id="59ba7-115">Multithreading</span></span>](#multithreading)
    -   [<span data-ttu-id="59ba7-116">Generar un archivo de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="59ba7-116">Generating a Bitmap File</span></span>](#generating-a-bitmap-file)
-   [<span data-ttu-id="59ba7-117">Conclusión</span><span class="sxs-lookup"><span data-stu-id="59ba7-117">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="59ba7-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59ba7-118">Related topics</span></span>](#related-topics)

## <a name="requirements-for-server-side-rendering"></a><span data-ttu-id="59ba7-119">Requisitos para la representación de Server-Side</span><span class="sxs-lookup"><span data-stu-id="59ba7-119">Requirements for Server-Side Rendering</span></span>

<span data-ttu-id="59ba7-120">A continuación se muestra un escenario típico para un servidor de gráficos: los gráficos y los gráficos se representan en un servidor y se entregan como mapas de bits en respuesta a las solicitudes Web.</span><span class="sxs-lookup"><span data-stu-id="59ba7-120">The following is a typical scenario for a chart server: charts and graphics are rendered on a server and delivered as bitmaps in response to Web requests.</span></span> <span data-ttu-id="59ba7-121">El servidor puede estar equipado con una tarjeta gráfica de low-end o sin tarjeta gráfica.</span><span class="sxs-lookup"><span data-stu-id="59ba7-121">The server might be equipped with a low-end graphics card or no graphics card at all.</span></span>

<span data-ttu-id="59ba7-122">Este escenario revela tres requisitos de aplicación.</span><span class="sxs-lookup"><span data-stu-id="59ba7-122">This scenario reveals three application requirements.</span></span> <span data-ttu-id="59ba7-123">En primer lugar, la aplicación debe controlar varias solicitudes simultáneas de forma eficaz, especialmente en los servidores de varios núcleos.</span><span class="sxs-lookup"><span data-stu-id="59ba7-123">First, the application must handle multiple concurrent requests efficiently, especially on multicore servers.</span></span> <span data-ttu-id="59ba7-124">En segundo lugar, la aplicación debe usar la representación de software cuando se ejecuta en servidores con una tarjeta gráfica de low-end o sin tarjeta gráfica.</span><span class="sxs-lookup"><span data-stu-id="59ba7-124">Second, the application must use software rendering when running on servers with a low-end graphics card or no graphics card.</span></span> <span data-ttu-id="59ba7-125">Por último, la aplicación debe ejecutarse como un servicio en la sesión 0 para que no sea necesario que un usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="59ba7-125">Finally, the application must run as a service in Session 0 so that it does not require a user to be logged in.</span></span> <span data-ttu-id="59ba7-126">Para obtener más información acerca de la sesión 0, vea [impacto del aislamiento de sesión 0 en servicios y controladores en Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span><span class="sxs-lookup"><span data-stu-id="59ba7-126">For more information about Session 0, see [Impact of Session 0 Isolation on Services and Drivers in Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span></span>

## <a name="options-for-available-apis"></a><span data-ttu-id="59ba7-127">Opciones para las API disponibles</span><span class="sxs-lookup"><span data-stu-id="59ba7-127">Options for Available APIs</span></span>

<span data-ttu-id="59ba7-128">Hay tres opciones para la representación del lado servidor: GDI, GDI+ y Direct2D.</span><span class="sxs-lookup"><span data-stu-id="59ba7-128">There are three options for server-side rendering: GDI, GDI+ and Direct2D.</span></span> <span data-ttu-id="59ba7-129">Como GDI y GDI+, Direct2D es una API de representación de 2D nativa que proporciona a las aplicaciones un mayor control sobre el uso de los dispositivos de gráficos.</span><span class="sxs-lookup"><span data-stu-id="59ba7-129">Like GDI and GDI+, Direct2D is a native 2D rendering API that gives applications more control over the use of graphics devices.</span></span> <span data-ttu-id="59ba7-130">Además, Direct2D es compatible de forma exclusiva con un generador multiproceso y un único subproceso.</span><span class="sxs-lookup"><span data-stu-id="59ba7-130">In addition, Direct2D uniquely supports a single-threaded and a multithreaded factory.</span></span> <span data-ttu-id="59ba7-131">En las secciones siguientes se comparan todas las API en términos de dibujo de calidad y representación en el lado servidor multiproceso.</span><span class="sxs-lookup"><span data-stu-id="59ba7-131">The following sections compare each API in terms of drawing qualities and multithreaded server-side rendering.</span></span>

### <a name="gdi"></a><span data-ttu-id="59ba7-132">GDI</span><span class="sxs-lookup"><span data-stu-id="59ba7-132">GDI</span></span>

<span data-ttu-id="59ba7-133">A diferencia de Direct2D y GDI+, GDI no admite características de dibujo de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="59ba7-133">Unlike Direct2D and GDI+, GDI does not support high-quality drawing features.</span></span> <span data-ttu-id="59ba7-134">Por ejemplo, GDI no admite el suavizado de contorno para crear líneas suaves y solo tiene compatibilidad limitada con la transparencia.</span><span class="sxs-lookup"><span data-stu-id="59ba7-134">For instance, GDI does not support antialiasing for creating smooth lines and has only limited support for transparency.</span></span> <span data-ttu-id="59ba7-135">En función de los resultados de las pruebas de rendimiento de gráficos en Windows 7 y Windows Server 2008 R2, Direct2D se escala de forma más eficaz que GDI, a pesar del rediseño de los bloqueos en GDI.</span><span class="sxs-lookup"><span data-stu-id="59ba7-135">Based on the graphics performance test results on Windows 7 and Windows Server 2008 R2, Direct2D scales more efficiently than GDI, despite the redesign of locks in GDI.</span></span> <span data-ttu-id="59ba7-136">Para obtener más información acerca de estos resultados de pruebas, vea [Engineering Windows 7 Graphics performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span><span class="sxs-lookup"><span data-stu-id="59ba7-136">For more information about these test results, see [Engineering Windows 7 Graphics Performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span></span>

<span data-ttu-id="59ba7-137">Además, las aplicaciones que usan GDI se limitan a los identificadores de GDI 10240 por proceso y 65536 a los identificadores de GDI por sesión.</span><span class="sxs-lookup"><span data-stu-id="59ba7-137">In addition, applications using GDI are limited to 10240 GDI handles per process and 65536 GDI handles per session.</span></span> <span data-ttu-id="59ba7-138">La razón es que internamente Windows usa una palabra de 16 bits para almacenar el índice de identificadores de cada sesión.</span><span class="sxs-lookup"><span data-stu-id="59ba7-138">The reason is that internally Windows uses a 16-bit WORD to store the index of handles for each session.</span></span>

### <a name="gdi"></a><span data-ttu-id="59ba7-139">GDI+</span><span class="sxs-lookup"><span data-stu-id="59ba7-139">GDI+</span></span>

<span data-ttu-id="59ba7-140">Aunque GDI+ admite el suavizado de contorno y la combinación alfa para el dibujo de alta calidad, el problema principal con GDI+ para los escenarios de servidor es que no admite la ejecución en la sesión 0.</span><span class="sxs-lookup"><span data-stu-id="59ba7-140">While GDI+ supports antialiasing and alpha blending for high-quality drawing, the main problem with GDI+ for server-scenarios is that it does not support running in Session 0.</span></span> <span data-ttu-id="59ba7-141">Dado que la sesión 0 solo admite la funcionalidad no interactiva, las funciones que interactúan directa o indirectamente con los dispositivos de pantalla recibirán errores.</span><span class="sxs-lookup"><span data-stu-id="59ba7-141">Since Session 0 only supports non-interactive functionality, functions that directly or indirectly interact with display devices will therefore receive errors.</span></span> <span data-ttu-id="59ba7-142">Algunos ejemplos específicos de funciones son no solo aquellos que se ocupan de mostrar los dispositivos, sino que también se ocupan indirectamente de los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="59ba7-142">Specific examples of functions include not only those dealing with display devices, but also those indirectly dealing with device drivers.</span></span>

<span data-ttu-id="59ba7-143">De forma similar a GDI, GDI+ está limitado por su mecanismo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="59ba7-143">Similar to GDI, GDI+ is limited by its locking mechanism.</span></span> <span data-ttu-id="59ba7-144">Los mecanismos de bloqueo en GDI+ son los mismos en Windows 7 y Windows Server 2008 R2, como en las versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="59ba7-144">The locking mechanisms in GDI+ are the same in Windows 7 and Windows Server 2008 R2 as in previous versions.</span></span>

### <a name="direct2d"></a><span data-ttu-id="59ba7-145">Direct2D</span><span class="sxs-lookup"><span data-stu-id="59ba7-145">Direct2D</span></span>

<span data-ttu-id="59ba7-146">Direct2D es una API de gráficos 2D de modo inmediato y con aceleración de hardware que proporciona alto rendimiento y representación de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="59ba7-146">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering.</span></span> <span data-ttu-id="59ba7-147">Ofrece una fábrica de un solo subproceso y un generador multiproceso y el escalado lineal de la representación de software específica del curso.</span><span class="sxs-lookup"><span data-stu-id="59ba7-147">It offers a single-threaded and a multithreaded factory and the linear scaling of course-grained software rendering.</span></span>

<span data-ttu-id="59ba7-148">Para ello, Direct2D define una interfaz de fábrica raíz.</span><span class="sxs-lookup"><span data-stu-id="59ba7-148">To do this, Direct2D defines a root factory interface.</span></span> <span data-ttu-id="59ba7-149">Como norma general, un objeto creado en un generador solo se puede usar con otros objetos creados desde el mismo generador.</span><span class="sxs-lookup"><span data-stu-id="59ba7-149">As a rule, an object created on a factory can only be used with other objects created from the same factory.</span></span> <span data-ttu-id="59ba7-150">El autor de la llamada puede solicitar un generador de un solo subproceso o multiproceso cuando se crea.</span><span class="sxs-lookup"><span data-stu-id="59ba7-150">The caller can request either a single-threaded or a multithreaded factory when it is created.</span></span> <span data-ttu-id="59ba7-151">Si se solicita un generador de un solo subproceso, no se realiza ningún bloqueo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="59ba7-151">If a single-threaded factory is requested, then no locking of threads is performed.</span></span> <span data-ttu-id="59ba7-152">Si el autor de la llamada solicita un generador multiproceso, se adquiere un bloqueo de subprocesos en toda la fábrica siempre que se realiza una llamada a Direct2D.</span><span class="sxs-lookup"><span data-stu-id="59ba7-152">If the caller requests a multithreaded factory, then, a factory-wide thread lock is acquired whenever a call is made into Direct2D.</span></span>

<span data-ttu-id="59ba7-153">Además, el bloqueo de subprocesos en Direct2D es más granular que en GDI y GDI+, de modo que el aumento del número de subprocesos tiene un impacto mínimo en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="59ba7-153">In addition, the locking of threads in Direct2D is more granular than in GDI and GDI+, so that the increase of the number of threads has minimal impact on the performance.</span></span>

## <a name="how-to-use-direct2d-for-server-side-rendering"></a><span data-ttu-id="59ba7-154">Cómo usar Direct2D para la representación de Server-Side</span><span class="sxs-lookup"><span data-stu-id="59ba7-154">How to Use Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="59ba7-155">En las secciones siguientes se describe cómo usar la representación de software, cómo usar óptimamente un generador de un solo subproceso y multiproceso, y cómo dibujar y guardar un dibujo complejo en un archivo.</span><span class="sxs-lookup"><span data-stu-id="59ba7-155">The following sections describe how to use software rendering, how to optimally use a single-threaded and a multithreaded factory, and how to draw and save a complex drawing to a file.</span></span>

### <a name="software-rendering"></a><span data-ttu-id="59ba7-156">Representación de software</span><span class="sxs-lookup"><span data-stu-id="59ba7-156">Software Rendering</span></span>

<span data-ttu-id="59ba7-157">Las aplicaciones de servidor usan la representación de software mediante la creación del destino de representación de [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , con el tipo de destino de representación establecido en D2D1 \_ representar el software de \_ \_ tipo destino \_ o D2D1 \_ representar \_ \_ \_ el tipo de destino predeterminado.</span><span class="sxs-lookup"><span data-stu-id="59ba7-157">Server-side applications use software rendering by creating [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target, with the render target type set to either D2D1\_RENDER\_TARGET\_TYPE\_SOFTWARE or D2D1\_RENDER\_TARGET\_TYPE\_DEFAULT.</span></span> <span data-ttu-id="59ba7-158">Para obtener más información sobre los destinos de representación de [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , vea el método [**ID2D1Factory:: CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) . para obtener más información sobre los tipos de destino de representación, vea [**D2D1 \_ Render \_ target \_ Type**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span><span class="sxs-lookup"><span data-stu-id="59ba7-158">For more information about [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render targets, see the [**ID2D1Factory::CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) method; for more information about the render target types, see [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span></span>

### <a name="multithreading"></a><span data-ttu-id="59ba7-159">Subprocesamiento múltiple</span><span class="sxs-lookup"><span data-stu-id="59ba7-159">Multithreading</span></span>

<span data-ttu-id="59ba7-160">Saber cómo crear y compartir factorías y representar destinos entre subprocesos puede afectar significativamente al rendimiento de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="59ba7-160">Knowing how to create and share factories and render targets across threads can significantly impact the performance of an application.</span></span> <span data-ttu-id="59ba7-161">Las tres figuras siguientes muestran tres enfoques variados.</span><span class="sxs-lookup"><span data-stu-id="59ba7-161">The following three figures show three varied approaches.</span></span> <span data-ttu-id="59ba7-162">El enfoque óptimo se muestra en la figura 3.</span><span class="sxs-lookup"><span data-stu-id="59ba7-162">The optimal approach is shown in figure 3.</span></span>

![diagrama multithreading de direct2d con un solo destino de representación.](images/server-side-rendering-1.png)

<span data-ttu-id="59ba7-164">En la figura 1, los distintos subprocesos comparten el mismo generador y el mismo destino de representación.</span><span class="sxs-lookup"><span data-stu-id="59ba7-164">In figure 1, different threads share the same factory and the same render target.</span></span> <span data-ttu-id="59ba7-165">Este enfoque puede provocar resultados imprevisibles en casos en los que varios subprocesos cambian simultáneamente el estado del destino de representación compartido, como establecer simultáneamente la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="59ba7-165">This approach can lead to unpredictable results in cases when multiple threads simultaneously change the state of the shared render target, such as simultaneously setting the transformation matrix.</span></span> <span data-ttu-id="59ba7-166">Dado que el bloqueo interno en Direct2D no sincroniza un recurso compartido, como los destinos de representación, este enfoque puede provocar un error en la llamada [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) en el subproceso 1, porque en el subproceso 2, la llamada **beginDraw** ya está usando el destino de representación compartido.</span><span class="sxs-lookup"><span data-stu-id="59ba7-166">As the internal locking in Direct2D does not synchronize a shared resource such as render targets, this approach can cause the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) call to fail in thread 1, because in thread 2, the **BeginDraw** call is already using the shared render target.</span></span>

![diagrama multithreading de direct2d con varios destinos de representación.](images/server-side-rendering-2.png)

<span data-ttu-id="59ba7-168">Para evitar los resultados imprevisibles encontrados en la figura 1, la figura 2 muestra un generador multiproceso con cada subproceso que tiene su propio destino de representación.</span><span class="sxs-lookup"><span data-stu-id="59ba7-168">To avoid the unpredictable results encountered in figure 1, figure 2 shows a multithreaded factory with each thread having its own render target.</span></span> <span data-ttu-id="59ba7-169">Este enfoque funciona, pero funciona eficazmente como una aplicación de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="59ba7-169">This approach works but it effectively functions as a single-threaded application.</span></span> <span data-ttu-id="59ba7-170">La razón es que el bloqueo de toda la fábrica solo se aplica al nivel de operación de dibujo y todas las llamadas de dibujo del mismo generador se serializan en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="59ba7-170">The reason is that the factory-wide lock applies only to the drawing-operation level and all the drawing calls in the same factory consequently are serialized.</span></span> <span data-ttu-id="59ba7-171">Como resultado, el subproceso 1 se bloquea al intentar entrar en una llamada de dibujo, mientras que el subproceso 2 se encuentra en medio de ejecutar otra llamada de dibujo.</span><span class="sxs-lookup"><span data-stu-id="59ba7-171">As a result, thread 1 becomes blocked when trying to enter a drawing call, while thread 2 is in the middle of executing another drawing call.</span></span>

![diagrama multithreading de direct2d con varios generadores y varios destinos de representación.](images/server-side-rendering-3.png)

<span data-ttu-id="59ba7-173">En la figura 3 se muestra el enfoque óptimo, donde se usan un generador de un solo subproceso y un destino de representación de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="59ba7-173">Figure 3 shows the optimal approach, where a single-threaded factory and a single-threaded render target are used.</span></span> <span data-ttu-id="59ba7-174">Dado que no se realiza ningún bloqueo cuando se usa un generador de un solo subproceso, las operaciones de dibujo de cada subproceso se pueden ejecutar simultáneamente para lograr un rendimiento óptimo.</span><span class="sxs-lookup"><span data-stu-id="59ba7-174">Since no locking is performed when using a single-threaded factory, drawing operations in each thread can run concurrently to achieve optimal performance.</span></span>

### <a name="generating-a-bitmap-file"></a><span data-ttu-id="59ba7-175">Generar un archivo de mapa de bits</span><span class="sxs-lookup"><span data-stu-id="59ba7-175">Generating a Bitmap File</span></span>

<span data-ttu-id="59ba7-176">Para generar un archivo de mapa de bits mediante la representación de software, use un destino de representación de [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="59ba7-176">To generate a bitmap file using software rendering, use an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="59ba7-177">Use un [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) para escribir el mapa de bits en un archivo.</span><span class="sxs-lookup"><span data-stu-id="59ba7-177">Use an [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) to write the bitmap to a file.</span></span> <span data-ttu-id="59ba7-178">Use [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) para codificar el mapa de bits en un formato de imagen especificado.</span><span class="sxs-lookup"><span data-stu-id="59ba7-178">Use [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap into a specified image format.</span></span> <span data-ttu-id="59ba7-179">En el ejemplo de código siguiente se muestra cómo dibujar y guardar la siguiente imagen en un archivo.</span><span class="sxs-lookup"><span data-stu-id="59ba7-179">The following code example shows how to draw and save the following image to a file.</span></span>

![imagen de salida de ejemplo.](images/saveasimagefile-sample.png)

<span data-ttu-id="59ba7-181">En primer lugar, este ejemplo de código crea un [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) y un destino de representación [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="59ba7-181">This code example first creates an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) and an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="59ba7-182">Después representa un dibujo con texto, una geometría de trazado que representa un reloj de hora y un cristal de hora transformada en un mapa de bits de WIC.</span><span class="sxs-lookup"><span data-stu-id="59ba7-182">It then renders a drawing with some text, a path geometry representing an hour glass, and a transformed hour glass into a WIC bitmap.</span></span> <span data-ttu-id="59ba7-183">A continuación, usa [IWICStream:: InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) para guardar el mapa de bits en un archivo.</span><span class="sxs-lookup"><span data-stu-id="59ba7-183">It then uses [IWICStream::InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) to save the bitmap to a file.</span></span> <span data-ttu-id="59ba7-184">Si su aplicación necesita guardar el mapa de bits en la memoria, use [IWICStream:: InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="59ba7-184">If your application needs to save the bitmap in memory, use [IWICStream::InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) instead.</span></span> <span data-ttu-id="59ba7-185">Por último, usa [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) para codificar el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="59ba7-185">Finally, it uses [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap.</span></span>


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a><span data-ttu-id="59ba7-186">Conclusión</span><span class="sxs-lookup"><span data-stu-id="59ba7-186">Conclusion</span></span>

<span data-ttu-id="59ba7-187">Tal y como se muestra en el apartado anterior, el uso de Direct2D para la representación del lado servidor es sencillo y sencillo.</span><span class="sxs-lookup"><span data-stu-id="59ba7-187">As seen from the above, using Direct2D for server-side rendering is simple and straightforward.</span></span> <span data-ttu-id="59ba7-188">Además, proporciona una representación de alta calidad y alta pueden paralelizar que se puede ejecutar en entornos con privilegios bajos del servidor.</span><span class="sxs-lookup"><span data-stu-id="59ba7-188">In addition, it provides high quality and highly parallelizable rendering that can run in low-privilege environments of the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59ba7-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="59ba7-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59ba7-190">Referencia de Direct2D</span><span class="sxs-lookup"><span data-stu-id="59ba7-190">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 