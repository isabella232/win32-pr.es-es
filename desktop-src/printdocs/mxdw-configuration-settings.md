---
description: El Escritor de documentos XPS de Microsoft (MXDW) permite a los usuarios crear archivos de documento XPS mediante la impresión desde cualquier Windows aplicación.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: Configuración de MXDW Configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a75d45ea3ad9c8c74280d1e70e418ee0bf4823d1f0332e3d5c772d29976cf2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971194"
---
# <a name="mxdw-configuration-settings"></a>Configuración de MXDW Configuración

El Escritor de documentos XPS de Microsoft (MXDW) permite a los usuarios crear archivos de documento XPS mediante la impresión desde cualquier Windows aplicación. Los desarrolladores de aplicaciones pueden controlar la siguiente configuración de salida de MXDW mediante las partes PrintTicket e PrintCapabilities del [esquema de impresión](./printschema.md).

## <a name="jobinterleaving"></a>JobInterleaving

La configuración JobInterleaving controla el orden de intercalación de contenido para los documentos XPS. Para obtener información sobre la intercalación de trabajos, vea el [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf). MXDW admite las dos opciones siguientes para esta configuración:

-   **Desactivado:** esta opción deshabilita la intercalación para que todos los datos de cada elemento de contenido del documento sea contiguo, lo que mejora la eficacia del acceso aleatorio. Esta opción es mejor para ver un documento XPS.
-   **On:** esta opción habilita la intercalación para que los datos de cada elemento de contenido se desglosan y se reordenen para un procesamiento secuencial más eficaz. Esta opción es mejor para la descarga y la impresión web.

El ejemplo siguiente es un ejemplo del XML PrintCapabilities que incluye la configuración JobInterleaving.


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



PrintTicket XML es similar, salvo que especifica una opción determinada. Consulte el [esquema de impresión para](./printschema.md) obtener más información.

Puesto que JobInterleaving no es una de las palabras clave públicas del esquema de impresión [,](./print-schema-public-keywords.md)debe incluir una declaración del espacio de nombres (en este caso , "ns0000" en la etiqueta **PrintCapabilities** (o **PrintTicket)** al principio del documento PrintCapabilities (o PrintTicket), como se muestra en el ejemplo siguiente:


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a>JobImageType

JobImageType controla el formato de salida de los formatos de mapa de bits incrustados. MXDW admite las cuatro opciones siguientes para esta configuración:

-   **JPEGHigh:** esta opción especifica la imagen JPEG con un alto nivel de compresión. Esta opción genera el tamaño de archivo más pequeño, pero la calidad de imagen más baja.
-   **JPEGMed:** esta opción especifica la imagen JPEG con un nivel medio de compresión. Esta opción proporciona el mejor equilibrio entre el tamaño de archivo y la calidad de la imagen.
-   **JPEGLow:** esta opción especifica la imagen JPEG con un bajo nivel de compresión. Esta opción produce la menor reducción en el tamaño de archivo y la alta calidad de la imagen.
-   **PNG:** esta opción especifica el formato de imagen PNG con compresión sin pérdida de datos. Esta opción genera el tamaño de archivo más grande y la mayor calidad de imagen.

A continuación se muestra el XML PrintCapabilities de la configuración JobImageType:


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



PrintTicket XML es similar, salvo que especifica una opción determinada. Consulte el [esquema de impresión para](./printschema.md) obtener más información.

Puesto que JobImageType no es una de las palabras clave públicas del esquema de impresión [,](./print-schema-public-keywords.md)debe incluir una declaración del espacio de nombres (en este caso , "ns0000" en la etiqueta **PrintCapabilities** (o **PrintTicket)** al principio del documento PrintCapabilities (o PrintTicket), como se muestra en el ejemplo siguiente:


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[Esquema de impresión](./printschema.md)
</dt> <dt>

[Especificación XPS y descargas de licencias](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
