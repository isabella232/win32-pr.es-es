---
description: Proporciona información sobre el códec DDS nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Información general sobre el formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c45222a66d5a250caaf46db465d2359e09b3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697224"
---
# <a name="dds-format-overview"></a>Información general sobre el formato DDS

En este tema se proporciona información sobre el códec DDS nativo disponible a través de Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad del códec

En la tabla siguiente se proporciona información de identificación del códec.



|                        |                    |
|------------------------|--------------------|
| Nombres formales         | Superficie de DirectDraw |
| Extensiones de nombre de archivo | DDS                |
| Tipo de MIME              | Image/vnd-ms. DDS   |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes del códec DDS nativo.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatDds | 9967cb95-2e85-4ac8-8ca283d7ccd425c9 |
| Descodificador          | CLSID \_ WICDdsDecoder     | 9053699f-a341-429d-9e90ee437cf80c73 |
| Codificador          | CLSID \_ WICDdsEncoder     | a61dde94-66ce-4ac1-881b71680588895e |



 

## <a name="pixel-format-support"></a>Compatibilidad con formato de píxeles

Tenga en cuenta que el formato DDS admite cualquier valor de [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) válido. Sin embargo, el códec DDS de WIC solo admite la descodificación y la codificación de archivos que contienen los formatos siguientes:

-   Formato de DXGI \_ \_ BC1 \_ UNORM
-   Formato de DXGI \_ \_ BC2 \_ UNORM
-   Formato de DXGI \_ \_ BC3 \_ UNORM

## <a name="encoding"></a>Encoding

Las API de codificación WIC están diseñadas para ser independientes del códec y, por lo tanto, la codificación de imágenes para códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

El formato de archivo DDS tiene requisitos únicos que surgen de su compatibilidad con conceptos como mapas de y matrices de texturas. Para ejercer el control completo sobre la codificación de imagen DDS, debe usar la interfaz [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) para establecer los parámetros de codificación específicos de DDS.

## <a name="decoding"></a>Descodificación

Las API de descodificación de WIC están diseñadas para ser independientes del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md). Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

## <a name="block-compressed-data-access"></a>Bloquear el acceso a datos comprimidos

Además de admitir las interfaces de códecs WIC estándar, el descodificador DDS proporciona acceso directo a los datos comprimidos de bloque nativo mediante las interfaces específicas de DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) y [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode). Para utilizar estas interfaces, llame a QueryInterface fuera de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) y [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectivamente.

 

 
