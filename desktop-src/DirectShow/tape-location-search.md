---
description: Búsqueda de ubicación de cinta
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: Búsqueda de ubicación de cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32dca3c2b52d1501207b5b86f4e30b148a57c3881a725284a21455f7c2789c69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050065"
---
# <a name="tape-location-search"></a>Búsqueda de ubicación de cinta

Aunque los dispositivos DV admiten un comando para buscar por código de tiempo o por número de seguimiento absoluto (ATN), el controlador MSDV no tiene una manera estándar independiente del dispositivo de acceder a estas funciones. La única opción consiste en enviar un comando de AV/C sin formato al controlador como se describe en el tema Emisión de [comandos de AV/C sin formato.](issuing-raw-av-c-commands.md)

El controlador UVC admite un conjunto de propiedades para las búsquedas de ubicación de cinta. Para enviar un comando de búsqueda, use la **interfaz IKsControl** y establezca la propiedad PROPSETID \_ EXT \_ TRANSPORT. El uso de un conjunto de propiedades es más seguro que enviar comandos de AV/C sin procesar al dispositivo, ya que los comandos de AV/C omiten el filtro y van directamente al controlador del dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una cámara dv](controlling-a-dv-camcorder.md)
</dt> <dt>

[Conjunto de propiedades de transporte de dispositivos externos](external-device-transport-property-set.md)
</dt> </dl>

 

 



