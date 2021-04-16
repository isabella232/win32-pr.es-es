---
description: El escritor de documentos XPS de Microsoft (MXDW) permite a los usuarios crear archivos de documentos XPS imprimiendo desde cualquier aplicación de Windows.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: Opciones de configuración de MXDW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4026a99baa33ec50bc3ad129ef6610a428f83ab
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689694"
---
# <a name="mxdw-configuration-settings"></a><span data-ttu-id="4f909-103">Opciones de configuración de MXDW</span><span class="sxs-lookup"><span data-stu-id="4f909-103">MXDW Configuration Settings</span></span>

<span data-ttu-id="4f909-104">El escritor de documentos XPS de Microsoft (MXDW) permite a los usuarios crear archivos de documentos XPS imprimiendo desde cualquier aplicación de Windows.</span><span class="sxs-lookup"><span data-stu-id="4f909-104">The Microsoft XPS Document Writer (MXDW) enables users to create XPS document files by printing from any Windows application.</span></span> <span data-ttu-id="4f909-105">Los desarrolladores de aplicaciones pueden controlar la siguiente configuración de salida de MXDW con las partes PrintTicket y PrintCapabilities del [esquema de impresión](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="4f909-105">Applications developers can control the following output settings of the MXDW using the PrintTicket and PrintCapabilities parts of the [Print Schema](./printschema.md).</span></span>

## <a name="jobinterleaving"></a><span data-ttu-id="4f909-106">JobInterleaving</span><span class="sxs-lookup"><span data-stu-id="4f909-106">JobInterleaving</span></span>

<span data-ttu-id="4f909-107">La configuración JobInterleaving controla el orden de intercalación del contenido de los documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="4f909-107">The JobInterleaving setting controls the content interleaving order for the XPS Documents.</span></span> <span data-ttu-id="4f909-108">Para obtener información sobre la intercalación de trabajos, vea la [especificación de papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="4f909-108">For information about job interleaving, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span> <span data-ttu-id="4f909-109">MXDW admite las dos opciones siguientes para esta configuración:</span><span class="sxs-lookup"><span data-stu-id="4f909-109">MXDW supports the following two options for this setting:</span></span>

-   <span data-ttu-id="4f909-110">**OFF** : esta opción deshabilita la intercalación para que todos los datos de cada elemento de contenido del documento sean contiguos, lo que mejora la eficacia del acceso aleatorio.</span><span class="sxs-lookup"><span data-stu-id="4f909-110">**Off** - This option disables interleaving so that all data for each content element in the document is contiguous, which improves the efficiency of random access.</span></span> <span data-ttu-id="4f909-111">Esta opción es la más adecuada para ver un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="4f909-111">This option is best for viewing an XPS document.</span></span>
-   <span data-ttu-id="4f909-112">**On** : esta opción habilita la intercalación, de modo que los datos de cada elemento de contenido se dividen y se reordenan para un procesamiento secuencial más eficaz.</span><span class="sxs-lookup"><span data-stu-id="4f909-112">**On** - This option enables interleaving so that data for each content element is broken up and reordered for more efficient sequential processing.</span></span> <span data-ttu-id="4f909-113">Esta opción es la más adecuada para la impresión y descarga Web.</span><span class="sxs-lookup"><span data-stu-id="4f909-113">This option is best for web download and printing.</span></span>

<span data-ttu-id="4f909-114">El ejemplo siguiente es un ejemplo del XML de PrintCapabilities que incluye la configuración JobInterleaving.</span><span class="sxs-lookup"><span data-stu-id="4f909-114">The following example is an example of the PrintCapabilities XML that includes the JobInterleaving setting.</span></span>


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="4f909-115">El XML de PrintTicket es similar, salvo que especifica una opción determinada.</span><span class="sxs-lookup"><span data-stu-id="4f909-115">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="4f909-116">Vea el [esquema de impresión](./printschema.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4f909-116">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="4f909-117">Dado que JobInterleaving no es una de las [palabras clave públicas del esquema de impresión](./print-schema-public-keywords.md), debe incluir una declaración del espacio de nombres (en este caso, "ns0000" en la etiqueta **PrintCapabilities** (o **PrintTicket**) al principio del documento de PrintCapabilities (o PrintTicket), tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f909-117">Since JobInterleaving is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a><span data-ttu-id="4f909-118">JobImageType</span><span class="sxs-lookup"><span data-stu-id="4f909-118">JobImageType</span></span>

<span data-ttu-id="4f909-119">JobImageType controla el formato de salida de los formatos de mapa de bits incrustados.</span><span class="sxs-lookup"><span data-stu-id="4f909-119">JobImageType controls the output format of embedded bitmap formats.</span></span> <span data-ttu-id="4f909-120">MXDW admite las siguientes cuatro opciones para esta configuración:</span><span class="sxs-lookup"><span data-stu-id="4f909-120">MXDW supports the following four options for this setting:</span></span>

-   <span data-ttu-id="4f909-121">**JPEGHigh** : esta opción especifica la imagen JPEG con un alto nivel de compresión.</span><span class="sxs-lookup"><span data-stu-id="4f909-121">**JPEGHigh** - This option specifies the JPEG image with a high level of compression.</span></span> <span data-ttu-id="4f909-122">Esta opción genera el tamaño de archivo más pequeño, pero la calidad de imagen más baja.</span><span class="sxs-lookup"><span data-stu-id="4f909-122">This option produces the smallest file size, but the lowest image quality.</span></span>
-   <span data-ttu-id="4f909-123">**JPEGMed** : esta opción especifica la imagen JPEG con un nivel medio de compresión.</span><span class="sxs-lookup"><span data-stu-id="4f909-123">**JPEGMed** - This option specifies the JPEG image with a medium level of compression.</span></span> <span data-ttu-id="4f909-124">Esta opción proporciona el mejor equilibrio entre el tamaño de archivo y la calidad de la imagen.</span><span class="sxs-lookup"><span data-stu-id="4f909-124">This option provides the best balance of file size and image quality.</span></span>
-   <span data-ttu-id="4f909-125">**JPEGLow** : esta opción especifica la imagen JPEG con un bajo nivel de compresión.</span><span class="sxs-lookup"><span data-stu-id="4f909-125">**JPEGLow** - This option specifies the JPEG image with a low level of compression.</span></span> <span data-ttu-id="4f909-126">Esta opción produce la menor reducción en el tamaño de archivo y la alta calidad de imagen.</span><span class="sxs-lookup"><span data-stu-id="4f909-126">This option produces the least reduction in file size and high image quality.</span></span>
-   <span data-ttu-id="4f909-127">**PNG** : esta opción especifica el formato de imagen PNG con compresión sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="4f909-127">**PNG** - This option specifies the PNG image format with lossless compression.</span></span> <span data-ttu-id="4f909-128">Esta opción genera el tamaño de archivo más grande y la calidad de imagen más alta.</span><span class="sxs-lookup"><span data-stu-id="4f909-128">This option produces the largest file size and the highest image quality.</span></span>

<span data-ttu-id="4f909-129">El XML de PrintCapabilities del valor JobImageType se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="4f909-129">The PrintCapabilities XML of the JobImageType setting appears below:</span></span>


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="4f909-130">El XML de PrintTicket es similar, salvo que especifica una opción determinada.</span><span class="sxs-lookup"><span data-stu-id="4f909-130">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="4f909-131">Vea el [esquema de impresión](./printschema.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4f909-131">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="4f909-132">Dado que JobImageType no es una de las [palabras clave públicas del esquema de impresión](./print-schema-public-keywords.md), debe incluir una declaración del espacio de nombres (en este caso, "ns0000" en la etiqueta **PrintCapabilities** (o **PrintTicket**) al principio del documento de PrintCapabilities (o PrintTicket), tal como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f909-132">Since JobImageType is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a><span data-ttu-id="4f909-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f909-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f909-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="4f909-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="4f909-135">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="4f909-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[<span data-ttu-id="4f909-136">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="4f909-136">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="4f909-137">Especificaciones de XPS y descargas de licencias</span><span class="sxs-lookup"><span data-stu-id="4f909-137">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
