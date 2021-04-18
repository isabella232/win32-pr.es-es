---
description: En este tema se proporciona información sobre el códec TIFF nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Información general sobre el formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db603857da892d4b699bb7df7d8b3e2ee5566326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706997"
---
# <a name="tiff-format-overview"></a>Información general sobre el formato TIFF

En este tema se proporciona información sobre el códec TIFF nativo disponible a través de Windows Imaging Component (WIC).

-   [Identidad del códec](#codec-identity)
-   [Encoding](#encoding)
    -   [Opciones del codificador](#encoder-options)
-   [Descodificación](#decoding)

## <a name="codec-identity"></a>Identidad del códec

En la tabla siguiente se proporciona información de identificación del códec.



|                        |                                 |
|------------------------|---------------------------------|
| Nombres formales         | Tagged Image File Format (TIFF) |
| Extensiones de nombre de archivo | TIFF, TIF                       |
| Tipos MIME           | imagen/TIFF, imagen/TIF           |
| Compatibilidad con las especificaciones  | Especificación TIFF 6,0          |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes del códec TIFF nativo.



| Componente        | Nombre descriptivo             | GUID                                 |
|------------------|---------------------------|--------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatTiff | 163bcc30-e2e9-4f0b-961da3e9fdb788a3  |
| Descodificador          | CLSID \_ WICTiffDecoder     | b54e85d9-fe23-499f-8b886acea7137502b |
| Codificador          | CLSID \_ WICTiffEncoder     | 0131be10-2001-4c5f-a9b0cc88fab64ce8  |



 

## <a name="encoding"></a>Encoding

La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para los códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las capacidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones del codificador pueden ser opciones básicas de WIC compatibles disponibles para todos los códigos habilitados para WIC (aunque no se admiten necesariamente) o las opciones específicas del códec diseñadas con el códec formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la interfaz **IPropertyBag2** para la codificación de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

El códec TIFF usa las opciones básicas de WIC. En la tabla siguiente se enumeran las opciones del codificador WIC admitidas por el códec TIFF nativo.

| Nombre de la propiedad         | VARTYPE | Intervalo de valores | Valor predeterminado    |
|-----------------------|---------|-------------|------------------|
| CompressionQuality    | VT \_ R4  | 0-1,0     | 0                |
| TiffCompressionMethod | VT \_ UI1 | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

Si una opción de codificador está presente en la lista de opciones [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.

### <a name="compressionquality-option"></a>Opción CompressionQuality

Especifica la calidad de compresión deseada. 0,0 indica el esquema de compresión menos eficaz disponible. Normalmente, este esquema da como resultado una codificación más rápida pero una salida más grande. Un valor de 1,0 especifica el esquema de compresión más eficaz disponible. Normalmente, este esquema da como resultado una codificación más larga, pero genera una salida más pequeña.

El valor predeterminado es 0.

### <a name="tiffcompressionmethod-option"></a>Opción TiffCompressionMethod

Especifica el método de compresión TIFF.

El valor predeterminado es [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).

## <a name="decoding"></a>Descodificación

Las API de descodificación de WIC están diseñadas para ser independientes del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md). Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

 

 
