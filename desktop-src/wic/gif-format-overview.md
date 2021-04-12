---
description: En este tema se proporciona información sobre el códec GIF nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Información general sobre el formato GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f592b50300edf79c71ff4050a2c0d5aeba8b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277770"
---
# <a name="gif-format-overview"></a>Información general sobre el formato GIF

En este tema se proporciona información sobre el códec GIF nativo disponible a través de Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad del códec

En la tabla siguiente se proporciona información de identificación del códec.



|                        |                                       |
|------------------------|---------------------------------------|
| Nombres formales         | Formato de intercambio de gráficos 89A (GIF) |
| Extensiones de nombre de archivo | GIF                                   |
| Tipo de MIME              | image/gif                             |
| Compatibilidad con las especificaciones  | Especificación de GIF 89A/89m             |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes del códec GIF nativo.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatGif | 1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5 |
| Descodificador          | CLSID \_ WICGifDecoder     | 381dda3c-9ce9-4834-a23e1f98f8fc52be |
| Codificador          | CLSID \_ WICGifEncoder     | 114f5598-0b22-40a0-86a1c83ea495adbd |



 

## <a name="encoding"></a>Encoding

La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para los códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las capacidades de un codificador de imágenes y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones del codificador pueden ser opciones básicas de WIC compatibles disponibles para todos los códigos habilitados para WIC (aunque no se admiten necesariamente) o las opciones específicas del códec diseñadas con el códec formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la interfaz [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la interfaz **IPropertyBag2** para la codificación de WIC, consulte la [información general](-wic-creating-encoder.md)sobre la codificación.

El codificador GIF no es compatible con las opciones básicas de WIC y no proporciona opciones de codificador personalizadas. Si una opción de codificador está en la lista de opciones [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , se omite.

## <a name="decoding"></a>Descodificación

La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md). Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

 

 
