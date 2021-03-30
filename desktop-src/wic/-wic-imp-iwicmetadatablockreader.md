---
description: Implementar IWICMetadataBlockReader
ms.assetid: 80ad8e20-a9d4-4503-94ba-1b7699e36111
title: Implementar IWICMetadataBlockReader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bfe53e87dae52d004fa90d1104fb60f252085d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910166"
---
# <a name="implementing-iwicmetadatablockreader"></a><span data-ttu-id="c0953-103">Implementar IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="c0953-103">Implementing IWICMetadataBlockReader</span></span>

## <a name="iwicmetadatablockreader"></a><span data-ttu-id="c0953-104">IWICMetadataBlockReader</span><span class="sxs-lookup"><span data-stu-id="c0953-104">IWICMetadataBlockReader</span></span>

<span data-ttu-id="c0953-105">A menudo existen varios bloques de metadatos en una imagen, cada uno de los cuales expone diferentes tipos de información en distintos formatos.</span><span class="sxs-lookup"><span data-stu-id="c0953-105">Multiple blocks of metadata often exist within an image, each exposing different types of information in different formats.</span></span> <span data-ttu-id="c0953-106">En el modelo de componentes de imágenes de Windows (WIC), los controladores de metadatos son componentes distintos que, como los descodificadores, son reconocibles en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="c0953-106">In the Windows Imaging Component (WIC) model, metadata handlers are distinct components that, like decoders, are discoverable at run time.</span></span> <span data-ttu-id="c0953-107">Cada formato de metadatos tiene un controlador independiente, y cada uno de estos controladores de metadatos se puede usar con cualquier formato de imagen que admita el formato de metadatos que controla.</span><span class="sxs-lookup"><span data-stu-id="c0953-107">Each metadata format has a separate handler, and each of these metadata handlers can be used with any image format that supports the metadata format it handles.</span></span> <span data-ttu-id="c0953-108">Por lo tanto, si el formato de imagen admite EXIF, XMP, IPTC u otro formato, puede aprovechar los controladores de metadatos estándar para estos formatos que se distribuyen con WIC y no es necesario que escriba los suyos propios.</span><span class="sxs-lookup"><span data-stu-id="c0953-108">Therefore, if your image format supports EXIF, XMP, IPTC, or another format, you can take advantage of the standard metadata handlers for these formats that ship with WIC, and you do not need to write your own.</span></span> <span data-ttu-id="c0953-109">Por supuesto, si crea un nuevo formato de metadatos, debe escribir un controlador de metadatos para él, que se detectará y se invocará en tiempo de ejecución del mismo modo que los estándares.</span><span class="sxs-lookup"><span data-stu-id="c0953-109">Of course, if you create a new metadata format, you must write a metadata handler for it, which will be discovered and invoked at run time just as the standard ones are.</span></span>

