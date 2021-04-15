---
description: En este artículo se describe cómo el administrador de gráficos de filtro localiza un filtro de origen, dado un nombre de archivo.
ms.assetid: bc0d5719-6325-40fe-8261-ad00b91f272c
title: Registro de un tipo de archivo personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e98c01555497ac628fff452f464c826475edbb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677092"
---
# <a name="registering-a-custom-file-type"></a><span data-ttu-id="9a874-103">Registro de un tipo de archivo personalizado</span><span class="sxs-lookup"><span data-stu-id="9a874-103">Registering a Custom File Type</span></span>

<span data-ttu-id="9a874-104">En este artículo se describe cómo el administrador de gráficos de filtro localiza un filtro de origen, dado un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="9a874-104">This article describes how the Filter Graph Manager locates a source filter, given a file name.</span></span> <span data-ttu-id="9a874-105">Puede usar este mecanismo para registrar sus propios tipos de archivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="9a874-105">You can use this mechanism to register your own custom file types.</span></span> <span data-ttu-id="9a874-106">Una vez registrado el tipo de archivo, DirectShow cargará automáticamente el filtro de origen correcto cada vez que una aplicación llame a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span><span class="sxs-lookup"><span data-stu-id="9a874-106">Once the file type is registered, DirectShow will automatically load the correct source filter whenever an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) or [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).</span></span>

