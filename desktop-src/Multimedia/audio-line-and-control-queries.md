---
title: Consultas de línea y control de audio
description: Consultas de línea y control de audio
ms.assetid: f0954fc7-9961-410a-a638-a7025fb2616a
keywords:
- audio multimedia, controles mezcladores
- audio, controles mezcladores
- mezcladores de audio, líneas de audio
- líneas de audio
- mezcladores de audio, controles
- mezcladores, controles
- mezcladores, líneas de audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec581f2ddb54b06de8fa1a1b1356d9b80422ad5c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062978"
---
# <a name="audio-line-and-control-queries"></a>Consultas de línea y control de audio

Los servicios mezcladores proporcionan funciones para determinar información sobre las líneas de audio, los controles de línea de audio y los detalles del control. Los servicios también proporcionan funciones para establecer los detalles del control.

Puede usar la función [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo) para recuperar información sobre una línea de audio especificada. Esta función rellena la estructura [**MIXERLINE de**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline) una línea de audio de origen, una línea de audio de destino o un identificador de línea especificados. La estructura incluye el número de línea de destino, el número de canales de la línea de audio, así como un nombre corto y largo para la línea de audio.

La [**función mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols) recupera información general sobre uno o varios controles asociados a una línea de audio. Esta función rellena la estructura [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols) con información sobre el control o los controles especificados. Puede usar **mixerGetLineControls para** recuperar las propiedades de control de una de las siguientes opciones:

-   Todos los controles de una línea de origen especificada
-   Control especificado para una línea de código fuente especificada
-   Primer control de una clase específica para una línea de origen especificada

La [**función mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails) recupera las propiedades de un único control asociado a una línea de audio. Esta función rellena la [**estructura MIXERCONTROLDETAILS con**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta) los valores actuales de un control.

La [**función mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails) usa el contenido de la estructura **MIXERCONTROLDETAILS** para establecer las propiedades del control especificado. Debe asegurarse de que todos los miembros de esta estructura se rellenan antes de llamar a **mixerSetControlDetails.**

 

 