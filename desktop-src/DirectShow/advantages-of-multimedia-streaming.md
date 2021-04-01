---
description: Ventajas del streaming multimedia
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Ventajas del streaming multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd907d9b8e91cb61709479a2d600323d6d420958
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157004"
---
# <a name="advantages-of-multimedia-streaming"></a>Ventajas del streaming multimedia

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.

 

Cuando los desarrolladores usan el streaming multimedia en sus aplicaciones, reduce en gran medida la cantidad de programación específica de formato necesaria. Normalmente, una aplicación que debe obtener datos de medios de un origen de archivos o hardware debe saber todo lo relacionado con el formato de datos y el dispositivo de hardware. La aplicación debe controlar la conexión, la transferencia de datos, cualquier conversión de datos necesaria y la representación de datos real o el almacenamiento de archivos. Dado que cada formato y dispositivo son ligeramente diferentes, este proceso suele ser complejo y engorroso. Por otro lado, el streaming multimedia negocia automáticamente la transferencia y la conversión de los datos desde el origen a la aplicación. Las interfaces de streaming proporcionan un método uniforme y predecible de acceso y control de los datos, lo que facilita que una aplicación pueda reproducir los datos, independientemente de su origen o formato original.

En los pasos siguientes se muestra cómo implementar el streaming, desde el dispositivo de hardware hasta la reproducción representada.

1.  Un origen de datos de vídeo, como DirectShow, expone las interfaces de streaming.
2.  El desarrollador de aplicaciones utiliza las interfaces de streaming multimedia para controlar la conversión del formato de datos.
3.  El desarrollador de aplicaciones utiliza las interfaces de DirectDraw para representar los datos resultantes.

La especificación de secuencias multimedia incluye varias interfaces; cada interfaz incluye métodos que controlan un aspecto determinado del proceso de streaming o controlan un determinado tipo de datos. Consulte la [lista de interfaces de streaming multimedia](list-of-multimedia-streaming-interfaces.md) para obtener información adicional.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la arquitectura de streaming multimedia](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



