---
description: En este tema se proporciona información sobre el códec ICO nativo disponible a través Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Introducción al formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf90f0a31beb2d004dcb43e08cb0b6b1539021071ff2cb3302b3076033bc833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204075"
---
# <a name="ico-format-overview"></a>Introducción al formato ICO

En este tema se proporciona información sobre el códec ICO nativo disponible a través Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad de códec

En la tabla siguiente se proporciona información de identificación de códecs.



|   Componente            | Descripción       |
|------------------------|-------------------|
| Nombres formales         | Formato de icono (ICO) |
| Extensiones de nombre de archivo | Ico               |
| Tipo de MIME              | image/ico         |
| Compatibilidad con especificaciones  |                   |



 

En la tabla siguiente se enumeran los GUID usados para identificar los componentes nativos del códec ICO.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatIco | a3a860c4-338f-4c17-919afba4b5628f21 |
| Descodificador          | CLSID \_ WICIcoDecoder     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| Codificador          | NO DISPONIBLE            | NO DISPONIBLE                       |



 

## <a name="encoding"></a>Encoding

WIC no proporciona un codificador de imagen ICO nativo.

## <a name="decoding"></a>Descodificación

La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre lacoding de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md) Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

 

 



