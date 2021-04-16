---
description: Decoder-Specific entradas del registro
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Decoder-Specific entradas del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720751"
---
# <a name="decoder-specific-registry-entries"></a><span data-ttu-id="925e9-103">Decoder-Specific entradas del registro</span><span class="sxs-lookup"><span data-stu-id="925e9-103">Decoder-Specific Registry Entries</span></span>


<span data-ttu-id="925e9-104">Además de las entradas del registro necesarias para todos los codificadores y descodificadores, se requieren las siguientes entradas del registro específicamente para los descodificadores.</span><span class="sxs-lookup"><span data-stu-id="925e9-104">In addition to the registry entries required for all encoders and decoders, the following registry entries are required specifically for decoders.</span></span>

<span data-ttu-id="925e9-105">Estas entradas registran el descodificador en la categoría de descodificadores de componentes de creación de imágenes de Windows (WIC).</span><span class="sxs-lookup"><span data-stu-id="925e9-105">These entries register your decoder under the category of Windows Imaging Component (WIC) decoders.</span></span> <span data-ttu-id="925e9-106">El primer GUID de estas entradas es el identificador de categoría (CATId) para [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span><span class="sxs-lookup"><span data-stu-id="925e9-106">The first GUID in these entries is the category identifier (CATID) for [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

<span data-ttu-id="925e9-107">Como se indicó en la sección de [detección y arbitraje](-wic-howwicworks.md) de cómo funciona el componente de creación de imágenes de Windows, el mecanismo que permite detectar un descodificador adecuado para una imagen específica se detecta en tiempo de ejecución se basa en la coincidencia de un patrón de identificación incrustado en el archivo de imagen con un patrón especificado en la entrada del registro del descodificador.</span><span class="sxs-lookup"><span data-stu-id="925e9-107">As noted in [Discovery and Arbitration](-wic-howwicworks.md) section of How The Windows Imaging Component Works, the mechanism that enables an appropriate decoder for a specific image to be discovered at run time is based on matching an identifying pattern embedded in the image file with a pattern specified in the decoder’s registry entry.</span></span> <span data-ttu-id="925e9-108">Para habilitar la detección en tiempo de ejecución de los descodificadores, debe registrar el patrón de identificación único para el formato de imagen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="925e9-108">To enable run-time discovery of decoders, you must register the unique identifying pattern for your image format as follows.</span></span> <span data-ttu-id="925e9-109">Todas estas entradas del registro son necesarias, a excepción de la entrada **EndOfStream** , que es opcional, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="925e9-109">All of these registry entries are required except for the **EndOfStream** entry, which is optional, as described in the following table.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| <span data-ttu-id="925e9-110">Value</span><span class="sxs-lookup"><span data-stu-id="925e9-110">Value</span></span>       | <span data-ttu-id="925e9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="925e9-111">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="925e9-112">Posición</span><span class="sxs-lookup"><span data-stu-id="925e9-112">Position</span></span>    | <span data-ttu-id="925e9-113">Desplazamiento en el archivo donde se puede encontrar el patrón.</span><span class="sxs-lookup"><span data-stu-id="925e9-113">The offset into the file where the pattern can be found.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="925e9-114">Length</span><span class="sxs-lookup"><span data-stu-id="925e9-114">Length</span></span>      | <span data-ttu-id="925e9-115">Longitud del patrón.</span><span class="sxs-lookup"><span data-stu-id="925e9-115">The length of the pattern.</span></span>                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="925e9-116">Patrón</span><span class="sxs-lookup"><span data-stu-id="925e9-116">Pattern</span></span>     | <span data-ttu-id="925e9-117">Bits reales que componen el modelo.</span><span class="sxs-lookup"><span data-stu-id="925e9-117">The actual bits that make up the pattern.</span></span> <span data-ttu-id="925e9-118">Estos son los bits que se comparan con el patrón de identificación en un archivo de imagen durante la detección.</span><span class="sxs-lookup"><span data-stu-id="925e9-118">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="925e9-119">Máscara</span><span class="sxs-lookup"><span data-stu-id="925e9-119">Mask</span></span>        | <span data-ttu-id="925e9-120">Permite valores comodín en los patrones.</span><span class="sxs-lookup"><span data-stu-id="925e9-120">Allows for wildcard values in patterns.</span></span> <span data-ttu-id="925e9-121">La máscara se aplica mediante la realización de una operación AND lógica en el patrón y la máscara.</span><span class="sxs-lookup"><span data-stu-id="925e9-121">The mask is applied by performing a logical AND operation on the pattern and the mask.</span></span> <span data-ttu-id="925e9-122">Cualquier bit del patrón que se corresponda con un bit de la máscara con un valor de 0 se omite.</span><span class="sxs-lookup"><span data-stu-id="925e9-122">Any bit in the pattern that corresponds to a bit in the mask with a value of 0 is ignored.</span></span>                                                                                                       |
| <span data-ttu-id="925e9-123">EndOfStream</span><span class="sxs-lookup"><span data-stu-id="925e9-123">EndOfStream</span></span> | <span data-ttu-id="925e9-124">El desplazamiento del patrón de identificación se debe calcular desde el final de la secuencia, en lugar de desde el principio.</span><span class="sxs-lookup"><span data-stu-id="925e9-124">The offset of the identifying pattern should be calculated from the end of the stream, rather than the beginning.</span></span> <span data-ttu-id="925e9-125">Algunos formatos de imagen colocan el patrón de identificación en el final del archivo o cerca de él.</span><span class="sxs-lookup"><span data-stu-id="925e9-125">Some image formats place the identifying pattern at or near the end of the file.</span></span> <span data-ttu-id="925e9-126">Dado que el valor predeterminado es buscar desde el principio, a menos que el patrón esté cerca del final del archivo, puede omitir esta entrada.</span><span class="sxs-lookup"><span data-stu-id="925e9-126">Because the default is to seek from the beginning, unless your pattern is near the end of the file, you can omit this entry.</span></span> |



 

<span data-ttu-id="925e9-127">Un códec puede admitir más de un patrón de identificación.</span><span class="sxs-lookup"><span data-stu-id="925e9-127">A codec can support more than one identifying pattern.</span></span> <span data-ttu-id="925e9-128">En ese caso, se repiten todas las claves de **\_ las clases HKEY \_ raíz \\ CLSID \\ {Encoder CLSID} \\ patrones** y se usa la clave numérica (0 en el ejemplo) para distinguir entre los distintos patrones.</span><span class="sxs-lookup"><span data-stu-id="925e9-128">In that case, you would repeat all of the keys under **HKEY\_CLASSES\_ROOT\\CLSID\\{Decoder CLSID}\\Patterns**, and use the numerical key (0 in the example) to distinguish between the different patterns.</span></span> <span data-ttu-id="925e9-129">Debe incluir cada uno de los cuatro valores de la clave para cada patrón.</span><span class="sxs-lookup"><span data-stu-id="925e9-129">You must include each of the four values under the key for each pattern.</span></span>

## <a name="registering-a-container-format-with-metadata-readers"></a><span data-ttu-id="925e9-130">Registro de un formato de contenedor con lectores de metadatos</span><span class="sxs-lookup"><span data-stu-id="925e9-130">Registering a Container Format with Metadata Readers</span></span>

<span data-ttu-id="925e9-131">Si crea un nuevo formato de contenedor para el códec, también debe crear entradas del registro para admitir la detección de lectores de metadatos para los bloques de metadatos de las imágenes, tal como hizo con los escritores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="925e9-131">If you create a new container format for your codec, you must also create registry entries to support discovery of metadata readers for the metadata blocks in your images, just as you did for the metadata writers.</span></span> <span data-ttu-id="925e9-132">Las siguientes entradas deben crearse en el identificador de clase (CLSID) del lector de metadatos para cada formato de metadatos que admita el formato de contenedor.</span><span class="sxs-lookup"><span data-stu-id="925e9-132">The following entries need to be created under the class identifier (CLSID) of the metadata reader for each metadata format your container format supports.</span></span> <span data-ttu-id="925e9-133">(Tenga en cuenta que, si el códec usa un contenedor de Tagged Image File Format (TIFF), esta información ya está en el registro).</span><span class="sxs-lookup"><span data-stu-id="925e9-133">(Note that, if your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry.)</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

<span data-ttu-id="925e9-134">Dado que las entradas de los lectores de metadatos también se usan para la detección, son muy similares a las entradas de los descodificadores.</span><span class="sxs-lookup"><span data-stu-id="925e9-134">Because the entries for metadata readers are also used for discovery, they are very similar to the entries for decoders.</span></span> <span data-ttu-id="925e9-135">El generador de componentes usa estas entradas para buscar los lectores de metadatos admitidos por el contenedor y seleccionar el adecuado cuando la implementación de [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) solicita un lector de metadatos.</span><span class="sxs-lookup"><span data-stu-id="925e9-135">These entries are used by the component factory to find the metadata readers supported by your container, and to select the appropriate one, when your [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) implementation requests a metadata reader.</span></span>



| <span data-ttu-id="925e9-136">Value</span><span class="sxs-lookup"><span data-stu-id="925e9-136">Value</span></span>      | <span data-ttu-id="925e9-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="925e9-137">Description</span></span>                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="925e9-138">Posición</span><span class="sxs-lookup"><span data-stu-id="925e9-138">Position</span></span>   | <span data-ttu-id="925e9-139">Desplazamiento en el contenedor del bloque de metadatos donde se puede encontrar el encabezado de metadatos.</span><span class="sxs-lookup"><span data-stu-id="925e9-139">The offset in the metadata block’s container where the metadata header can be found.</span></span> <span data-ttu-id="925e9-140">En el caso de los bloques de metadatos de nivel superior, este es el desplazamiento en la secuencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="925e9-140">For top-level metadata blocks, this is the offset in the file stream.</span></span> <span data-ttu-id="925e9-141">En el caso de los bloques de metadatos anidados en otros bloques de metadatos, es el desplazamiento relativo al bloque de metadatos contenedor.</span><span class="sxs-lookup"><span data-stu-id="925e9-141">For metadata blocks nested in other metadata blocks, it is the offset relative to the containing metadata block.</span></span> |
| <span data-ttu-id="925e9-142">Patrón</span><span class="sxs-lookup"><span data-stu-id="925e9-142">Pattern</span></span>    | <span data-ttu-id="925e9-143">Bits reales que componen el modelo.</span><span class="sxs-lookup"><span data-stu-id="925e9-143">The actual bits that make up the pattern.</span></span> <span data-ttu-id="925e9-144">Estos son los bits que se comparan con el patrón de identificación en un archivo de imagen durante la detección.</span><span class="sxs-lookup"><span data-stu-id="925e9-144">These are the bits that are matched against the identifying pattern in an image file during discovery.</span></span>                                                                                                                            |
| <span data-ttu-id="925e9-145">Máscara</span><span class="sxs-lookup"><span data-stu-id="925e9-145">Mask</span></span>       | <span data-ttu-id="925e9-146">El encabezado de metadatos se define generalmente mediante el controlador de metadatos.</span><span class="sxs-lookup"><span data-stu-id="925e9-146">The metadata header is generally defined by the metadata handler.</span></span> <span data-ttu-id="925e9-147">Debe utilizar el encabezado de metadatos estándar para cada lector a menos que, por algún motivo, el patrón deba tener un formato diferente en el contenedor.</span><span class="sxs-lookup"><span data-stu-id="925e9-147">You should use the standard metadata header for each reader unless, for some reason, the pattern must have a different format in your container.</span></span>                                                          |
| <span data-ttu-id="925e9-148">DataOffset</span><span class="sxs-lookup"><span data-stu-id="925e9-148">DataOffset</span></span> | <span data-ttu-id="925e9-149">Desplazamiento desde el principio del encabezado de metadatos en el que se inician los datos reales.</span><span class="sxs-lookup"><span data-stu-id="925e9-149">The offset from the beginning of the metadata header at which the actual data begins.</span></span> <span data-ttu-id="925e9-150">En los casos en los que los metadatos no se encuentran en un desplazamiento específico del encabezado, esta entrada se puede omitir.</span><span class="sxs-lookup"><span data-stu-id="925e9-150">In cases where the metadata isn’t located at a specific offset from the header, this entry can be omitted.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="925e9-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="925e9-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="925e9-152">**Vista**</span><span class="sxs-lookup"><span data-stu-id="925e9-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="925e9-153">Entradas del registro específicas del codificador</span><span class="sxs-lookup"><span data-stu-id="925e9-153">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)
</dt> <dt>

[<span data-ttu-id="925e9-154">Integración con la Galería fotográfica de Windows y el explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="925e9-154">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)
</dt> <dt>

[<span data-ttu-id="925e9-155">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="925e9-155">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="925e9-156">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="925e9-156">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



