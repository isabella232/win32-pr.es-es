---
description: Búsqueda de ubicación de cinta
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: Búsqueda de ubicación de cinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d1fb719f3b43374e5aa86f34c60e5b8f14d536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688210"
---
# <a name="tape-location-search"></a>Búsqueda de ubicación de cinta

Aunque los dispositivos DV admiten un comando para buscar por código de tiempo o por número de pista absoluta (ATN), el controlador MSDV no tiene un método estándar, independiente del dispositivo, para tener acceso a estas funciones. La única opción es enviar un comando AV/C sin formato al controlador, tal como se describe en el tema [emisión de comandos AV/c sin procesar](issuing-raw-av-c-commands.md).

El controlador UVC admite un conjunto de propiedades para las búsquedas de ubicaciones de cinta. Para enviar un comando de búsqueda, use la interfaz **IKsControl** y establezca la \_ propiedad de transporte ext PROPSETID \_ . El uso de un conjunto de propiedades es más seguro que el envío de comandos AV/C sin formato al dispositivo, ya que los comandos AV/C omiten el filtro y van directamente al controlador de dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de una videocámara DV](controlling-a-dv-camcorder.md)
</dt> <dt>

[Conjunto de propiedades de transporte de dispositivo externo](external-device-transport-property-set.md)
</dt> </dl>

 

 



