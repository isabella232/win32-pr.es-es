---
description: En este tema se proporciona información sobre el códec ICO nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Información general sobre el formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d370497e9231d6deb8d1793a26a53565b5cd99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707133"
---
# <a name="ico-format-overview"></a>Información general sobre el formato ICO

En este tema se proporciona información sobre el códec ICO nativo disponible a través de Windows Imaging Component (WIC).

## <a name="codec-identity"></a>Identidad del códec

En la tabla siguiente se proporciona información de identificación del códec.



|                        |                   |
|------------------------|-------------------|
| Nombres formales         | Formato de icono (ICO) |
| Extensiones de nombre de archivo | ICO               |
| Tipo de MIME              | imagen/ICO         |
| Compatibilidad con las especificaciones  |                   |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes del códec ICO nativo.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatIco | a3a860c4-338f-4c17-919afba4b5628f21 |
| Descodificador          | CLSID \_ WICIcoDecoder     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| Codificador          | NO DISPONIBLE            | NO DISPONIBLE                       |



 

## <a name="encoding"></a>Encoding

WIC no proporciona un codificador de imágenes ICO nativo.

## <a name="decoding"></a>Descodificación

La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md). Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

 

 



