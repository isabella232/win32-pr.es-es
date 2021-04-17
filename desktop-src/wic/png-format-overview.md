---
description: En este tema se proporciona información sobre el códec PNG nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Información general sobre el formato PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118d6af831c8fb6f8cacc8407e90f610c0fc426d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706874"
---
# <a name="png-format-overview"></a>Información general sobre el formato PNG

En este tema se proporciona información sobre el códec PNG nativo disponible a través de Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad del códec

En la tabla siguiente se proporciona información de identificación del códec.



|                        |                                 |
|------------------------|---------------------------------|
| Nombres formales         | Formato PNG (Portable Network Graphics) |
| Extensiones de nombre de archivo | png                             |
| Tipo de MIME              | image/png                       |
| Compatibilidad con las especificaciones  | Especificación PNG 1,2           |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec PNG nativos.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatPng | 1b7cfaf4-713f-473c-bbcd6137425faeaf |
| Descodificador          | CLSID \_ WICPngDecoder     | 389ea17b-5078-4cde-b6ef25c15175c751 |
| Codificador          | CLSID \_ WICPngEncoder     | 27949969-876a-41d7-9447568f6a35a4dc |



 

### <a name="windows-8-and-later"></a>Windows 8 y versiones posteriores

A partir de Windows 8, WIC proporciona un descodificador PNG adicional

## <a name="encoding"></a>Encoding

La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para los códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las capacidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones del codificador pueden ser opciones básicas de WIC compatibles disponibles para todos los códigos habilitados para WIC (aunque no se admiten necesariamente) o las opciones específicas del códec diseñadas con el códec formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la interfaz **IPropertyBag2** para la codificación de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

El códec PNG usa las opciones básicas del codificador WIC. En la tabla siguiente se enumeran las opciones del codificador WIC admitidas por el códec PNG nativo.



| Nombre de la propiedad   | VARTYPE  | Intervalo de valores                                                 | Valor predeterminado                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| InterlaceOption | VT \_ bool | **True** / **False**                                          | **FALSE**                                                        |
| FilterOption    | VT \_ UI1  | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

Si una opción de codificador está presente en la lista de opciones [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que el códec no admite, se omite.

### <a name="interlaceoption"></a>InterlaceOption

Especifica si se codifican los datos de la imagen como entrelazados.

El valor predeterminado es **FALSE**.

### <a name="filteroption"></a>FilterOption

Especifica la opción de filtro que se va a utilizar para la compresión de imágenes.

El valor predeterminado es [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).

## <a name="decoding"></a>Descodificación

La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md). Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

El códec PNG nativo también admite [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) en la descodificación de fotogramas agregar opciones avanzadas para descodificar una secuencia de imágenes. Para obtener más información acerca de estas opciones avanzadas, consulte la [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

 

 
