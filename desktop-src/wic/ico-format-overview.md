---
description: En este tema se proporciona información sobre el códec ICO nativo disponible a través Windows Imaging Component (WIC).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Introducción al formato ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329a53a3b5d386c5e5386141162c608dc9db1ec0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444476"
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



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec ICO nativos.



| Componente        | Nombre descriptivo            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatIco | a3a860c4-338f-4c17-919afba4b5628f21 |
| Descodificador          | CLSID \_ WICIcoDecoder     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| Codificador          | NO DISPONIBLE            | NO DISPONIBLE                       |



 

## <a name="encoding"></a>Encoding

WIC no proporciona un codificador de imágenes ICO nativo.

## <a name="decoding"></a>Descodificación

La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre lacodación de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md) Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

 

 