> [!Note]  
> <span data-ttu-id="c0953-110">Si el formato de la imagen se basa en un contenedor Tagged Image File Format (TIFF) o JPEG, no tendrá que escribir ningún controlador de metadatos (a menos que desarrolle un formato de metadatos nuevo o propietario).</span><span class="sxs-lookup"><span data-stu-id="c0953-110">If your image format is based on a Tagged Image File Format (TIFF) or JPEG container, you won’t need to write any metadata handlers (unless you develop a new or proprietary metadata format).</span></span> <span data-ttu-id="c0953-111">En los contenedores TIFF y JPEG, los bloques de metadatos se encuentran dentro de IFDs y cada contenedor tiene una estructura de IFD diferente.</span><span class="sxs-lookup"><span data-stu-id="c0953-111">In TIFF and JPEG containers, blocks of metadata are located within IFDs, and each container has a different IFD structure.</span></span> <span data-ttu-id="c0953-112">WIC proporciona controladores de IFD para ambos formatos de contenedor que navegan por la estructura de IFD y delegan en los controladores de metadatos estándar para tener acceso a los metadatos de ellos.</span><span class="sxs-lookup"><span data-stu-id="c0953-112">WIC provides IFD handlers for both of these container formats that navigate the IFD structure and delegate to the standard metadata handlers to access the metadata within them.</span></span> <span data-ttu-id="c0953-113">Por lo tanto, si el formato de la imagen se basa en cualquiera de estos contenedores, puede aprovechar automáticamente los controladores de la IFD de WIC.</span><span class="sxs-lookup"><span data-stu-id="c0953-113">So, if your image format is based on either of these containers, you can automatically take advantage of the WIC IFD handlers.</span></span> <span data-ttu-id="c0953-114">Sin embargo, si tiene un formato de contenedor propietario que tiene su propia estructura de metadatos de nivel superior única, debe escribir un controlador que pueda navegar por esa estructura de nivel superior y delegar en los controladores de metadatos adecuados, al igual que hacen los controladores de IFD.</span><span class="sxs-lookup"><span data-stu-id="c0953-114">However, if you have a proprietary container format that has its own unique top-level metadata structure, you must write a handler that can navigate that top-level structure and delegate to the appropriate metadata handlers, just like the IFD handlers do.)</span></span>

 

<span data-ttu-id="c0953-115">Del mismo modo que WIC proporciona una capa de abstracción para aplicaciones que les permite trabajar con todos los formatos de imagen de la misma manera a través de un conjunto coherente de interfaces, WIC proporciona una capa de abstracción para los autores de códecs con respecto a los formatos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="c0953-115">The same way WIC provides a layer of abstraction for applications that allows them to work with all image formats in the same way through a consistent set of interfaces, WIC provides a layer of abstraction for codec authors with regard to metadata formats.</span></span> <span data-ttu-id="c0953-116">Como se indicó anteriormente, los creadores de códecs no suelen tener que trabajar directamente con los distintos formatos de metadatos que pueden estar presentes en una imagen.</span><span class="sxs-lookup"><span data-stu-id="c0953-116">As noted previously, codec authors generally do not need to work directly with the various metadata formats that may be present in an image.</span></span> <span data-ttu-id="c0953-117">Sin embargo, cada autor de códec es responsable de proporcionar una manera de enumerar los bloques de metadatos para que se pueda detectar y crear una instancia de un controlador de metadatos adecuado para cada bloque.</span><span class="sxs-lookup"><span data-stu-id="c0953-117">However, every codec author is responsible for providing a way to enumerate the blocks of metadata so an appropriate metadata handler can be discovered and instantiated for each block.</span></span>

<span data-ttu-id="c0953-118">Debe implementar esta interfaz en la clase de descodificación de nivel de marco.</span><span class="sxs-lookup"><span data-stu-id="c0953-118">You must implement this interface on your frame-level decoding class.</span></span> <span data-ttu-id="c0953-119">También puede ser necesario implementarlo en la clase descodificador de nivel de contenedor si el formato de la imagen expone metadatos globales fuera de los fotogramas de imagen individuales.</span><span class="sxs-lookup"><span data-stu-id="c0953-119">You may also need to implement it on your container-level decoder class if your image format exposes global metadata outside of any individual image frames.</span></span>

``` syntax
interface IWICMetadataBlockReader : IUnknown
{
   // All methods required
   HRESULT GetContainerFormat ( GUID *pguidContainerFormat );
   HRESULT GetCount ( UINT *pcCount );
   HRESULT GetEnumerator ( IEnumUnknown **ppIEnumMetadata );
   HRESULT GetReaderByIndex ( UINT nIndex, IWICMetadataReader **ppIMetadataReader );
}
```

