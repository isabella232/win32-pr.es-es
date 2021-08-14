---
description: Proporciona información sobre el códec DDS nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Introducción al formato DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a9fd00f17d17b7bb227a04e56bbc9369de86eb03f9c953a73267400d4a6df9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204483"
---
# <a name="dds-format-overview"></a>Introducción al formato DDS

En este tema se proporciona información sobre el códec DDS nativo disponible a través de Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad de códec

En la tabla siguiente se proporciona información de identificación de códecs.



| Componente              | Descripción        |
|------------------------|--------------------|
| Nombres formales         | DirectDraw Surface |
| Extensiones de nombre de archivo | Dds                |
| Tipo de MIME              | image/vnd-ms.dds   |



 

En la tabla siguiente se enumeran los GUID usados para identificar los componentes de códec DDS nativos.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatDds | 9967cb95-2e85-4ac8-8ca283d7ccd425c9 |
| Descodificador          | CLSID \_ WICDdsDecoder     | 9053699f-a341-429d-9e90ee437cf80c73 |
| Codificador          | CLSID \_ WICDdsEncoder     | a61dde94-66ce-4ac1-881b71680588895e |



 

## <a name="pixel-format-support"></a>Compatibilidad con formato de píxel

Tenga en cuenta que el formato DDS admite cualquier valor [**VÁLIDO DE DXGI \_ FORMAT.**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Sin embargo, el códec WIC DDS solo admite la codificación y la codificación de archivos que contienen los siguientes formatos:

-   DXGI \_ FORMAT \_ BC1 \_ UNORM
-   DXGI \_ FORMAT \_ BC2 \_ UNORM
-   DXGI \_ FORMAT \_ BC3 \_ UNORM

## <a name="encoding"></a>Encoding

Las API de codificación WIC están diseñadas para ser independientes del códec y, por tanto, la codificación de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, vea Información general [sobre codificación.](-wic-creating-encoder.md)

El formato de archivo DDS tiene requisitos únicos que surgen de su compatibilidad con conceptos como mapas mip y matrices de textura. Para controlar completamente la codificación de imágenes DDS, debe usar la interfaz [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) para establecer parámetros de codificación específicos de DDS.

## <a name="decoding"></a>Descodificación

Las API de decodificación de WIC están diseñadas para ser independientes del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre lacoding de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md) Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

## <a name="block-compressed-data-access"></a>Bloquear el acceso a datos comprimidos

Además de admitir las interfaces de códec WIC estándar, el descodificador DDS proporciona acceso directo a los datos comprimidos en bloque nativo mediante las interfaces específicas de DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) e [**IWICDdsFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode) Para usar estas interfaces, llame a QueryInterface fuera de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)respectivamente.

 

 
