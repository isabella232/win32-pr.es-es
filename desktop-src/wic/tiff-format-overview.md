---
description: En este tema se proporciona información sobre el códec TIFF nativo disponible a través Windows Imaging Component (WIC).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Información general sobre el formato TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 995b8635756a1cc807d3125240517ce5d1eef54d447540028408eb3048d6143a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841345"
---
# <a name="tiff-format-overview"></a>Información general sobre el formato TIFF

En este tema se proporciona información sobre el códec TIFF nativo disponible a través Windows Imaging Component (WIC).

-   [Identidad de códec](#codec-identity)
-   [Encoding](#encoding)
    -   [Opciones del codificador](#encoder-options)
-   [Descodificación](#decoding)

## <a name="codec-identity"></a>Identidad de códec

En la tabla siguiente se proporciona información de identificación de códecs.



|   Componente            |   Descripción                   |
|------------------------|---------------------------------|
| Nombres formales         | Tagged Image File Format (TIFF) |
| Extensiones de nombre de archivo | tiff, tif                       |
| Tipos MIME           | image/tiff, image/tif           |
| Compatibilidad con especificaciones  | Especificación TIFF 6.0          |



 

En la tabla siguiente se enumeran los GUID usados para identificar los componentes de códec TIFF nativos.



| Componente        | Nombre descriptivo             | GUID                                 |
|------------------|---------------------------|--------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatTiff | 163bcc30-e2e9-4f0b-961da3e9fdb788a3  |
| Descodificador          | CLSID \_ WICTiffDecoder     | b54e85d9-fe23-499f-8b886acea7137502b |
| Codificador          | CLSID \_ WICTiffEncoder     | 0131be10-2001-4c5f-a9b0cc88fab64ce8  |



 

## <a name="encoding"></a>Encoding

La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, vea Información general [sobre codificación.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las funcionalidades de un codificador de imagen y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones de codificador pueden ser opciones básicas compatibles con WIC disponibles para todos los códigos habilitados para WIC (aunque no necesariamente admitidos) o opciones específicas del códec diseñadas por el códec de formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la [**interfaz IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la **interfaz IPropertyBag2 para** la codificación WIC , vea Información general [sobre la codificación.](-wic-creating-encoder.md)

El códec TIFF usa opciones básicas de WIC. En la tabla siguiente se enumeran las opciones del codificador WIC compatibles con el códec TIFF nativo.

| Nombre de la propiedad         | VARTYPE | Intervalo de valores | Valor predeterminado    |
|-----------------------|---------|-------------|------------------|
| CompressionQuality    | VT \_ R4  | 0 - 1.0     | 0                |
| TiffCompressionMethod | VT \_ UI1 | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

Si hay una opción de codificador en la lista [**de opciones IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.

### <a name="compressionquality-option"></a>CompressionQuality (opción)

Especifica la calidad de compresión deseada. 0.0 indica el esquema de compresión menos eficaz disponible. Normalmente, este esquema da como resultado una codificación más rápida, pero una salida mayor. Un valor de 1,0 especifica el esquema de compresión más eficaz disponible. Normalmente, este esquema da como resultado una codificación más larga, pero genera una salida más pequeña.

El valor predeterminado es 0.

### <a name="tiffcompressionmethod-option"></a>Opción TiffCompressionMethod

Especifica el método de compresión TIFF.

El valor predeterminado es [**WICTiffCompressionDontCare.**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption)

## <a name="decoding"></a>Descodificación

Las API de decodificación de WIC están diseñadas para ser independientes del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre lacoding de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md) Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

 

 