-   [<span data-ttu-id="c0953-120">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="c0953-120">GetContainerFormat</span></span>](#getcontainerformat)
-   [<span data-ttu-id="c0953-121">GetCount</span><span class="sxs-lookup"><span data-stu-id="c0953-121">GetCount</span></span>](#getcount)
-   [<span data-ttu-id="c0953-122">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="c0953-122">GetEnumerator</span></span>](#getenumerator)
-   [<span data-ttu-id="c0953-123">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="c0953-123">GetReaderByIndex</span></span>](#getreaderbyindex)

### <a name="getcontainerformat"></a><span data-ttu-id="c0953-124">GetContainerFormat</span><span class="sxs-lookup"><span data-stu-id="c0953-124">GetContainerFormat</span></span>

<span data-ttu-id="c0953-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) es el mismo que el método [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) en la [implementación de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span><span class="sxs-lookup"><span data-stu-id="c0953-125">[**GetContainerFormat**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat) is the same as the [GetContainerFormat](-wic-imp-iwicbitmapdecoder.md) method on [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).</span></span>

### <a name="getcount"></a><span data-ttu-id="c0953-126">GetCount</span><span class="sxs-lookup"><span data-stu-id="c0953-126">GetCount</span></span>

<span data-ttu-id="c0953-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) devuelve el número de bloques de metadatos de nivel superior asociados al marco.</span><span class="sxs-lookup"><span data-stu-id="c0953-127">[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) returns the number of top-level metadata blocks associated with the frame.</span></span>

### <a name="getenumerator"></a><span data-ttu-id="c0953-128">GetEnumerator</span><span class="sxs-lookup"><span data-stu-id="c0953-128">GetEnumerator</span></span>

<span data-ttu-id="c0953-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) devuelve un enumerador que el llamador puede utilizar para enumerar los bloques de metadatos del marco y leer sus metadatos.</span><span class="sxs-lookup"><span data-stu-id="c0953-129">[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator) returns an enumerator that the caller can use to enumerate over the metadata blocks in the frame and read their metadata.</span></span> <span data-ttu-id="c0953-130">Para implementar este método, debe crear un lector de metadatos para cada bloque de metadatos e implementar un objeto de enumeración que Enumere la colección de lectores de metadatos.</span><span class="sxs-lookup"><span data-stu-id="c0953-130">To implement this method, you need to create a metadata reader for each block of metadata, and implement an enumeration object that enumerates over the collection of metadata readers.</span></span> <span data-ttu-id="c0953-131">El objeto de enumeración debe implementar [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) para que pueda convertirlo en IEnumUnknown cuando lo devuelva en el parámetro *ppIEnumMetadata* .</span><span class="sxs-lookup"><span data-stu-id="c0953-131">The enumeration object must implement [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) so you can cast it to IEnumUnknown when you return it in the *ppIEnumMetadata* parameter.</span></span>

<span data-ttu-id="c0953-132">Al implementar el objeto de enumeración, se pueden crear todos los lectores de metadatos cuando se crea por primera vez el objeto [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) o cuando se crea por primera vez el objeto de enumeración, o se pueden crear de forma diferida dentro de la implementación del método [IEnumUnknown:: Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) .</span><span class="sxs-lookup"><span data-stu-id="c0953-132">When implementing the enumeration object, you can create all the metadata readers when you first create the [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object or when you first create the enumeration object, or you can create them lazily inside the implementation of the [IEnumUnknown::Next](/windows/win32/api/objidlbase/nf-objidlbase-ienumunknown-next) method.</span></span> <span data-ttu-id="c0953-133">En muchos casos, es más eficaz crearlos de forma diferida pero, en el ejemplo siguiente, se crean todos los lectores de bloque en el constructor para ahorrar espacio.</span><span class="sxs-lookup"><span data-stu-id="c0953-133">In many cases, it’s more efficient to create them lazily but, in the following example, the block readers are all created in the constructor to save space.</span></span>


```C++
public class MetadataReaderEnumerator : public IEnumUnknown
{
   UINT m_current;
   UINT m_blockCount;
   IWICMetadataReader** m_ppMetadataReader;
   IStream* m_pStream;

   MetadataReaderEnumerator() 
   {
       // Set m_blockCount to the number of metadata blocks in the frame. 
      ...
      m_ppMetadataReader = IWICMetadataReader*[m_blockCount];
       m_current = 0;

      for (UINT x=0; x < m_blockCount; x++) 
      {
         // Find the position in the file where the xth
         // block of metadata lives and seek m_piStream 
         // to that position.
         ...

         m_pComponentFactory->CreateMetadataReaderFromContainer(
            GUID_ContainerFormatTiff,
                        NULL,
                        WICPersistOptions.WICPersistOptionsDefault | 
            WICMetadataCreationOptions.WICMetadataCreationDefault, 
                        m_pStream, &m_ppMetadataReader[x]);
        }
    }

    // Implementation of IEnumUnknown and IUnknown interfaces
    ...
}
```



<span data-ttu-id="c0953-134">Para crear los lectores de metadatos, se usa el método [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) .</span><span class="sxs-lookup"><span data-stu-id="c0953-134">To create the metadata readers, you use the [**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) method.</span></span> <span data-ttu-id="c0953-135">Al invocar este método, se pasa el GUID del formato de contenedor en el parámetro *guidContainerFormat* .</span><span class="sxs-lookup"><span data-stu-id="c0953-135">When invoking this method, you pass in the GUID of the container format in the *guidContainerFormat* parameter.</span></span> <span data-ttu-id="c0953-136">Si tiene una preferencia de proveedor para un lector de metadatos, puede pasar el GUID de su proveedor preferido en el parámetro *pGuidVendor* .</span><span class="sxs-lookup"><span data-stu-id="c0953-136">If you have a preference of vendor for a metadata reader, you can pass the GUID of your preferred vendor in the *pGuidVendor* parameter.</span></span> <span data-ttu-id="c0953-137">Por ejemplo, si su compañía escribe controladores de metadatos y desea utilizar el suyo propio, puede pasar el GUID del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c0953-137">For example, if your company writes metadata handlers, and you want to use your own if present, you can pass in your vendor GUID.</span></span> <span data-ttu-id="c0953-138">En la mayoría de los casos, simplemente pasaría **null** y dejar que el sistema Seleccione el lector de metadatos adecuado.</span><span class="sxs-lookup"><span data-stu-id="c0953-138">In most cases, you would just pass **NULL**, and let the system select the appropriate metadata reader.</span></span> <span data-ttu-id="c0953-139">Si solicita un proveedor específico y ese proveedor tiene un lector de metadatos instalado en el equipo, WIC devolverá el lector del proveedor.</span><span class="sxs-lookup"><span data-stu-id="c0953-139">If you do request a specific vendor, and that vendor does have a metadata reader installed on the computer, WIC will return that vendor’s reader.</span></span> <span data-ttu-id="c0953-140">Sin embargo, si el proveedor solicitado no tiene un lector de metadatos instalado en el equipo y está disponible un lector de metadatos adecuado, se devolverá ese lector aunque no sea del proveedor preferido.</span><span class="sxs-lookup"><span data-stu-id="c0953-140">However, if the requested vendor does not have a metadata reader installed on the computer, and if there is an appropriate metadata reader available, that reader will be returned even though it is not from the preferred vendor.</span></span> <span data-ttu-id="c0953-141">Si no hay ningún lector de metadatos en el equipo para el tipo de metadatos en el bloque, el generador de componentes devolverá el controlador de metadatos desconocido, que tratará el bloque de metadatos como un objeto binario grande (BLOB) y deserializará el bloque de metadatos del archivo sin que se intente analizarlo.</span><span class="sxs-lookup"><span data-stu-id="c0953-141">If there is no metadata reader on the computer for the type of metadata in the block, the component factory will return the Unknown Metadata Handler, which will treat the block of metadata as a binary large object (BLOB), and will deserialize the block of metadata from the file without any attempt at parsing it.</span></span>

<span data-ttu-id="c0953-142">Para el parámetro *dwOptions* , realice una operación OR entre el [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) adecuado con el [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions)adecuado.</span><span class="sxs-lookup"><span data-stu-id="c0953-142">For the *dwOptions* parameter, perform an OR operation between the appropriate [**WICPersistOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicpersistoptions) with the appropriate [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions).</span></span> <span data-ttu-id="c0953-143">El **WICPersistOptions** describe cómo se diseña el contenedor. Little-Endian es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c0953-143">The **WICPersistOptions** describe how your container is laid out. Little-endian is the default.</span></span>

``` syntax
enum WICPersistOptions
{   
   WICPersistOptionDefault,
   WICPersistOptionLittleEndian,
   WICPersistOptionBigEndian,
   WICPersistOptionStrictFormat,
   WICPersistOptionNoCacheStream,
   WICPersistOptionPreferUTF8
};
```

<span data-ttu-id="c0953-144">El [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) especifica si desea obtener el UnknownMetadataHandler si no se encuentra ningún lector de metadatos en el equipo que pueda leer el formato de metadatos de un bloque determinado.</span><span class="sxs-lookup"><span data-stu-id="c0953-144">The [**WICMetadataCreationOptions**](/windows/desktop/api/Wincodecsdk/ne-wincodecsdk-wicmetadatacreationoptions) specify whether you want to get back the UnknownMetadataHandler if no metadata reader is found on the machine that can read the metadata format of a particular block.</span></span> <span data-ttu-id="c0953-145">**WICMetadataCreationAllowUnknown** es el valor predeterminado y siempre debe permitir la creación de UnknownMetadtataHandler.</span><span class="sxs-lookup"><span data-stu-id="c0953-145">**WICMetadataCreationAllowUnknown** is the default, and you should always allow creation of the UnknownMetadtataHandler.</span></span> <span data-ttu-id="c0953-146">UnknownMetadataHandler trata los metadatos no reconocidos como un BLOB.</span><span class="sxs-lookup"><span data-stu-id="c0953-146">The UnknownMetadataHandler treats unrecognized metadata as a BLOB.</span></span> <span data-ttu-id="c0953-147">No puede analizarlo, pero lo escribe en la secuencia como un BLOB y lo conserva intacto cuando se vuelve a escribir en la secuencia durante la codificación.</span><span class="sxs-lookup"><span data-stu-id="c0953-147">It cannot parse it, but it writes it out into the stream as a BLOB, and persists it intact when it’s written back to the stream during encoding.</span></span> <span data-ttu-id="c0953-148">Esto hace que sea seguro crear controladores de metadatos para metadatos de propietario o formatos de metadatos que no se distribuyen con el sistema.</span><span class="sxs-lookup"><span data-stu-id="c0953-148">This makes it safe to create metadata handlers for proprietary metadata or metadata formats that don’t ship with the system.</span></span> <span data-ttu-id="c0953-149">Dado que los metadatos se conservan intactos, incluso si no hay ningún controlador en el equipo que lo reconozca, cuando se instale posteriormente un controlador de metadatos adecuado, los metadatos seguirán estando allí y se podrán leer.</span><span class="sxs-lookup"><span data-stu-id="c0953-149">Because metadata is preserved intact, even if no handler is present on the computer that recognizes it, when an appropriate metadata handler is later installed, the metadata will still be there and can be read.</span></span> <span data-ttu-id="c0953-150">Si no permite la creación de UnknownMetadataHandler, la alternativa es descartar o sobrescribir metadatos no reconocidos.</span><span class="sxs-lookup"><span data-stu-id="c0953-150">If you don’t allow creation of the UnknownMetadataHandler, the alternative is discarding or overwriting unrecognized metadata.</span></span> <span data-ttu-id="c0953-151">Se trata de una forma de pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="c0953-151">This is a form of data loss.</span></span>

> [!Note]  
> <span data-ttu-id="c0953-152">Si escribe su propio controlador de metadatos para los metadatos de propiedad, nunca debe incluir referencias a nada fuera del propio bloque de metadatos.</span><span class="sxs-lookup"><span data-stu-id="c0953-152">If you write your own metadata handler for proprietary metadata, you should never include references to anything outside the metadata block itself.</span></span> <span data-ttu-id="c0953-153">Aunque el UnknownMetadataHandler conserva los metadatos intactos, los metadatos se mueven cuando se editan los archivos y las referencias a cualquier elemento que esté fuera de su propio bloque dejarán de ser válidos cuando esto suceda.</span><span class="sxs-lookup"><span data-stu-id="c0953-153">Even though the UnknownMetadataHandler preserves metadata intact, metadata does get moved when files are edited, and any references to anything outside its own block will no longer be valid when this happens.</span></span>

 

``` syntax
enum WICMetadataCreationOptions
{
   WICMetadataCreationDefault = 0x00000000,
   WICMetadataCreationAllowUnknown = WICMetadataCreationDefault,
   WICMetadataCreationFailUnknown = 0x00010000,
   WICMetadataCreationMask = 0xFFFF0000
};
```

<span data-ttu-id="c0953-154">El parámetro *pIStream* es el flujo real que se va a descodificar.</span><span class="sxs-lookup"><span data-stu-id="c0953-154">The *pIStream* parameter is the actual stream that you are decoding.</span></span> <span data-ttu-id="c0953-155">Antes de pasar el flujo, debe buscar el principio del bloque de metadatos para el que está solicitando un lector.</span><span class="sxs-lookup"><span data-stu-id="c0953-155">Before passing in the stream, you should seek to the beginning of the metadata block for which you’re requesting a reader.</span></span> <span data-ttu-id="c0953-156">El lector de metadatos adecuado para el bloque de metadatos en la posición actual en [IStream](/windows/desktop/api/objidl/nn-objidl-istream) se devolverá en el parámetro *ppiReader* .</span><span class="sxs-lookup"><span data-stu-id="c0953-156">The appropriate metadata reader for the metadata block at the current position in the [IStream](/windows/desktop/api/objidl/nn-objidl-istream) will be returned in the *ppiReader* parameter.</span></span>

### <a name="getreaderbyindex"></a><span data-ttu-id="c0953-157">GetReaderByIndex</span><span class="sxs-lookup"><span data-stu-id="c0953-157">GetReaderByIndex</span></span>

<span data-ttu-id="c0953-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) devuelve el lector de metadatos en el índice solicitado de la colección.</span><span class="sxs-lookup"><span data-stu-id="c0953-158">[**GetReaderByIndex**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex) returns the metadata reader at the requested index in the collection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0953-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0953-159">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c0953-160">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="c0953-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c0953-161">**IWICMetadataBlockReader**</span><span class="sxs-lookup"><span data-stu-id="c0953-161">**IWICMetadataBlockReader**</span></span>](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)
</dt> <dt>

<span data-ttu-id="c0953-162">**Vista**</span><span class="sxs-lookup"><span data-stu-id="c0953-162">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c0953-163">Implementación de IWICBitmapFrameDecode</span><span class="sxs-lookup"><span data-stu-id="c0953-163">Implementing IWICBitmapFrameDecode</span></span>](-wic-imp-iwicbitmapframedecode.md)
</dt> <dt>

[<span data-ttu-id="c0953-164">Implementación de IWICBitmapSourceTransform</span><span class="sxs-lookup"><span data-stu-id="c0953-164">Implementing IWICBitmapSourceTransform</span></span>](-wic-imp-iwicbitmapsourcetransform.md)
</dt> <dt>

[<span data-ttu-id="c0953-165">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="c0953-165">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="c0953-166">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="c0953-166">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
