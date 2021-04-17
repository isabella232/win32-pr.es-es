---
description: 'Integridad de características: interfaces recomendadas'
ms.assetid: 759bf253-7450-4895-a550-9f81f3498f79
title: 'Integridad de características: interfaces recomendadas'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1dba4bcc029b2205985afb443526376c0eecb16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697490"
---
# <a name="feature-completeness-recommended-interfaces"></a>Integridad de características: interfaces recomendadas

En la tabla siguiente se enumeran los códecs sin formato de Windows Imaging Component (WIC) que deben implementar.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Interfaz</th>
<th>Requerido para</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a></td>
<td>Descodificadores</td>
<td>Representa el punto inicial para descodificar un archivo de imagen. Proporciona acceso a las propiedades de nivel de contenedor como miniaturas, fotogramas y paleta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a></td>
<td>Descodificadores</td>
<td>Representa un marco de imagen específico dentro del contenedor que proporciona acceso a las propiedades de nivel de marco. Esta es la interfaz que descodifica los bits de imagen reales.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a></td>
<td>Descodificadores</td>
<td>Se requiere para enumerar y recorrer en iteración los bloques de metadatos e invocar los lectores de metadatos adecuados al leer de un archivo de imagen. <br/>
<blockquote>
[!Note]<br />
Si el formato de contenedor sin formato es compatible con TIFF o usa IFDs estándar o IRBs para almacenar metadatos EXIF o XMP, los creadores de códecs pueden optar por invocar los lectores de metadatos integrados en lugar de escribir los suyos propios.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform"><strong>IWICBitmapSourceTransform</strong></a></td>
<td>Descodificadores</td>
<td>Permite al llamador especificar el escalado, el recorte, la rotación o el formato de píxel deseado para la imagen descodificada, lo que puede mejorar significativamente el rendimiento del descodificador. Por ejemplo, los descodificadores JPEG y Protocolo de datagramas inalámbricos (WDP) de Microsoft usan un esquema de optimización piramidal para lograr una descodificación más rápida cuando el mapa de bits de destino es menor que el mapa de bits de origen. Windows Vista (y versiones posteriores) intentará usar esta interfaz para extraer una &quot; &quot; vista previa rápida de una imagen sin procesar siempre que falte la vista previa incrustada o menos de 1.024 píxeles en su dimensión más grande.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw"><strong>IWICDevelopRaw</strong></a></td>
<td>Descodificadores</td>
<td>Se requiere para los formatos sin formato. Expone parámetros que son específicos del procesamiento de imágenes sin procesar. Los códecs sin formato deben admitir todos los parámetros que se aplican al códec.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a></td>
<td>Codificadores</td>
<td>Representa el punto inicial para codificar un archivo de imagen. Esta interfaz se usa para establecer las propiedades de nivel de contenedor, como miniaturas, fotogramas y paleta. También es necesario invocar un escritor de metadatos para habilitar la persistencia de metadatos en el archivo de imagen. Por estos motivos, esta interfaz es necesaria incluso si no se admite la codificación del mapa de bits principal en el formato sin procesar.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a></td>
<td>Codificadores</td>
<td>Representa un marco de imagen específico dentro del contenedor. Esta interfaz se usa para codificar los bits de imagen reales y para establecer las propiedades y los metadatos de cada fotograma.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a></td>
<td>Codificadores</td>
<td>Necesario para recorrer en iteración los bloques de metadatos e invocar los escritores de metadatos adecuados al serializar un archivo de imagen.<br/>
<blockquote>
[!Note]<br />
Si el formato de contenedor sin formato es compatible con TIFF, los creadores de códecs pueden optar por invocar los escritores de metadatos integrados en lugar de escribir los suyos propios.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Instrucciones de WIC para formatos de imagen RAW de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




