---
description: La compresión de bloque es una técnica de compresión de textura para reducir el tamaño de la textura.
ms.assetid: add98d8f-6846-4dd6-b0e2-a4b6e89cbcc5
title: Compresión de bloques (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fcfb4bc91256415ab23686b7333df7d21df335d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570873"
---
# <a name="block-compression-direct3d-10"></a><span data-ttu-id="5e473-103">Compresión de bloques (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5e473-103">Block Compression (Direct3D 10)</span></span>

<span data-ttu-id="5e473-104">La compresión de bloque es una técnica de compresión de textura para reducir el tamaño de la textura.</span><span class="sxs-lookup"><span data-stu-id="5e473-104">Block compression is a texture compression technique for reducing texture size.</span></span> <span data-ttu-id="5e473-105">Cuando se comparan con una textura con 32 bits por color, una textura comprimida en bloque puede tener un tamaño de hasta un 75% inferior.</span><span class="sxs-lookup"><span data-stu-id="5e473-105">When compared to a texture with 32-bits per color, a block-compressed texture can be up to 75 percent smaller.</span></span> <span data-ttu-id="5e473-106">Las aplicaciones normalmente ven un aumento del rendimiento cuando se usa la compresión de bloques debido a la menor superficie de memoria.</span><span class="sxs-lookup"><span data-stu-id="5e473-106">Applications usually see a performance increase when using block compression because of the smaller memory footprint.</span></span>

<span data-ttu-id="5e473-107">Aunque la pérdida, la compresión de bloque funciona bien y se recomienda para todas las texturas que se transforman y filtran por la canalización.</span><span class="sxs-lookup"><span data-stu-id="5e473-107">While lossy, block compression works well and is recommended for all textures that get transformed and filtered by the pipeline.</span></span> <span data-ttu-id="5e473-108">Las texturas que se asignan directamente a la pantalla (elementos de la interfaz de usuario como iconos y texto) no son buenas opciones de compresión porque los artefactos son más evidentes.</span><span class="sxs-lookup"><span data-stu-id="5e473-108">Textures that are directly mapped to the screen (UI elements like icons and text) are not good choices for compression because artifacts are more noticeable.</span></span>

<span data-ttu-id="5e473-109">Una textura comprimida en bloques debe crearse como un múltiplo del tamaño 4 en todas las dimensiones y no se puede usar como salida de la canalización.</span><span class="sxs-lookup"><span data-stu-id="5e473-109">A block-compressed texture must be created as a multiple of size 4 in all dimensions and cannot be used as an output of the pipeline.</span></span>

-   [<span data-ttu-id="5e473-110">¿Cómo funciona la compresión de bloque?</span><span class="sxs-lookup"><span data-stu-id="5e473-110">How Does Block Compression Work?</span></span>](#how-does-block-compression-work)
    -   [<span data-ttu-id="5e473-111">Almacenar datos sin comprimir</span><span class="sxs-lookup"><span data-stu-id="5e473-111">Storing Uncompressed Data</span></span>](#storing-uncompressed-data)
    -   [<span data-ttu-id="5e473-112">Almacenar datos comprimidos</span><span class="sxs-lookup"><span data-stu-id="5e473-112">Storing Compressed Data</span></span>](#storing-compressed-data)
-   [<span data-ttu-id="5e473-113">Usar la compresión de bloque</span><span class="sxs-lookup"><span data-stu-id="5e473-113">Using Block Compression</span></span>](#using-block-compression)
    -   [<span data-ttu-id="5e473-114">Tamaño virtual frente al tamaño físico</span><span class="sxs-lookup"><span data-stu-id="5e473-114">Virtual Size versus Physical Size</span></span>](#virtual-size-versus-physical-size)
-   [<span data-ttu-id="5e473-115">Algoritmos de compresión</span><span class="sxs-lookup"><span data-stu-id="5e473-115">Compression Algorithms</span></span>](#compression-algorithms)
    -   [<span data-ttu-id="5e473-116">BC1</span><span class="sxs-lookup"><span data-stu-id="5e473-116">BC1</span></span>](#bc1)
    -   [<span data-ttu-id="5e473-117">BC2</span><span class="sxs-lookup"><span data-stu-id="5e473-117">BC2</span></span>](#bc2)
    -   [<span data-ttu-id="5e473-118">BC3</span><span class="sxs-lookup"><span data-stu-id="5e473-118">BC3</span></span>](#bc3)
    -   [<span data-ttu-id="5e473-119">LAS texturas BC4</span><span class="sxs-lookup"><span data-stu-id="5e473-119">BC4</span></span>](#bc4)
    -   [<span data-ttu-id="5e473-120">BC5</span><span class="sxs-lookup"><span data-stu-id="5e473-120">BC5</span></span>](#bc5)
-   [<span data-ttu-id="5e473-121">Conversión de formato mediante Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="5e473-121">Format Conversion Using Direct3D 10.1</span></span>](#format-conversion-using-direct3d-101)
-   [<span data-ttu-id="5e473-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e473-122">Related topics</span></span>](#related-topics)

## <a name="how-does-block-compression-work"></a><span data-ttu-id="5e473-123">¿Cómo funciona la compresión de bloque?</span><span class="sxs-lookup"><span data-stu-id="5e473-123">How Does Block Compression Work?</span></span>

<span data-ttu-id="5e473-124">La compresión de bloque es una técnica para reducir la cantidad de memoria necesaria para almacenar los datos de color.</span><span class="sxs-lookup"><span data-stu-id="5e473-124">Block compression is a technique for reducing the amount of memory required to store color data.</span></span> <span data-ttu-id="5e473-125">Al almacenar algunos colores en su tamaño original y otros colores con un esquema de codificación, puede reducir drásticamente la cantidad de memoria necesaria para almacenar la imagen.</span><span class="sxs-lookup"><span data-stu-id="5e473-125">By storing some colors in their original size, and other colors using an encoding scheme, you can dramatically reduce the amount of memory required to store the image.</span></span> <span data-ttu-id="5e473-126">Dado que el hardware descodifica automáticamente los datos comprimidos, no hay ninguna penalización de rendimiento para el uso de texturas comprimidas.</span><span class="sxs-lookup"><span data-stu-id="5e473-126">Since the hardware automatically decodes compressed data, there is no performance penalty for using compressed textures.</span></span>

<span data-ttu-id="5e473-127">Para ver cómo funciona la compresión, consulte los dos ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="5e473-127">To see how compression works, look at the following two examples.</span></span> <span data-ttu-id="5e473-128">En el primer ejemplo se describe la cantidad de memoria que se utiliza al almacenar datos sin comprimir. en el segundo ejemplo se describe la cantidad de memoria que se utiliza al almacenar datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="5e473-128">The first example describes the amount of memory used when storing uncompressed data; the second example describes the amount of memory used when storing compressed data.</span></span>

### <a name="storing-uncompressed-data"></a><span data-ttu-id="5e473-129">Almacenar datos sin comprimir</span><span class="sxs-lookup"><span data-stu-id="5e473-129">Storing Uncompressed Data</span></span>

<span data-ttu-id="5e473-130">En la ilustración siguiente se representa una textura de 4 × 4 sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="5e473-130">The following illustration represents an uncompressed 4×4 texture.</span></span> <span data-ttu-id="5e473-131">Supongamos que cada color contiene un componente de color único (rojo por ejemplo) y se almacena en un byte de memoria.</span><span class="sxs-lookup"><span data-stu-id="5e473-131">Assume that each color contains a single color component (red for instance) and is stored in one byte of memory.</span></span>

![Ilustración de una textura 4x4 sin comprimir](images/d3d10-block-compress-1.png)

<span data-ttu-id="5e473-133">Los datos sin comprimir se colocan en la memoria secuencialmente y requieren 16 bytes, tal como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="5e473-133">The uncompressed data is laid out in memory sequentially and requires 16 bytes, as shown in the following illustration.</span></span>

![Ilustración de datos sin comprimir en memoria secuencial](images/d3d10-block-compress-2.png)

### <a name="storing-compressed-data"></a><span data-ttu-id="5e473-135">Almacenar datos comprimidos</span><span class="sxs-lookup"><span data-stu-id="5e473-135">Storing Compressed Data</span></span>

<span data-ttu-id="5e473-136">Ahora que ha visto cuánta memoria utiliza una imagen sin comprimir, eche un vistazo a cuánta memoria guarda una imagen comprimida.</span><span class="sxs-lookup"><span data-stu-id="5e473-136">Now that you've seen how much memory an uncompressed image uses, take a look at how much memory a compressed image saves.</span></span> <span data-ttu-id="5e473-137">El formato de compresión [BC1](#bc1) almacena 2 colores (1 byte cada uno) y índices de 16 3 bits (48 bits o 6 bytes) que se usan para interpolar los colores originales en la textura, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="5e473-137">The [BC1](#bc1) compression format stores 2 colors (1 byte each) and 16 3-bit indices (48 bits, or 6 bytes) that are used to interpolate the original colors in the texture, as shown in the following illustration.</span></span>

![Ilustración del formato de compresión BC1](images/d3d10-block-compress-3.png)

<span data-ttu-id="5e473-139">El espacio total necesario para almacenar los datos comprimidos es de 8 bytes, lo que supone un ahorro de memoria del 50% sobre el ejemplo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="5e473-139">The total space required to store the compressed data is 8 bytes which is a 50-percent memory savings over the uncompressed example.</span></span> <span data-ttu-id="5e473-140">El ahorro es incluso mayor cuando se usa más de un componente de color.</span><span class="sxs-lookup"><span data-stu-id="5e473-140">The savings are even larger when more than one color component is used.</span></span>

<span data-ttu-id="5e473-141">El importante ahorro de memoria que proporciona la compresión por bloques puede dar lugar a un aumento del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5e473-141">The substantial memory savings provided by block compression can lead to an increase in performance.</span></span> <span data-ttu-id="5e473-142">Este rendimiento se produce a costa de la calidad de la imagen (debido a la interpolación de color). sin embargo, la calidad inferior no suele ser apreciable.</span><span class="sxs-lookup"><span data-stu-id="5e473-142">This performance comes at the cost of image quality (due to color interpolation); however, the lower quality is often not noticeable.</span></span>

<span data-ttu-id="5e473-143">En la sección siguiente se muestra cómo Direct3D 10 facilita el uso de la compresión de bloque en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e473-143">The next section shows you how Direct3D 10 makes it easy for you to use block compression in your application.</span></span>

## <a name="using-block-compression"></a><span data-ttu-id="5e473-144">Usar la compresión de bloque</span><span class="sxs-lookup"><span data-stu-id="5e473-144">Using Block Compression</span></span>

<span data-ttu-id="5e473-145">Cree una textura comprimida en bloque como una textura sin comprimir (consulte [creación de una textura a partir de un archivo](d3d10-graphics-programming-guide-resources-creating-textures.md)), excepto que se especifica un formato comprimido en bloques.</span><span class="sxs-lookup"><span data-stu-id="5e473-145">Create a block-compressed texture just like an uncompressed texture (see [Create a Texture from a File](d3d10-graphics-programming-guide-resources-creating-textures.md)) except that you specify a block-compressed format.</span></span>


```
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;
D3DX10CreateTextureFromFile(...);
```



<span data-ttu-id="5e473-146">A continuación, cree una vista para enlazar la textura a la canalización.</span><span class="sxs-lookup"><span data-stu-id="5e473-146">Next, create a view to bind the texture to the pipeline.</span></span> <span data-ttu-id="5e473-147">Dado que una textura con compresión de bloque solo se puede usar como entrada para una fase de sombreador, desea crear una vista de recursos de sombreador mediante una llamada a [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="5e473-147">Since a block-compressed texture can be used only as an input to a shader-stage, you want to create a shader-resource view by calling [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>

<span data-ttu-id="5e473-148">Use una textura comprimida de bloque del mismo modo que usaría una textura sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="5e473-148">Use a block compressed texture the same way you would use an uncompressed texture.</span></span> <span data-ttu-id="5e473-149">Si la aplicación va a obtener un puntero de memoria para bloquear datos comprimidos, debe tener en cuenta el relleno de memoria en un mipmap que hace que el tamaño declarado difiera del tamaño real.</span><span class="sxs-lookup"><span data-stu-id="5e473-149">If your application will get a memory pointer to block-compressed data, you need to account for the memory padding in a mipmap that causes the declared size to differ from the actual size.</span></span>

### <a name="virtual-size-versus-physical-size"></a><span data-ttu-id="5e473-150">Tamaño virtual frente al tamaño físico</span><span class="sxs-lookup"><span data-stu-id="5e473-150">Virtual Size versus Physical Size</span></span>

<span data-ttu-id="5e473-151">Si tiene código de aplicación que usa un puntero de memoria para recorrer la memoria de una textura comprimida de bloque, hay una consideración importante que puede requerir una modificación en el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e473-151">If you have application code that uses a memory pointer to walk the memory of a block compressed texture, there is one important consideration that may require a modification in your application code.</span></span> <span data-ttu-id="5e473-152">Una textura comprimida por bloques debe ser un múltiplo de 4 en todas las dimensiones, ya que los algoritmos de compresión de bloque operan en bloques textura de 4x4.</span><span class="sxs-lookup"><span data-stu-id="5e473-152">A block-compressed texture must be a multiple of 4 in all dimensions because the block-compression algorithms operate on 4x4 texel blocks.</span></span> <span data-ttu-id="5e473-153">Esto supondrá un problema para un mipmap cuyas dimensiones iniciales son divisibles en 4, pero los niveles subdivididos no lo son.</span><span class="sxs-lookup"><span data-stu-id="5e473-153">This will be a problem for a mipmap whose initial dimensions are divisible by 4, but subdivided levels are not.</span></span> <span data-ttu-id="5e473-154">En el diagrama siguiente se muestra la diferencia en el área entre el tamaño virtual (declarado) y el tamaño físico (real) de cada nivel de mipmap.</span><span class="sxs-lookup"><span data-stu-id="5e473-154">The following diagram shows the difference in area between the virtual (declared) size and the physical (actual) size of each mipmap level.</span></span>

![diagrama de niveles de mipmap sin comprimir y comprimidos](images/d3d10-block-compress-pad.png)

<span data-ttu-id="5e473-156">En el lado izquierdo del diagrama se muestran los tamaños de nivel de mipmap que se generan para una textura de 60 × 40 sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="5e473-156">The left side of the diagram shows the mipmap level sizes that are generated for an uncompressed 60×40 texture.</span></span> <span data-ttu-id="5e473-157">El tamaño de nivel superior se toma de la llamada API que genera la textura; cada nivel subsiguiente es la mitad del tamaño del nivel anterior.</span><span class="sxs-lookup"><span data-stu-id="5e473-157">The top level size is taken from the API call that generates the texture; each subsequent level is half the size of the previous level.</span></span> <span data-ttu-id="5e473-158">En el caso de una textura sin comprimir, no hay ninguna diferencia entre el tamaño virtual (declarado) y el tamaño físico (real).</span><span class="sxs-lookup"><span data-stu-id="5e473-158">For an uncompressed texture, there is no difference between the virtual (declared) size and the physical (actual) size.</span></span>

<span data-ttu-id="5e473-159">En el lado derecho del diagrama se muestran los tamaños de nivel de mipmap que se generan para la misma textura de 60 × 40 con compresión.</span><span class="sxs-lookup"><span data-stu-id="5e473-159">The right side of the diagram shows the mipmap level sizes that are generated for the same 60×40 texture with compression.</span></span> <span data-ttu-id="5e473-160">Tenga en cuenta que tanto el segundo como el tercer nivel tienen un relleno de memoria para que los factores de tamaño de 4 se conviertan en todos los niveles.</span><span class="sxs-lookup"><span data-stu-id="5e473-160">Notice that both the second and third levels have memory padding to make the sizes factors of 4 on every level.</span></span> <span data-ttu-id="5e473-161">Esto es necesario para que los algoritmos puedan funcionar en 4 × 4 bloques textura.</span><span class="sxs-lookup"><span data-stu-id="5e473-161">This is necessary so that the algorithms can operate on 4×4 texel blocks.</span></span> <span data-ttu-id="5e473-162">Este especiales es evidente si tiene en cuenta los niveles de mipmap inferiores a 4 × 4; el tamaño de estos niveles de mipmap pequeños se redondeará al factor más cercano de 4 cuando se asigne memoria de textura.</span><span class="sxs-lookup"><span data-stu-id="5e473-162">This is expecially evident if you consider mipmap levels that are smaller than 4×4; the size of these very small mipmap levels will be rounded up to the nearest factor of 4 when texture memory is allocated.</span></span>

<span data-ttu-id="5e473-163">El hardware de muestreo utiliza el tamaño virtual; Cuando se muestrea la textura, se omite el relleno de memoria.</span><span class="sxs-lookup"><span data-stu-id="5e473-163">Sampling hardware uses the virtual size; when the texture is sampled, the memory padding is ignored.</span></span> <span data-ttu-id="5e473-164">En el caso de los niveles de mipmap inferiores a 4 × 4, solo se usarán los cuatro primeros textura para un mapa 2 × 2 y solo el primer textura se usará en un bloque 1 × 1.</span><span class="sxs-lookup"><span data-stu-id="5e473-164">For mipmap levels that are smaller than 4×4, only the first four texels will be used for a 2×2 map, and only the first texel will be used by a 1×1 block.</span></span> <span data-ttu-id="5e473-165">Sin embargo, no hay ninguna estructura de API que exponga el tamaño físico (incluido el relleno de memoria).</span><span class="sxs-lookup"><span data-stu-id="5e473-165">However, there is no API structure that exposes the physical size (including the memory padding).</span></span>

<span data-ttu-id="5e473-166">En Resumen, tenga cuidado de utilizar bloques de memoria alineados al copiar regiones que contienen datos comprimidos en bloques.</span><span class="sxs-lookup"><span data-stu-id="5e473-166">In summary, be careful to use aligned memory blocks when copying regions that contain block-compressed data.</span></span> <span data-ttu-id="5e473-167">Para hacer esto en una aplicación que obtiene un puntero de memoria, asegúrese de que el puntero usa el paso de la superficie para tener en cuenta el tamaño de la memoria física.</span><span class="sxs-lookup"><span data-stu-id="5e473-167">To do this in an application that gets a memory pointer, make sure that the pointer uses the surface pitch to account for the physical memory size.</span></span>

## <a name="compression-algorithms"></a><span data-ttu-id="5e473-168">Algoritmos de compresión</span><span class="sxs-lookup"><span data-stu-id="5e473-168">Compression Algorithms</span></span>

<span data-ttu-id="5e473-169">Las técnicas de compresión en bloque de Direct3D dividen los datos de textura sin comprimir en 4 × 4 bloques, comprimen cada bloque y, a continuación, almacenan los datos.</span><span class="sxs-lookup"><span data-stu-id="5e473-169">Block compression techniques in Direct3D break up uncompressed texture data into 4×4 blocks, compress each block, and then store the data.</span></span> <span data-ttu-id="5e473-170">Por esta razón, se espera que las texturas se compriman deben tener dimensiones de textura que sean múltiplos de 4.</span><span class="sxs-lookup"><span data-stu-id="5e473-170">For this reason, textures are expected to be compressed must have texture dimensions that are multiples of 4.</span></span>

![diagrama de la compresión de bloque](images/d3d10-compression-1.png)

<span data-ttu-id="5e473-172">En el diagrama anterior se muestra una textura particionada en bloques textura.</span><span class="sxs-lookup"><span data-stu-id="5e473-172">The preceding diagram shows a texture partitioned into texel blocks.</span></span> <span data-ttu-id="5e473-173">El primer bloque muestra el diseño de los 16 textura etiquetados como-p, pero cada bloque tiene la misma organización de datos.</span><span class="sxs-lookup"><span data-stu-id="5e473-173">The first block shows the layout of the 16 texels labeled a-p, but every block has the same organization of data.</span></span>

<span data-ttu-id="5e473-174">Direct3D implementa varios esquemas de compresión, cada uno de ellos implementa un equilibrio diferente entre el número de componentes almacenados, el número de bits por componente y la cantidad de memoria consumida.</span><span class="sxs-lookup"><span data-stu-id="5e473-174">Direct3D implements several compression schemes, each implements a different tradeoff between number of components stored, the number of bits per component, and the amount of memory consumed.</span></span> <span data-ttu-id="5e473-175">Use esta tabla para ayudar a elegir el formato que mejor se adapte al tipo de datos y la resolución de los datos que mejor se adapta a su aplicación.</span><span class="sxs-lookup"><span data-stu-id="5e473-175">Use this table to help choose the format that works best with the type of data and the data resolution that best fits your application.</span></span>



| <span data-ttu-id="5e473-176">Datos de origen</span><span class="sxs-lookup"><span data-stu-id="5e473-176">Source Data</span></span>                     | <span data-ttu-id="5e473-177">Resolución de compresión de datos (en bits)</span><span class="sxs-lookup"><span data-stu-id="5e473-177">Data Compression Resolution (in bits)</span></span> | <span data-ttu-id="5e473-178">Elegir este formato de compresión</span><span class="sxs-lookup"><span data-stu-id="5e473-178">Choose this compression format</span></span> |
|---------------------------------|---------------------------------------|--------------------------------|
| <span data-ttu-id="5e473-179">Color de tres componentes y alfa</span><span class="sxs-lookup"><span data-stu-id="5e473-179">Three-component color and alpha</span></span> | <span data-ttu-id="5e473-180">Color (5:6:5), alfa (1) o no alfa</span><span class="sxs-lookup"><span data-stu-id="5e473-180">Color (5:6:5), Alpha (1) or no alpha</span></span>  | <span data-ttu-id="5e473-181">BC1</span><span class="sxs-lookup"><span data-stu-id="5e473-181">BC1</span></span>                            |
| <span data-ttu-id="5e473-182">Color de tres componentes y alfa</span><span class="sxs-lookup"><span data-stu-id="5e473-182">Three-component color and alpha</span></span> | <span data-ttu-id="5e473-183">Color (5:6:5), alfa (4)</span><span class="sxs-lookup"><span data-stu-id="5e473-183">Color (5:6:5), Alpha (4)</span></span>              | [<span data-ttu-id="5e473-184">BC2</span><span class="sxs-lookup"><span data-stu-id="5e473-184">BC2</span></span>](#bc2)                    |
| <span data-ttu-id="5e473-185">Color de tres componentes y alfa</span><span class="sxs-lookup"><span data-stu-id="5e473-185">Three-component color and alpha</span></span> | <span data-ttu-id="5e473-186">Color (5:6:5), alfa (8)</span><span class="sxs-lookup"><span data-stu-id="5e473-186">Color (5:6:5), Alpha (8)</span></span>              | [<span data-ttu-id="5e473-187">BC3</span><span class="sxs-lookup"><span data-stu-id="5e473-187">BC3</span></span>](#bc3)                    |
| <span data-ttu-id="5e473-188">Color de un componente</span><span class="sxs-lookup"><span data-stu-id="5e473-188">One-component color</span></span>             | <span data-ttu-id="5e473-189">Un componente (8)</span><span class="sxs-lookup"><span data-stu-id="5e473-189">One component (8)</span></span>                     | [<span data-ttu-id="5e473-190">LAS texturas BC4</span><span class="sxs-lookup"><span data-stu-id="5e473-190">BC4</span></span>](#bc4)                    |
| <span data-ttu-id="5e473-191">Color de dos componentes</span><span class="sxs-lookup"><span data-stu-id="5e473-191">Two-component color</span></span>             | <span data-ttu-id="5e473-192">Dos componentes (8:8)</span><span class="sxs-lookup"><span data-stu-id="5e473-192">Two components (8:8)</span></span>                  | [<span data-ttu-id="5e473-193">BC5</span><span class="sxs-lookup"><span data-stu-id="5e473-193">BC5</span></span>](#bc5)                    |



 

### <a name="bc1"></a><span data-ttu-id="5e473-194">BC1</span><span class="sxs-lookup"><span data-stu-id="5e473-194">BC1</span></span>

<span data-ttu-id="5e473-195">Use el primer formato de compresión de bloque (BC1) (el formato de DXGI \_ \_ BC1 \_ sin tipo, \_ el formato de DXGI \_ BC1 \_ UNORM o dxgi \_ BC1 \_ UNORM \_ sRGB) para almacenar datos de color de tres componentes mediante un color de 5:6:5 (5 bits rojo, 6 bits verde, 5 bits azul).</span><span class="sxs-lookup"><span data-stu-id="5e473-195">Use the first block compression format (BC1) (either DXGI\_FORMAT\_BC1\_TYPELESS, DXGI\_FORMAT\_BC1\_UNORM, or DXGI\_BC1\_UNORM\_SRGB) to store three-component color data using a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue).</span></span> <span data-ttu-id="5e473-196">Esto es así incluso si los datos también contienen alfa de 1 bit.</span><span class="sxs-lookup"><span data-stu-id="5e473-196">This is true even if the data also contains 1-bit alpha.</span></span> <span data-ttu-id="5e473-197">Suponiendo una textura de 4 × 4 con el formato de datos más grande posible, el formato BC1 reduce la cantidad de memoria necesaria de 48 bytes (16 colores × 3 componentes/color × 1 byte/componente) a 8 bytes de memoria.</span><span class="sxs-lookup"><span data-stu-id="5e473-197">Assuming a 4×4 texture using the largest data format possible, the BC1 format reduces the memory required from 48 bytes (16 colors × 3 components/color × 1 byte/component) to 8 bytes of memory.</span></span>

<span data-ttu-id="5e473-198">El algoritmo funciona en 4 × 4 bloques de textura.</span><span class="sxs-lookup"><span data-stu-id="5e473-198">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="5e473-199">En lugar de almacenar 16 colores, el algoritmo guarda 2 colores de referencia (color \_ 0 y color \_ 1) y índices de color de 16 2 bits (bloques a – p), tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e473-199">Instead of storing 16 colors, the algorithm saves 2 reference colors (color\_0 and color\_1) and 16 2-bit color indices (blocks a–p), as shown in the following diagram.</span></span>

![diagrama del diseño de la compresión BC1](images/d3d10-compression-bc1.png)

<span data-ttu-id="5e473-201">Los índices de color (a – p) se usan para buscar los colores originales de una tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="5e473-201">The color indices (a–p) are used to look up the original colors from a color table.</span></span> <span data-ttu-id="5e473-202">La tabla de colores contiene 4 colores.</span><span class="sxs-lookup"><span data-stu-id="5e473-202">The color table contains 4 colors.</span></span> <span data-ttu-id="5e473-203">Los dos primeros colores (color \_ 0 y color \_ 1) son los colores mínimo y máximo.</span><span class="sxs-lookup"><span data-stu-id="5e473-203">The first two colors—color\_0 and color\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="5e473-204">Los otros dos colores, color \_ 2 y color \_ 3, son colores intermedios calculados con interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="5e473-204">The other two colors, color\_2 and color\_3, are intermediate colors calculated with linear interpolation.</span></span>


```
color_2 = 2/3*color_0 + 1/3*color_1
color_3 = 1/3*color_0 + 2/3*color_1
```



<span data-ttu-id="5e473-205">A los cuatro colores se les asignan valores de índice de 2 bits que se guardarán en bloques a – p.</span><span class="sxs-lookup"><span data-stu-id="5e473-205">The four colors are assigned 2-bit index values that will be saved in blocks a–p.</span></span>


```
color_0 = 00
color_1 = 01
color_2 = 10
color_3 = 11
```



<span data-ttu-id="5e473-206">Por último, cada uno de los colores de los bloques a – p se comparan con los cuatro colores de la tabla de colores y el índice del color más cercano se almacena en los bloques de 2 bits.</span><span class="sxs-lookup"><span data-stu-id="5e473-206">Finally, each of the colors in blocks a–p are compared with the four colors in the color table, and the index for the closest color is stored in the 2-bit blocks.</span></span>

<span data-ttu-id="5e473-207">Este algoritmo se presta a los datos que contienen también Alpha de 1 bit.</span><span class="sxs-lookup"><span data-stu-id="5e473-207">This algorithm lends itself to data that contains 1-bit alpha also.</span></span> <span data-ttu-id="5e473-208">La única diferencia es que el color \_ 3 se establece en 0 (que representa un color transparente) y \_ el color 2 es una mezcla lineal del color \_ 0 y el color \_ 1.</span><span class="sxs-lookup"><span data-stu-id="5e473-208">The only difference is that color\_3 is set to 0 (which represents a transparent color) and color\_2 is a linear blend of color\_0 and color\_1.</span></span>


```
color_2 = 1/2*color_0 + 1/2*color_1;
color_3 = 0;
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e473-209">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="5e473-209">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="5e473-210">Este formato existe en Direct3D 9 y 10.</span><span class="sxs-lookup"><span data-stu-id="5e473-210">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="5e473-211">En Direct3D 9, el formato BC1 se denomina D3DFMT_DXT1.</span><span class="sxs-lookup"><span data-stu-id="5e473-211">In Direct3D 9, the BC1 format is called D3DFMT_DXT1.</span></span></li>
<li><span data-ttu-id="5e473-212">En Direct3D 10, el formato BC1 se representa mediante DXGI_FORMAT_BC1_UNORM o DXGI_FORMAT_BC1_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="5e473-212">In Direct3D 10, the BC1 format is represented by DXGI_FORMAT_BC1_UNORM or DXGI_FORMAT_BC1_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc2"></a><span data-ttu-id="5e473-213">BC2</span><span class="sxs-lookup"><span data-stu-id="5e473-213">BC2</span></span>

<span data-ttu-id="5e473-214">Use el formato BC2 (ya sea el formato de DXGI \_ \_ BC2 \_ sin tipo, el formato de dxgi \_ \_ BC2 \_ UNORM o dxgi \_ BC2 \_ UNORM \_ sRGB) para almacenar datos que contengan datos de color y alfa con baja coherencia (use [BC3](#bc3) para datos alfa altamente coherentes).</span><span class="sxs-lookup"><span data-stu-id="5e473-214">Use the BC2 format (either DXGI\_FORMAT\_BC2\_TYPELESS, DXGI\_FORMAT\_BC2\_UNORM, or DXGI\_BC2\_UNORM\_SRGB) to store data that contains color and alpha data with low coherency (use [BC3](#bc3) for highly-coherent alpha data).</span></span> <span data-ttu-id="5e473-215">El formato BC2 almacena los datos RGB como un color 5:6:5 (5 bits rojo, 6 bits verde, 5 bits azul) y alfa como un valor de 4 bits independiente.</span><span class="sxs-lookup"><span data-stu-id="5e473-215">The BC2 format stores RGB data as a 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha as a separate 4-bit value.</span></span> <span data-ttu-id="5e473-216">Suponiendo una textura de 4 × 4 con el formato de datos más grande posible, esta técnica de compresión reduce la cantidad de memoria necesaria de 64 bytes (16 colores × 4 componentes/color × 1 byte/componente) a 16 bytes de memoria.</span><span class="sxs-lookup"><span data-stu-id="5e473-216">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="5e473-217">El formato BC2 almacena los colores con el mismo número de bits y diseño de datos que el formato [BC1](#bc1) . sin embargo, BC2 requiere una memoria adicional de 64 bits para almacenar los datos alfa, tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e473-217">The BC2 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC2 requires an additional 64-bits of memory to store the alpha data, as shown in the following diagram.</span></span>

![diagrama del diseño de la compresión BC2](images/d3d10-compression-bc2.png)

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e473-219">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="5e473-219">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="5e473-220">Este formato existe en Direct3D 9 y 10.</span><span class="sxs-lookup"><span data-stu-id="5e473-220">This format exists in both Direct3D 9 and 10.</span></span><br/>
<ul>
<li><span data-ttu-id="5e473-221">En Direct3D 9, el formato BC2 se denomina D3DFMT_DXT2 y D3DFMT_DXT3.</span><span class="sxs-lookup"><span data-stu-id="5e473-221">In Direct3D 9, the BC2 format is called D3DFMT_DXT2 and D3DFMT_DXT3.</span></span></li>
<li><span data-ttu-id="5e473-222">En Direct3D 10, el formato BC2 se representa mediante DXGI_FORMAT_BC2_UNORM o DXGI_FORMAT_BC2_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="5e473-222">In Direct3D 10, the BC2 format is represented by DXGI_FORMAT_BC2_UNORM or DXGI_FORMAT_BC2_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc3"></a><span data-ttu-id="5e473-223">BC3</span><span class="sxs-lookup"><span data-stu-id="5e473-223">BC3</span></span>

<span data-ttu-id="5e473-224">Use el formato BC3 (ya sea el formato de DXGI \_ \_ BC3 \_ sin tipo, el formato de dxgi \_ \_ BC3 \_ UNORM o dxgi \_ BC3 \_ UNORM \_ sRGB) para almacenar datos de color muy coherentes (use [BC2](#bc2) con datos alfa menos coherentes).</span><span class="sxs-lookup"><span data-stu-id="5e473-224">Use the BC3 format (either DXGI\_FORMAT\_BC3\_TYPELESS, DXGI\_FORMAT\_BC3\_UNORM, or DXGI\_BC3\_UNORM\_SRGB) to store highly coherent color data (use [BC2](#bc2) with less coherent alpha data).</span></span> <span data-ttu-id="5e473-225">El formato BC3 almacena los datos de color con color 5:6:5 (5 bits rojo, 6 bits verde, 5 bits azul) y datos alfa usando un byte.</span><span class="sxs-lookup"><span data-stu-id="5e473-225">The BC3 format stores color data using 5:6:5 color (5 bits red, 6 bits green, 5 bits blue) and alpha data using one byte.</span></span> <span data-ttu-id="5e473-226">Suponiendo una textura de 4 × 4 con el formato de datos más grande posible, esta técnica de compresión reduce la cantidad de memoria necesaria de 64 bytes (16 colores × 4 componentes/color × 1 byte/componente) a 16 bytes de memoria.</span><span class="sxs-lookup"><span data-stu-id="5e473-226">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 64 bytes (16 colors × 4 components/color × 1 byte/component) to 16 bytes of memory.</span></span>

<span data-ttu-id="5e473-227">El formato BC3 almacena los colores con el mismo número de bits y diseño de datos que el formato [BC1](#bc1) . sin embargo, BC3 requiere una memoria adicional de 64 bits para almacenar los datos alfa.</span><span class="sxs-lookup"><span data-stu-id="5e473-227">The BC3 format stores colors with the same number of bits and data layout as the [BC1](#bc1) format; however, BC3 requires an additional 64-bits of memory to store the alpha data.</span></span> <span data-ttu-id="5e473-228">El formato BC3 controla el valor alfa al almacenar dos valores de referencia y interpolar entre ellos (de forma similar al modo en que BC1 almacena el color RGB).</span><span class="sxs-lookup"><span data-stu-id="5e473-228">The BC3 format handles alpha by storing two reference values and interpolating between them (similarly to how BC1 stores RGB color).</span></span>

<span data-ttu-id="5e473-229">El algoritmo funciona en 4 × 4 bloques de textura.</span><span class="sxs-lookup"><span data-stu-id="5e473-229">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="5e473-230">En lugar de almacenar 16 valores alfa, el algoritmo almacena 2 alfas de referencia (alfa \_ 0 y alfa \_ 1) y los índices de color de 16 3 bits (alfa a a p), tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e473-230">Instead of storing 16 alpha values, the algorithm stores 2 reference alphas (alpha\_0 and alpha\_1) and 16 3-bit color indices (alpha a through p), as shown in the following diagram.</span></span>

![diagrama del diseño de la compresión BC3](images/d3d10-compression-bc3.png)

<span data-ttu-id="5e473-232">El formato BC3 usa los índices alfa (a – p) para buscar los colores originales de una tabla de búsqueda que contiene 8 valores.</span><span class="sxs-lookup"><span data-stu-id="5e473-232">The BC3 format uses the alpha indices (a–p) to look up the original colors from a lookup table that contains 8 values.</span></span> <span data-ttu-id="5e473-233">Los dos primeros valores (alfa \_ 0 y alfa \_ 1) son los valores mínimo y máximo; los otros seis valores intermedios se calculan mediante la interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="5e473-233">The first two values—alpha\_0 and alpha\_1—are the minimum and maximum values; the other six intermediate values are calculated using linear interpolation.</span></span>

<span data-ttu-id="5e473-234">El algoritmo determina el número de valores alfa interpolados examinando los dos valores alfa de referencia.</span><span class="sxs-lookup"><span data-stu-id="5e473-234">The algorithm determines the number of interpolated alpha values by examining the two reference alpha values.</span></span> <span data-ttu-id="5e473-235">Si el \_ valor alfa 0 es mayor que el \_ valor alfa 1, BC3 interpola 6 valores alfa; de lo contrario, interpola 4.</span><span class="sxs-lookup"><span data-stu-id="5e473-235">If alpha\_0 is greater than alpha\_1, then BC3 interpolates 6 alpha values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="5e473-236">Cuando BC3 interpola solo 4 valores alfa, establece dos valores alfa adicionales (0 para totalmente transparente y 255 para totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="5e473-236">When BC3 interpolates only 4 alpha values, it sets two additional alpha values (0 for fully transparent and 255 for fully opaque).</span></span> <span data-ttu-id="5e473-237">BC3 comprime los valores alfa en el área textura de 4 × 4 almacenando el código de bit correspondiente a los valores alfa interpolados que más se aproxime al alfa original de un textura determinado.</span><span class="sxs-lookup"><span data-stu-id="5e473-237">BC3 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values which most closely matches the original alpha for a given texel.</span></span>


```
if( alpha_0 > alpha_1 )
{
  // 6 interpolated alpha values.
  alpha_2 = 6/7*alpha_0 + 1/7*alpha_1; // bit code 010
  alpha_3 = 5/7*alpha_0 + 2/7*alpha_1; // bit code 011
  alpha_4 = 4/7*alpha_0 + 3/7*alpha_1; // bit code 100
  alpha_5 = 3/7*alpha_0 + 4/7*alpha_1; // bit code 101
  alpha_6 = 2/7*alpha_0 + 5/7*alpha_1; // bit code 110
  alpha_7 = 1/7*alpha_0 + 6/7*alpha_1; // bit code 111
}
else
{
  // 4 interpolated alpha values.
  alpha_2 = 4/5*alpha_0 + 1/5*alpha_1; // bit code 010
  alpha_3 = 3/5*alpha_0 + 2/5*alpha_1; // bit code 011
  alpha_4 = 2/5*alpha_0 + 3/5*alpha_1; // bit code 100
  alpha_5 = 1/5*alpha_0 + 4/5*alpha_1; // bit code 101
  alpha_6 = 0;                         // bit code 110
  alpha_7 = 255;                       // bit code 111
}
```





<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e473-238">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="5e473-238">Differences between Direct3D 9 and Direct3D 10:</span></span><br/>
<ul>
<li><span data-ttu-id="5e473-239">En Direct3D 9, el formato BC3 se denomina D3DFMT_DXT4 y D3DFMT_DXT5.</span><span class="sxs-lookup"><span data-stu-id="5e473-239">In Direct3D 9, the BC3 format is called D3DFMT_DXT4 and D3DFMT_DXT5.</span></span></li>
<li><span data-ttu-id="5e473-240">En Direct3D 10, el formato BC3 se representa mediante DXGI_FORMAT_BC3_UNORM o DXGI_FORMAT_BC3_UNORM_SRGB.</span><span class="sxs-lookup"><span data-stu-id="5e473-240">In Direct3D 10, the BC3 format is represented by DXGI_FORMAT_BC3_UNORM or DXGI_FORMAT_BC3_UNORM_SRGB.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="bc4"></a><span data-ttu-id="5e473-241">LAS texturas BC4</span><span class="sxs-lookup"><span data-stu-id="5e473-241">BC4</span></span>

<span data-ttu-id="5e473-242">Use el formato las texturas BC4 para almacenar datos de color de un componente usando 8 bits para cada color.</span><span class="sxs-lookup"><span data-stu-id="5e473-242">Use the BC4 format to store one-component color data using 8 bits for each color.</span></span> <span data-ttu-id="5e473-243">Como resultado de la mayor precisión (en comparación con [BC1](#bc1)), las texturas BC4 es ideal para almacenar los datos de punto flotante en el intervalo de \[ 0 a 1 \] mediante el formato de dxgi \_ \_ las texturas BC4 \_ UNORM y \[ -1 a + 1 \] con el formato dxgi \_ \_ las texturas BC4 \_ SNORM.</span><span class="sxs-lookup"><span data-stu-id="5e473-243">As a result of the increased accuracy (compared to [BC1](#bc1)), BC4 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC4\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC4\_SNORM format.</span></span> <span data-ttu-id="5e473-244">Suponiendo una textura de 4 × 4 con el formato de datos más grande posible, esta técnica de compresión reduce la cantidad de memoria necesaria de 16 bytes (16 colores × 1 componentes/color × 1 byte/componente) a 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="5e473-244">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 16 bytes (16 colors × 1 components/color × 1 byte/component) to 8 bytes.</span></span>

<span data-ttu-id="5e473-245">El algoritmo funciona en 4 × 4 bloques de textura.</span><span class="sxs-lookup"><span data-stu-id="5e473-245">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="5e473-246">En lugar de almacenar 16 colores, el algoritmo almacena 2 colores de referencia (rojo \_ 0 y rojo \_ 1) y índices de color de 16 3 bits (rojo a a rojo p), tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e473-246">Instead of storing 16 colors, the algorithm stores 2 reference colors (red\_0 and red\_1) and 16 3-bit color indices (red a through red p), as shown in the following diagram.</span></span>

![diagrama del diseño de la compresión las texturas BC4](images/d3d10-compression-bc4.png)

<span data-ttu-id="5e473-248">El algoritmo utiliza los índices de 3 bits para buscar colores de una tabla de colores que contiene 8 colores.</span><span class="sxs-lookup"><span data-stu-id="5e473-248">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="5e473-249">Los dos primeros colores, rojo \_ 0 y rojo \_ 1, son los colores mínimo y máximo.</span><span class="sxs-lookup"><span data-stu-id="5e473-249">The first two colors—red\_0 and red\_1—are the minimum and maximum colors.</span></span> <span data-ttu-id="5e473-250">El algoritmo calcula el resto de los colores mediante la interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="5e473-250">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="5e473-251">El algoritmo determina el número de valores de color interpolados examinando los dos valores de referencia.</span><span class="sxs-lookup"><span data-stu-id="5e473-251">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="5e473-252">Si el rojo \_ 0 es mayor que rojo \_ 1, las texturas BC4 interpola los valores de 6 colores; de lo contrario, interpola 4.</span><span class="sxs-lookup"><span data-stu-id="5e473-252">If red\_0 is greater than red\_1, then BC4 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="5e473-253">Cuando las texturas BC4 interpola solo 4 valores de color, establece dos valores de color adicionales (0.0 f para totalmente transparente y 1,0 f para totalmente opaco).</span><span class="sxs-lookup"><span data-stu-id="5e473-253">When BC4 interpolates only 4 color values, it sets two additional color values (0.0f for fully transparent and 1.0f for fully opaque).</span></span> <span data-ttu-id="5e473-254">LAS texturas BC4 comprime los valores alfa en el área textura de 4 × 4 almacenando el código de bit correspondiente a los valores alfa interpolados que más se aproxime al alfa original de un textura determinado.</span><span class="sxs-lookup"><span data-stu-id="5e473-254">BC4 compresses the alpha values in the 4×4 texel area by storing the bit code corresponding to the interpolated alpha values that most closely matches the original alpha for a given texel.</span></span>

-   [<span data-ttu-id="5e473-255">LAS texturas BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-255">BC4\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="5e473-256">LAS texturas BC4 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-256">BC4\_SNORM</span></span>](/windows)

### <a name="bc4_unorm"></a><span data-ttu-id="5e473-257">LAS texturas BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-257">BC4\_UNORM</span></span>

<span data-ttu-id="5e473-258">La interpolación de los datos de un solo componente se realiza como en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e473-258">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="5e473-259">A los colores de referencia se les asignan índices de 3 bits (000 – 111, ya que hay 8 valores), que se guardarán en bloques rojo a a rojo p durante la compresión.</span><span class="sxs-lookup"><span data-stu-id="5e473-259">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc4_snorm"></a><span data-ttu-id="5e473-260">LAS texturas BC4 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-260">BC4\_SNORM</span></span>

<span data-ttu-id="5e473-261">El formato de DXGI \_ \_ las texturas BC4 \_ SNORM es exactamente el mismo, salvo que los datos se codifican en el intervalo SNORM y cuando se interpolan 4 valores de color.</span><span class="sxs-lookup"><span data-stu-id="5e473-261">The DXGI\_FORMAT\_BC4\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 color values are interpolated.</span></span> <span data-ttu-id="5e473-262">La interpolación de los datos de un solo componente se realiza como en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e473-262">The interpolation of the single-component data is done as in the following code sample.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                     // bit code 110
  red_7 =  1.0f;                     // bit code 111
}
```



<span data-ttu-id="5e473-263">A los colores de referencia se les asignan índices de 3 bits (000 – 111, ya que hay 8 valores), que se guardarán en bloques rojo a a rojo p durante la compresión.</span><span class="sxs-lookup"><span data-stu-id="5e473-263">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5"></a><span data-ttu-id="5e473-264">BC5</span><span class="sxs-lookup"><span data-stu-id="5e473-264">BC5</span></span>

<span data-ttu-id="5e473-265">Use el formato BC5 para almacenar datos de color de dos componentes mediante 8 bits para cada color.</span><span class="sxs-lookup"><span data-stu-id="5e473-265">Use the BC5 format to store two-component color data using 8 bits for each color.</span></span> <span data-ttu-id="5e473-266">Como resultado de la mayor precisión (en comparación con [BC1](#bc1)), BC5 es ideal para almacenar los datos de punto flotante en el intervalo de \[ 0 a 1 \] mediante el formato de dxgi \_ \_ BC5 \_ UNORM y \[ -1 a + 1 \] con el formato dxgi \_ \_ BC5 \_ SNORM.</span><span class="sxs-lookup"><span data-stu-id="5e473-266">As a result of the increased accuracy (compared to [BC1](#bc1)), BC5 is ideal for storing floating-point data in the range of \[0 to 1\] using the DXGI\_FORMAT\_BC5\_UNORM format and \[-1 to +1\] using the DXGI\_FORMAT\_BC5\_SNORM format.</span></span> <span data-ttu-id="5e473-267">Suponiendo una textura de 4 × 4 con el formato de datos más grande posible, esta técnica de compresión reduce la cantidad de memoria necesaria de 32 bytes (16 colores × 2 componentes/color × 1 byte/componente) a 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="5e473-267">Assuming a 4×4 texture using the largest data format possible, this compression technique reduces the memory required from 32 bytes (16 colors × 2 components/color × 1 byte/component) to 16 bytes.</span></span>

<span data-ttu-id="5e473-268">El algoritmo funciona en 4 × 4 bloques de textura.</span><span class="sxs-lookup"><span data-stu-id="5e473-268">The algorithm works on 4×4 blocks of texels.</span></span> <span data-ttu-id="5e473-269">En lugar de almacenar 16 colores para ambos componentes, el algoritmo almacena 2 colores de referencia para cada componente (rojo \_ 0, rojo \_ 1, verde \_ 0 y verde \_ 1) y los índices de color de 16 3 bits para cada componente (de rojo a a rojo p y de verde a a verde p), tal y como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e473-269">Instead of storing 16 colors for both components, the algorithm stores 2 reference colors for each component (red\_0, red\_1, green\_0, and green\_1) and 16 3-bit color indices for each component (red a through red p and green a through green p), as shown in the following diagram.</span></span>

![diagrama del diseño de la compresión BC5](images/d3d10-compression-bc5.png)

<span data-ttu-id="5e473-271">El algoritmo utiliza los índices de 3 bits para buscar colores de una tabla de colores que contiene 8 colores.</span><span class="sxs-lookup"><span data-stu-id="5e473-271">The algorithm uses the 3-bit indices to look up colors from a color table that contains 8 colors.</span></span> <span data-ttu-id="5e473-272">Los dos primeros colores, rojo \_ 0 y rojo \_ 1 (o verde \_ 0 y verde \_ 1), son los colores mínimo y máximo.</span><span class="sxs-lookup"><span data-stu-id="5e473-272">The first two colors—red\_0 and red\_1 (or green\_0 and green\_1)—are the minimum and maximum colors.</span></span> <span data-ttu-id="5e473-273">El algoritmo calcula el resto de los colores mediante la interpolación lineal.</span><span class="sxs-lookup"><span data-stu-id="5e473-273">The algorithm calculates the remaining colors using linear interpolation.</span></span>

<span data-ttu-id="5e473-274">El algoritmo determina el número de valores de color interpolados examinando los dos valores de referencia.</span><span class="sxs-lookup"><span data-stu-id="5e473-274">The algorithm determines the number of interpolated color values by examining the two reference values.</span></span> <span data-ttu-id="5e473-275">Si el rojo \_ 0 es mayor que rojo \_ 1, BC5 interpola los valores de 6 colores; de lo contrario, interpola 4.</span><span class="sxs-lookup"><span data-stu-id="5e473-275">If red\_0 is greater than red\_1, then BC5 interpolates 6 color values; otherwise, it interpolates 4.</span></span> <span data-ttu-id="5e473-276">Cuando BC5 interpola solo 4 valores de color, establece los dos valores de color restantes en 0,0 f y 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="5e473-276">When BC5 interpolates only 4 color values, it sets the remaining two color values at 0.0f and 1.0f.</span></span>

-   [<span data-ttu-id="5e473-277">BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-277">BC5\_UNORM</span></span>](/windows)
-   [<span data-ttu-id="5e473-278">BC5 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-278">BC5\_SNORM</span></span>](/windows)

### <a name="bc5_unorm"></a><span data-ttu-id="5e473-279">BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-279">BC5\_UNORM</span></span>

<span data-ttu-id="5e473-280">La interpolación de los datos de un solo componente se realiza como en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e473-280">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="5e473-281">Los cálculos de los componentes verdes son similares.</span><span class="sxs-lookup"><span data-stu-id="5e473-281">The calculations for the green components are similar.</span></span>


```
unsigned word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = 0.0f;                     // bit code 110
  red_7 = 1.0f;                     // bit code 111
}
```



<span data-ttu-id="5e473-282">A los colores de referencia se les asignan índices de 3 bits (000 – 111, ya que hay 8 valores), que se guardarán en bloques rojo a a rojo p durante la compresión.</span><span class="sxs-lookup"><span data-stu-id="5e473-282">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

### <a name="bc5_snorm"></a><span data-ttu-id="5e473-283">BC5 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-283">BC5\_SNORM</span></span>

<span data-ttu-id="5e473-284">El formato de DXGI \_ \_ BC5 \_ SNORM es exactamente el mismo, salvo que los datos se codifican en el intervalo SNORM y cuando se interpolan 4 valores de datos, los dos valores adicionales son: 1,0 f y 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="5e473-284">The DXGI\_FORMAT\_BC5\_SNORM is exactly the same, except that the data is encoded in SNORM range and when 4 data values are interpolated, the two additional values are -1.0f and 1.0f.</span></span> <span data-ttu-id="5e473-285">La interpolación de los datos de un solo componente se realiza como en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e473-285">The interpolation of the single-component data is done as in the following code sample.</span></span> <span data-ttu-id="5e473-286">Los cálculos de los componentes verdes son similares.</span><span class="sxs-lookup"><span data-stu-id="5e473-286">The calculations for the green components are similar.</span></span>


```
signed word red_0, red_1;

if( red_0 > red_1 )
{
  // 6 interpolated color values
  red_2 = (6*red_0 + 1*red_1)/7.0f; // bit code 010
  red_3 = (5*red_0 + 2*red_1)/7.0f; // bit code 011
  red_4 = (4*red_0 + 3*red_1)/7.0f; // bit code 100
  red_5 = (3*red_0 + 4*red_1)/7.0f; // bit code 101
  red_6 = (2*red_0 + 5*red_1)/7.0f; // bit code 110
  red_7 = (1*red_0 + 6*red_1)/7.0f; // bit code 111
}
else
{
  // 4 interpolated color values
  red_2 = (4*red_0 + 1*red_1)/5.0f; // bit code 010
  red_3 = (3*red_0 + 2*red_1)/5.0f; // bit code 011
  red_4 = (2*red_0 + 3*red_1)/5.0f; // bit code 100
  red_5 = (1*red_0 + 4*red_1)/5.0f; // bit code 101
  red_6 = -1.0f;                    // bit code 110
  red_7 =  1.0f;                    // bit code 111
}
```



<span data-ttu-id="5e473-287">A los colores de referencia se les asignan índices de 3 bits (000 – 111, ya que hay 8 valores), que se guardarán en bloques rojo a a rojo p durante la compresión.</span><span class="sxs-lookup"><span data-stu-id="5e473-287">The reference colors are assigned 3-bit indices (000–111 since there are 8 values), which will be saved in blocks red a through red p during compression.</span></span>

## <a name="format-conversion-using-direct3d-101"></a><span data-ttu-id="5e473-288">Conversión de formato mediante Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="5e473-288">Format Conversion Using Direct3D 10.1</span></span>

<span data-ttu-id="5e473-289">Direct3D 10,1 habilita las copias entre texturas con tipo preestructurado y texturas comprimidas por bloques de los mismos anchos de bits.</span><span class="sxs-lookup"><span data-stu-id="5e473-289">Direct3D 10.1 enables copies between prestructured-typed textures and block-compressed textures of the same bit widths.</span></span> <span data-ttu-id="5e473-290">Las funciones que pueden lograr esto son [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) y [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span><span class="sxs-lookup"><span data-stu-id="5e473-290">The functions that can accomplish this are [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion).</span></span>

<span data-ttu-id="5e473-291">A partir de Direct3D 10,1, puede usar [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) y [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) para copiar entre algunos tipos de formato.</span><span class="sxs-lookup"><span data-stu-id="5e473-291">Beginning with Direct3D 10.1, you can use [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) and [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) to copy between a few format types.</span></span> <span data-ttu-id="5e473-292">Este tipo de operación de copia realiza un tipo de conversión de formato que reinterpreta los datos de recursos como un tipo de formato diferente.</span><span class="sxs-lookup"><span data-stu-id="5e473-292">This type of copy operation performs a type of format conversion that reinterprets resource data as a different format type.</span></span> <span data-ttu-id="5e473-293">Considere este ejemplo que muestra la diferencia entre reinterpretar los datos con la manera en que se comporta un tipo más típico de conversión:</span><span class="sxs-lookup"><span data-stu-id="5e473-293">Consider this example that shows the difference between reinterpreting data with the way a more typical type of conversion behaves:</span></span>


```
    FLOAT32 f = 1.0f;
    UINT32 u;
```



<span data-ttu-id="5e473-294">Para reinterpretar ' f ' como el tipo de ' u ', use [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span><span class="sxs-lookup"><span data-stu-id="5e473-294">To reinterpret ‘f’ as the type of ‘u’, use [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy):</span></span>


```
    memcpy( &u, &f, sizeof( f ) ); // ‘u’ becomes equal to 0x3F800000.
```



<span data-ttu-id="5e473-295">En la reinterpretación anterior, el valor subyacente de los datos no cambia; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterpreta el Float como un entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="5e473-295">In the preceding reinterpretation, the underlying value of the data doesn’t change; [memcpy](/cpp/c-runtime-library/reference/memcpy-wmemcpy) reinterprets the float as an unsigned integer.</span></span>

<span data-ttu-id="5e473-296">Para realizar el tipo más típico de conversión, use la asignación:</span><span class="sxs-lookup"><span data-stu-id="5e473-296">To perform the more typical type of conversion, use assignment:</span></span>


```
    u = f; // ‘u’ becomes 1.
```



<span data-ttu-id="5e473-297">En la conversión anterior, cambia el valor subyacente de los datos.</span><span class="sxs-lookup"><span data-stu-id="5e473-297">In the preceding conversion, the underlying value of the data changes.</span></span>

<span data-ttu-id="5e473-298">En la tabla siguiente se enumeran los formatos de origen y destino permitidos que se pueden usar en este tipo de reinterpretación de conversión de formato.</span><span class="sxs-lookup"><span data-stu-id="5e473-298">The following table lists the allowable source and destination formats that you can use in this reinterpretation type of format conversion.</span></span> <span data-ttu-id="5e473-299">Debe codificar los valores correctamente para que la reinterpretación funcione según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="5e473-299">You must encode the values properly for the reinterpretation to work as expected.</span></span>



| <span data-ttu-id="5e473-300">Ancho de bits</span><span class="sxs-lookup"><span data-stu-id="5e473-300">Bit Width</span></span> | <span data-ttu-id="5e473-301">Recurso sin comprimir</span><span class="sxs-lookup"><span data-stu-id="5e473-301">Uncompressed Resource</span></span>                                                                                                                                               | <span data-ttu-id="5e473-302">Block-Compressed recurso</span><span class="sxs-lookup"><span data-stu-id="5e473-302">Block-Compressed Resource</span></span>                                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e473-303">32</span><span class="sxs-lookup"><span data-stu-id="5e473-303">32</span></span>        | <span data-ttu-id="5e473-304">Formato de DXGI \_ \_ R32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="5e473-304">DXGI\_FORMAT\_R32\_UINT</span></span><br/> <span data-ttu-id="5e473-305">Formato de DXGI \_ \_ R32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="5e473-305">DXGI\_FORMAT\_R32\_SINT</span></span><br/>                                                                                               | <span data-ttu-id="5e473-306">Formato de DXGI \_ \_ R9G9B9E5 \_ SHAREDEXP</span><span class="sxs-lookup"><span data-stu-id="5e473-306">DXGI\_FORMAT\_R9G9B9E5\_SHAREDEXP</span></span>                                                                                                                                   |
| <span data-ttu-id="5e473-307">64</span><span class="sxs-lookup"><span data-stu-id="5e473-307">64</span></span>        | <span data-ttu-id="5e473-308">Formato de DXGI \_ \_ R16G16B16A16 \_ uint</span><span class="sxs-lookup"><span data-stu-id="5e473-308">DXGI\_FORMAT\_R16G16B16A16\_UINT</span></span><br/> <span data-ttu-id="5e473-309">Formato de DXGI \_ \_ R16G16B16A16 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="5e473-309">DXGI\_FORMAT\_R16G16B16A16\_SINT</span></span><br/> <span data-ttu-id="5e473-310">Formato de DXGI \_ \_ R32G32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="5e473-310">DXGI\_FORMAT\_R32G32\_UINT</span></span><br/> <span data-ttu-id="5e473-311">Formato de DXGI \_ \_ R32G32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="5e473-311">DXGI\_FORMAT\_R32G32\_SINT</span></span><br/> | <span data-ttu-id="5e473-312">Formato de DXGI \_ \_ BC1 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="5e473-312">DXGI\_FORMAT\_BC1\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="5e473-313">Formato de DXGI \_ \_ las texturas BC4 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-313">DXGI\_FORMAT\_BC4\_UNORM</span></span><br/> <span data-ttu-id="5e473-314">Formato de DXGI \_ \_ las texturas BC4 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-314">DXGI\_FORMAT\_BC4\_SNORM</span></span><br/>                                               |
| <span data-ttu-id="5e473-315">128</span><span class="sxs-lookup"><span data-stu-id="5e473-315">128</span></span>       | <span data-ttu-id="5e473-316">Formato de DXGI \_ \_ R32G32B32A32 \_ uint</span><span class="sxs-lookup"><span data-stu-id="5e473-316">DXGI\_FORMAT\_R32G32B32A32\_UINT</span></span><br/> <span data-ttu-id="5e473-317">Formato de DXGI \_ \_ R32G32B32A32 \_ Sint</span><span class="sxs-lookup"><span data-stu-id="5e473-317">DXGI\_FORMAT\_R32G32B32A32\_SINT</span></span><br/>                                                                             | <span data-ttu-id="5e473-318">Formato de DXGI \_ \_ BC2 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="5e473-318">DXGI\_FORMAT\_BC2\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="5e473-319">Formato de DXGI \_ \_ BC3 \_ UNORM \[ \_ sRGB\]</span><span class="sxs-lookup"><span data-stu-id="5e473-319">DXGI\_FORMAT\_BC3\_UNORM\[\_SRGB\]</span></span><br/> <span data-ttu-id="5e473-320">Formato de DXGI \_ \_ BC5 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-320">DXGI\_FORMAT\_BC5\_UNORM</span></span><br/> <span data-ttu-id="5e473-321">Formato de DXGI \_ \_ BC5 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="5e473-321">DXGI\_FORMAT\_BC5\_SNORM</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5e473-322">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e473-322">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e473-323">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="5e473-323">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
