---
description: En este tema se proporciona información sobre el códec DNG nativo disponible a través de Windows Imaging Component (WIC).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Información general sobre el formato DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360762"
---
# <a name="dng-format-overview"></a>Información general sobre el formato DNG

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

En este tema se proporciona información sobre el códec DNG nativo disponible a través de Windows Imaging Component (WIC).

-   [Identidad del códec](#codec-identity)
-   [Descodificación](#decoding)

## <a name="codec-identity"></a>Identidad del códec

En la tabla siguiente se proporciona información de identificación del códec.



|                        |                                                      |
|------------------------|------------------------------------------------------|
| Nombres formales         | Negativo digital (DNG)                               |
| Extensiones de nombre de archivo | .dng                                                 |
| Tipos MIME           | imagen/DNG                                            |
| Compatibilidad con las especificaciones  | Versión de especificación negativa digital (DNG) 1.4.0.0 |



 

En la tabla siguiente se enumeran los GUID que se usan para identificar los componentes del códec DNG nativo.



| Componente        | Nombre descriptivo             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Formato de contenedor | GUID \_ ContainerFormatAdng | f3ff6d0d-38c0-41c4-b1fe1f3824f17b84 |
| Descodificador          | CLSID \_ WICAdngDecoder     | 981d9411-909e-42a7-8f5da747ff052edb |



 

## <a name="decoding"></a>Descodificación

La API de descodificación de WIC está diseñada para ser independiente del códec y la descodificación de imágenes para códecs habilitados para WIC es esencialmente la misma. Para obtener más información sobre la descodificación de imágenes, consulte la [información general sobre descodificación](-wic-creating-decoder.md). Para obtener más información sobre el uso de datos de imagen descodificados, vea [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

El descodificador no admite la descodificación de datos de sensor sin procesar y solo admite archivos con una representación de imagen sin formato insertada en una IFD con NewSubFileType igual a 1.

 

 



