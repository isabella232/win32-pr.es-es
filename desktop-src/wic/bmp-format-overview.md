---
description: En este tema se proporciona información sobre el códec BMP nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Información general sobre el formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3492189f80b43915bab94a7ea8359f2e5950f7c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814238"
---
# <a name="bmp-format-overview"></a>Información general sobre el formato BMP

En este tema se proporciona información sobre el códec BMP nativo disponible a través de Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad del códec

En la tabla siguiente se proporciona información de identificación del códec.



|                        |                       |
|------------------------|-----------------------|
| Nombres formales         | Formato de mapa de bits de Windows |
| Extensiones de nombre de archivo | BMP, DIB              |
| Tipo de MIME              | image/bmp             |
| Compatibilidad con las especificaciones  | Especificación de BMP V5  |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes nativos del códec BMP.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatBmp | 0af1d87e-fcfe-4188-bdeba7906471cbe3 |
| Descodificador          | CLSID \_ WICBmpDecoder     | 6b462062-7cbf-400d-9fdb813dd10f2778 |
| Codificador          | CLSID \_ WICBmpEncoder     | 69be8bb4-d66d-47c8-865aed1589433782 |



 

## <a name="encoding"></a>Encoding

La API de codificación WIC está diseñada para ser independiente del códec y, por lo tanto, la codificación de imágenes para códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las capacidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones del codificador pueden ser opciones básicas de WIC compatibles disponibles para todos los códigos habilitados para WIC (aunque no se admiten necesariamente) o las opciones específicas del códec diseñadas con el códec formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la interfaz **IPropertyBag2** para la codificación de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

En la tabla siguiente se enumeran las opciones del codificador WIC admitidas por el códec BMP nativo.



| Nombre de la propiedad               | VARTYPE      | Intervalo de valores                      | Valor predeterminado      |
|-----------------------------|--------------|----------------------------------|--------------------|
| **EnableV5Header32bppBGRA** | **VT \_ bool** | **VARIANTE \_ verdadera/variante \_ falsa** | **VARIANTE \_ false** |



 

### <a name="enablev5header32bppbgra"></a>EnableV5Header32bppBGRA

Especifica si se permite la codificación de datos en el \_ formato de píxel de GUID WICPixelFormat32bppBGRA. Si esta opción se establece en **Variant \_ true**, el BMP se escribirá con un encabezado BITMAPV5HEADER.

El valor predeterminado es **Variant \_ false**.

Si una opción de codificador está presente en la lista de opciones IPropertyBag2 que el códec no admite, se omite.

Nota para los archivos BMP de Windows de 16 y 32 bits, el códec BMP omite cualquier canal alfa, ya que muchos archivos de imagen heredados contienen datos no válidos en este canal adicional. A partir de Windows 8, los archivos BMP de Windows de 32 bits escritos con el **BITMAPV5HEADER** con contenido de canal alfa válido se leen como WICPixelFormat32bppBGRA

## <a name="decoding"></a>Descodificación

La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md). Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

 

 