-   [<span data-ttu-id="9a874-107">Información general</span><span class="sxs-lookup"><span data-stu-id="9a874-107">Overview</span></span>](#overview)
-   [<span data-ttu-id="9a874-108">Protocolos</span><span class="sxs-lookup"><span data-stu-id="9a874-108">Protocols</span></span>](#protocols)
-   [<span data-ttu-id="9a874-109">Extensiones de archivo</span><span class="sxs-lookup"><span data-stu-id="9a874-109">File Extensions</span></span>](#file-extensions)
-   [<span data-ttu-id="9a874-110">Comprobar bytes</span><span class="sxs-lookup"><span data-stu-id="9a874-110">Check Bytes</span></span>](#check-bytes)
-   [<span data-ttu-id="9a874-111">Cargar el filtro de origen</span><span class="sxs-lookup"><span data-stu-id="9a874-111">Loading the Source Filter</span></span>](#loading-the-source-filter)
-   [<span data-ttu-id="9a874-112">Tipos de archivo personalizados en Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="9a874-112">Custom File Types in Windows Media Player</span></span>](#custom-file-types-in-windows-media-player)
-   [<span data-ttu-id="9a874-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a874-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="9a874-114">Información general</span><span class="sxs-lookup"><span data-stu-id="9a874-114">Overview</span></span>

<span data-ttu-id="9a874-115">Para buscar un filtro de origen a partir de un nombre de archivo determinado, el administrador de gráficos de filtros intenta hacer lo siguiente, en orden:</span><span class="sxs-lookup"><span data-stu-id="9a874-115">To locate a source filter from a given file name, the Filter Graph Manager attempts to do the following, in order:</span></span>

1.  <span data-ttu-id="9a874-116">Coincide con el protocolo, si existe.</span><span class="sxs-lookup"><span data-stu-id="9a874-116">Match the protocol, if any.</span></span>
2.  <span data-ttu-id="9a874-117">Coincide con la extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="9a874-117">Match the file extension.</span></span>
3.  <span data-ttu-id="9a874-118">Coincide con patrones de bytes dentro del archivo, denominado *check bytes*.</span><span class="sxs-lookup"><span data-stu-id="9a874-118">Match patterns of bytes within the file, called *check bytes*.</span></span>

## <a name="protocols"></a><span data-ttu-id="9a874-119">Protocolos</span><span class="sxs-lookup"><span data-stu-id="9a874-119">Protocols</span></span>

<span data-ttu-id="9a874-120">Los nombres de protocolo como "FTP" o "http" se registran en el</span><span class="sxs-lookup"><span data-stu-id="9a874-120">Protocol names such as "ftp" or "http" are registered under the</span></span>

<span data-ttu-id="9a874-121">**\_clase HKEY \_ raíz**</span><span class="sxs-lookup"><span data-stu-id="9a874-121">**HKEY\_CLASSES\_ROOT**</span></span>

<span data-ttu-id="9a874-122">clave, con la siguiente estructura:</span><span class="sxs-lookup"><span data-stu-id="9a874-122">key, with the following structure:</span></span>


```C++
HKEY_CLASSES_ROOT
    <protocol>
        Source Filter = <Source filter CLSID>
        Extensions
            <.ext1> = <Source filter CLSID>
            <.ext2> = <Source filter CLSID>
```



<span data-ttu-id="9a874-123">Si el nombre de archivo o la dirección URL contienen dos puntos (': '), el administrador de gráficos de filtros intenta usar la parte anterior a ': ' como nombre de protocolo.</span><span class="sxs-lookup"><span data-stu-id="9a874-123">If the file name or URL contains a colon (':'), the Filter Graph Manager attempts to use the portion before the ':' as a protocol name.</span></span> <span data-ttu-id="9a874-124">Por ejemplo, si el nombre es "myprot://myfile.ext", busca una clave del **registro denominada me**.</span><span class="sxs-lookup"><span data-stu-id="9a874-124">For example, if the name is "myprot://myfile.ext", it searches for a registry key named **myprot**.</span></span> <span data-ttu-id="9a874-125">Si esta clave existe y contiene una subclave denominada "Extensions", el administrador de gráficos de filtro busca en esa subclave las entradas que coinciden con la extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="9a874-125">If this key exists and contains a subkey named "Extensions", the Filter Graph Manager searches within that subkey for entries that match the file extension.</span></span> <span data-ttu-id="9a874-126">El valor de la clave debe ser un GUID en formato de cadena. por ejemplo, " {00000000-0000-0000-0000-000000000000} ".</span><span class="sxs-lookup"><span data-stu-id="9a874-126">The value of the key must be a GUID in string form; for example, "{00000000-0000-0000-0000-000000000000}".</span></span> <span data-ttu-id="9a874-127">Si Filter Graph Manager no puede coincidir con nada de la subclave **extensions** , busca una subclave denominada **filtro de origen**, que también debe ser un GUID en formato de cadena.</span><span class="sxs-lookup"><span data-stu-id="9a874-127">If the Filter Graph Manager cannot match anything within the **Extensions** subkey, it looks for a subkey named **Source Filter**, which must also be a GUID in string form.</span></span>

<span data-ttu-id="9a874-128">Si el administrador de gráficos de filtro encuentra un GUID coincidente, lo usa como CLSID del filtro de origen e intenta cargar el filtro.</span><span class="sxs-lookup"><span data-stu-id="9a874-128">If the Filter Graph Manager finds a matching GUID, it uses this as the CLSID of the source filter, and attempts to load the filter.</span></span> <span data-ttu-id="9a874-129">Si no encuentra ninguna coincidencia, utiliza el filtro de [origen de archivo (URL)](file-source--url--filter.md) , que trata el nombre de archivo como una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="9a874-129">If it does not find a match, it uses the [File Source (URL)](file-source--url--filter.md) filter, which treats the file name as a URL.</span></span>

<span data-ttu-id="9a874-130">Hay dos excepciones a este algoritmo:</span><span class="sxs-lookup"><span data-stu-id="9a874-130">There are two exceptions to this algorithm:</span></span>

-   <span data-ttu-id="9a874-131">Para excluir Letras de controlador, las cadenas de un solo carácter no se consideran protocolos.</span><span class="sxs-lookup"><span data-stu-id="9a874-131">To exclude driver letters, single-character strings are not considered protocols.</span></span>
-   <span data-ttu-id="9a874-132">Si la cadena es "File:" o "file://", no se trata como un protocolo.</span><span class="sxs-lookup"><span data-stu-id="9a874-132">If the string is "file:" or "file://", it is not treated as a protocol.</span></span>

## <a name="file-extensions"></a><span data-ttu-id="9a874-133">Extensiones de archivo</span><span class="sxs-lookup"><span data-stu-id="9a874-133">File Extensions</span></span>

<span data-ttu-id="9a874-134">Si no hay ningún protocolo en el nombre de archivo, el administrador de gráficos de filtro busca en el registro entradas con **las \_ \_ \\ \\ extensiones \\ de tipo de medio raíz de las clases HKEY** de clave.*EXT* \\ , donde.*EXT* es la extensión de archivo.</span><span class="sxs-lookup"><span data-stu-id="9a874-134">If there is no protocol in the file name, the Filter Graph Manager looks in the registry for entries with the key **HKEY\_CLASSES\_ROOT\\Media Type\\Extensions\\**.*ext*\\, where .*ext* is the file extension.</span></span> <span data-ttu-id="9a874-135">Si esta clave existe, el **filtro de origen** del valor contiene el CLSID del filtro de origen, en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="9a874-135">If this key exists, the value **Source Filter** contains the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="9a874-136">Opcionalmente, la clave puede tener valores para el **tipo de medio** y el **subtipo**, que proporcionan los GUID de tipo y subtipo principales.</span><span class="sxs-lookup"><span data-stu-id="9a874-136">Optionally, the key can have values for **Media Type** and **Subtype**, which give the major type and subtype GUIDs.</span></span>

## <a name="check-bytes"></a><span data-ttu-id="9a874-137">Comprobar bytes</span><span class="sxs-lookup"><span data-stu-id="9a874-137">Check Bytes</span></span>

<span data-ttu-id="9a874-138">Algunos tipos de archivo se pueden identificar mediante patrones específicos de bits que se producen en determinados desplazamientos de bytes en el archivo.</span><span class="sxs-lookup"><span data-stu-id="9a874-138">Some file types can be identified by specific patterns of bits occurring at specific byte offsets in the file.</span></span> <span data-ttu-id="9a874-139">Filter Graph Manager busca claves con el siguiente formato en el registro:</span><span class="sxs-lookup"><span data-stu-id="9a874-139">The Filter Graph Manager looks in the registry for keys with the following form:</span></span>

<span data-ttu-id="9a874-140">**HKEY \_ Clases \_ \\ mediatype \\ raíz**{ *tipo principal* } \\ { *SubType* }</span><span class="sxs-lookup"><span data-stu-id="9a874-140">**HKEY\_CLASSES\_ROOT\\MediaType\\**{ *major type* }\\{ *subtype* }</span></span>

<span data-ttu-id="9a874-141">donde *major Type* y *SubType* son GUID que definen el tipo de medio para la secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="9a874-141">where *major type* and *subtype* are GUIDs that define the media type for the byte stream.</span></span> <span data-ttu-id="9a874-142">Cada clave contiene una o más subclaves, normalmente denominadas 1, 2, etc., que definen los bytes de comprobación; y una subclave denominada **filtro de origen** que proporciona el CLSID del filtro de origen, en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="9a874-142">Each key contains one or more subkeys, usually named 1, 2, and so on, which define the check bytes; and a subkey named **Source Filter** that gives the CLSID of the source filter, in string form.</span></span> <span data-ttu-id="9a874-143">Las subclaves check-byte son cadenas que contienen uno o más cuádruples de números denominados:</span><span class="sxs-lookup"><span data-stu-id="9a874-143">The check-byte subkeys are strings that contain one or more quads of numbers called:</span></span>

<span data-ttu-id="9a874-144">*offset*, *CB*, *Mask*, *Val*</span><span class="sxs-lookup"><span data-stu-id="9a874-144">*offset*, *cb*, *mask*, *val*</span></span>

<span data-ttu-id="9a874-145">Para que coincida con el archivo, el administrador de gráficos de filtro Lee los bytes CB, empezando por el desplazamiento del número de bytes.</span><span class="sxs-lookup"><span data-stu-id="9a874-145">To match the file, the Filter Graph Manager reads cb bytes, starting from byte number offset.</span></span> <span data-ttu-id="9a874-146">A continuación, realiza una operación and bit a bit con el valor de Mask.</span><span class="sxs-lookup"><span data-stu-id="9a874-146">It then performs a bitwise-AND against the value in mask.</span></span> <span data-ttu-id="9a874-147">Si el resultado es igual a Val, el archivo es una coincidencia para ese cuádruple.</span><span class="sxs-lookup"><span data-stu-id="9a874-147">If the result equals val, the file is a match for that quad.</span></span> <span data-ttu-id="9a874-148">Los valores Mask y Val se proporcionan en hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="9a874-148">The values mask and val are given in hex.</span></span> <span data-ttu-id="9a874-149">Una entrada en blanco para Mask se trata como una cadena de 1s de longitud CB.</span><span class="sxs-lookup"><span data-stu-id="9a874-149">A blank entry for mask is treated as a string of 1s of length cb.</span></span> <span data-ttu-id="9a874-150">Un valor negativo para PosiciónInicial indica un desplazamiento desde el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="9a874-150">A negative value for offset indicates an offset from the end of the file.</span></span> <span data-ttu-id="9a874-151">Para que coincida con la clave, el archivo debe coincidir con todas las cuádruples de cualquiera de las subclaves.</span><span class="sxs-lookup"><span data-stu-id="9a874-151">To match the key, the file must match all of the quads in any of the subkeys.</span></span>

<span data-ttu-id="9a874-152">Por ejemplo, supongamos que el registro contiene las siguientes claves en el **\\ tipo de medio HKCR**:</span><span class="sxs-lookup"><span data-stu-id="9a874-152">For example, assume the registry contains the following keys under **HKCR\\Media Type**:</span></span>


```C++
{e436eb83-524f-11ce-9f53-0020af0ba770}
    {7364696D-0000-0010-8000-00AA00389B71}
        0                    "0,4,,52494646,8,4,,524D4944"
        1                    "0,4,,4D546864"
        Source Filter        "{E436EBB5-524F-11CE-9F53-0020AF0BA770}"
```



<span data-ttu-id="9a874-153">La primera clave corresponde a la secuencia de tipo MEDIATYPE principal \_ .</span><span class="sxs-lookup"><span data-stu-id="9a874-153">The first key corresponds to the major type MEDIATYPE\_Stream.</span></span> <span data-ttu-id="9a874-154">La subclave siguiente que corresponde al subtipo MEDIATYPE \_ MIDI.</span><span class="sxs-lookup"><span data-stu-id="9a874-154">The subkey below that corresponds to the subtype MEDIATYPE\_Midi.</span></span> <span data-ttu-id="9a874-155">El valor de la subclave de filtro de origen es CLSID \_ AsyncReader, el CLSID del filtro de [origen de archivo (Async)](file-source--async--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="9a874-155">The value for the Source Filter subkey is CLSID\_AsyncReader, the CLSID of the [File Source (Async)](file-source--async--filter.md) filter.</span></span>

<span data-ttu-id="9a874-156">Cada entrada puede tener varios cuadruplican; todos ellos deben coincidir.</span><span class="sxs-lookup"><span data-stu-id="9a874-156">Each entry can have multiple quadruples; all of them must match.</span></span> <span data-ttu-id="9a874-157">En el ejemplo siguiente, los cuatro primeros bytes del archivo deben ser 0xAB, 0xCD, 0X12, 0x34; y los últimos 4 bytes del archivo deben ser 0xAB, 0xAB, 0x00, 0xAB:</span><span class="sxs-lookup"><span data-stu-id="9a874-157">In the following example, the first 4 bytes of the file must be 0xAB, 0xCD, 0x12, 0x34; and the last 4 bytes of the file must be 0xAB, 0xAB, 0x00, 0xAB:</span></span>


```C++
    0, 4, , ABCD1234,  -4, 4, , ABAB00AB 
```



<span data-ttu-id="9a874-158">Además, puede haber varias entradas enumeradas bajo un solo tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="9a874-158">Also, there can be multiple entries listed under a single media type.</span></span> <span data-ttu-id="9a874-159">Es suficiente una coincidencia con cualquiera de ellas.</span><span class="sxs-lookup"><span data-stu-id="9a874-159">A match to any of them is sufficient.</span></span> <span data-ttu-id="9a874-160">Este esquema permite un conjunto de máscaras alternativas; por ejemplo, archivos. wav que pueden tener o no un encabezado RIFF.</span><span class="sxs-lookup"><span data-stu-id="9a874-160">This scheme allows for a set of alternative masks; for instance, .wav files that might or might not have a RIFF header.</span></span>

> [!Note]  
> <span data-ttu-id="9a874-161">Este esquema es similar al utilizado por la función [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) .</span><span class="sxs-lookup"><span data-stu-id="9a874-161">This scheme is similar to the one used by the [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile) function.</span></span>

 

## <a name="loading-the-source-filter"></a><span data-ttu-id="9a874-162">Cargar el filtro de origen</span><span class="sxs-lookup"><span data-stu-id="9a874-162">Loading the Source Filter</span></span>

<span data-ttu-id="9a874-163">Suponiendo que el administrador de gráficos de filtro encuentra un filtro de origen coincidente para el archivo, agrega ese filtro al gráfico, consulta el filtro para la interfaz [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) y llama a [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span><span class="sxs-lookup"><span data-stu-id="9a874-163">Assuming that the Filter Graph Manager finds a matching source filter for the file, it adds that filter to the graph, queries the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface, and calls [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load).</span></span> <span data-ttu-id="9a874-164">Los argumentos para el método **Load** son el nombre de archivo y el tipo de medio, tal y como se determina en el registro.</span><span class="sxs-lookup"><span data-stu-id="9a874-164">The arguments to the **Load** method are the file name and the media type, as determined from the registry.</span></span>

<span data-ttu-id="9a874-165">Si el administrador de gráficos de filtro no encuentra nada en el registro, se usa de forma predeterminada el filtro de origen de archivo asincrónico.</span><span class="sxs-lookup"><span data-stu-id="9a874-165">If the Filter Graph Manager cannot find anything from the registry, it defaults to using the Async File Source filter.</span></span> <span data-ttu-id="9a874-166">En ese caso, establece el tipo de medio en **\_ flujo de MEDIATYPE**, **MEDIASUBTYPE \_ ninguno**.</span><span class="sxs-lookup"><span data-stu-id="9a874-166">In that case, it sets the media type to **MEDIATYPE\_Stream**, **MEDIASUBTYPE\_None**.</span></span>

## <a name="custom-file-types-in-windows-media-player"></a><span data-ttu-id="9a874-167">Tipos de archivo personalizados en Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="9a874-167">Custom File Types in Windows Media Player</span></span>

<span data-ttu-id="9a874-168">Windows Media Player usa un conjunto adicional de entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="9a874-168">Windows Media Player uses an additional set of registry entries.</span></span> <span data-ttu-id="9a874-169">Para obtener más información, consulte [configuración del registro](../wmp/file-name-extension-registry-settings.md) de la extensión de nombre de archivo en el SDK de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9a874-169">For more information, see [File Name Extension Registry Settings](../wmp/file-name-extension-registry-settings.md) in the Windows Media Player SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a874-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9a874-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a874-171">Escribir filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="9a874-171">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 
