---
description: En este tema se proporciona información sobre el códec BMP nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Información general sobre el formato BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a107704f883f061f8a39abecedb813f35ba4faf3d4477f56767c6a0f946403e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032012"
---
# <a name="bmp-format-overview"></a>Información general sobre el formato BMP

En este tema se proporciona información sobre el códec BMP nativo disponible a través de Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad de códec

En la tabla siguiente se proporciona información de identificación de códecs.



| Componente              | Descripción           |
|------------------------|-----------------------|
| Nombres formales         | Windows Formato de mapa de bits |
| Extensiones de nombre de archivo | bmp, dib              |
| Tipo de MIME              | image/bmp             |
| Compatibilidad con especificaciones  | Especificación BMP v5  |



 

En la tabla siguiente se enumeran los GUID usados para identificar los componentes de códec BMP nativos.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatBmp | 0af1d87e-fcfe-4188-bdeba7906471cbe3 |
| Descodificador          | CLSID \_ WICBmpDecoder     | 6b462062-7cbf-400d-9fdb813dd10f2778 |
| Codificador          | CLSID \_ WICBmpEncoder     | 69be8bb4-d66d-47c8-865aed1589433782 |



 

## <a name="encoding"></a>Encoding

La API de codificación WIC está diseñada para ser independiente del códec y, por tanto, la codificación de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, vea Información general [sobre codificación.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las funcionalidades de un codificador de imagen y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones de codificador pueden ser opciones básicas compatibles con WIC disponibles para todos los códigos habilitados para WIC (aunque no necesariamente admitidos) o opciones específicas del códec diseñadas por el códec de formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la [**interfaz IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la **interfaz IPropertyBag2 para** la codificación WIC, vea Información general [sobre la codificación.](-wic-creating-encoder.md)

En la tabla siguiente se enumeran las opciones del codificador WIC compatibles con el códec BMP nativo.



| Nombre de la propiedad               | VARTYPE      | Intervalo de valores                      | Valor predeterminado      |
|-----------------------------|--------------|----------------------------------|--------------------|
| **EnableV5Header32bppBGRA** | **VT \_ BOOL** | **VARIANT \_ TRUE/VARIANT \_ FALSE** | **VARIANT \_ FALSE** |



 

### <a name="enablev5header32bppbgra"></a>EnableV5Header32bppBGRA

Especifica si se permiten los datos de codificación en el formato de píxel \_ WICPixelFormat32bppBGRA de GUID. Si esta opción se establece en **VARIANT \_ TRUE,** bmp se escribirá con un encabezado BITMAPV5HEADER.

El valor predeterminado es **VARIANT \_ FALSE.**

Si hay una opción de codificador en la lista de opciones IPropertyBag2 que el códec no admite, se omite.

Tenga en cuenta que para los archivos BMP de 16 y 32 bits Windows, el códec BMP omite cualquier canal alfa, ya que muchos archivos de imagen heredados contienen datos no válidos en este canal adicional. A partir Windows 8, los archivos BMP de 32 bits Windows escritos con **BITMAPV5HEADER** con contenido de canal alfa válido se leen como WICPixelFormat32bppBGRA.

## <a name="decoding"></a>Descodificación

La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre lacoding de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md) Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

 

 
