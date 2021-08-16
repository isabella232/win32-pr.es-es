---
description: En este tema se proporciona información sobre el códec DNG nativo disponible a través Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Información general sobre el formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32719e3fa9f45802058708e83635e52e287524496ae49f13f2168362358a7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204382"
---
# <a name="dng-format-overview"></a>Información general sobre el formato DNG

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

En este tema se proporciona información sobre el códec DNG nativo disponible a través Windows Imaging Component (WIC).

-   [Identidad de códec](#codec-identity)
-   [Descodificación](#decoding)

## <a name="codec-identity"></a>Identidad de códec

En la tabla siguiente se proporciona información de identificación de códecs.



|     Componente          |  Descripción                                         |
|------------------------|------------------------------------------------------|
| Nombres formales         | Negativo digital (DNG)                               |
| Extensiones de nombre de archivo | .dng                                                 |
| Tipos MIME           | image/DNG                                            |
| Compatibilidad con especificaciones  | Especificación de negativo digital (DNG) versión 1.4.0.0 |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes de códec DNG nativos.



| Componente        | Nombre descriptivo             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatAdng | f3ff6d0d-38c0-41c4-b1fe1f3824f17b84 |
| Descodificador          | CLSID \_ WICAdngDecoder     | 981d9411-909e-42a7-8f5da747ff052edb |



 

## <a name="decoding"></a>Descodificación

La API de decoding de WIC está diseñada para ser independiente del códec y lacoding de imágenes para códecs habilitados para WIC es básicamente la misma. Para obtener más información sobre lacodación de imágenes, vea Información general [sobre la decodación.](-wic-creating-decoder.md) Para obtener más información sobre el uso de datos de imagen descodificados, vea Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

El descodificador no admite la descodificación de datos sin procesar del sensor y solo admite archivos con una representación de imagen sin procesar incrustada en un IFD con NewSubFileType igual a 1.

 

 



