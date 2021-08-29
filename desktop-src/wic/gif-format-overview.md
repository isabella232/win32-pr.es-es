---
description: En este tema se proporciona información sobre el códec GIF nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Introducción al formato GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 345f3856c01ff94ba51ce16ccc64bd299312d75777b1f269c0cf9a4e67c56a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709504"
---
# <a name="gif-format-overview"></a>Introducción al formato GIF

En este tema se proporciona información sobre el códec GIF nativo disponible a través de Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad de códec

En la tabla siguiente se proporciona información de identificación de códecs.



|  Componente             | Descripción                           |
|------------------------|---------------------------------------|
| Nombres formales         | Formato de intercambio de gráficos 89a (GIF) |
| Extensiones de nombre de archivo | GIF                                   |
| Tipo de MIME              | image/gif                             |
| Compatibilidad con especificaciones  | Especificación GIF 89a/89 m             |



 

En la tabla siguiente se enumeran los GUID usados para identificar los componentes de códec GIF nativos.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatGif | 1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5 |
| Descodificador          | CLSID \_ WICGifDecoder     | 381dda3c-9ce9-4834-a23e1f98f8fc52be |
| Codificador          | CLSID \_ WICGifEncoder     | 114f5598-0b22-40a0-86a1c83ea495adbd |



 

## <a name="encoding"></a>Encoding

La API de codificación WIC está diseñada para ser independiente del códec y la codificación de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre la codificación de imágenes mediante la API de WIC, vea Información general [sobre codificación.](-wic-creating-encoder.md)

### <a name="encoder-options"></a>Opciones del codificador

Los códecs habilitados para WIC difieren en el nivel de opción de codificación. Las opciones del codificador reflejan las funcionalidades de un codificador de imagen y cada códec nativo admite un conjunto de estas opciones de codificador. Las opciones de codificador pueden ser opciones básicas compatibles con WIC disponibles para todos los códigos habilitados para WIC (aunque no necesariamente admitidos) o opciones específicas del códec diseñadas por el códec de formato de imagen. Para administrar estas opciones de codificación durante el proceso de codificación, WIC usa la [**interfaz IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Para obtener más información sobre el uso de la **interfaz IPropertyBag2 para** la codificación WIC , vea Información general [sobre la codificación.](-wic-creating-encoder.md)

El codificador GIF no admite ninguna opción básica de WIC y no proporciona opciones de codificador personalizadas. Si una opción de codificador está en la [**lista de opciones IPropertyBag2,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) se omite.

## <a name="decoding"></a>Descodificación

La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre lacoding de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md) Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

 

 
