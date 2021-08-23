---
description: Ventajas del streaming multimedia
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Ventajas del streaming multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06df23ce833462aee9b7d4b3840c1fae2d4f3b15c4ee6daee2e4a421259493a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537545"
---
# <a name="advantages-of-multimedia-streaming"></a>Ventajas del streaming multimedia

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow de filtro.

 

Cuando los desarrolladores usan streaming multimedia en sus aplicaciones, reduce considerablemente la cantidad de programación específica del formato necesaria. Normalmente, una aplicación que debe obtener datos multimedia de un archivo o origen de hardware debe conocer todo sobre el formato de datos y el dispositivo de hardware. La aplicación debe controlar la conexión, la transferencia de datos, cualquier conversión de datos necesaria y la representación de datos real o el almacenamiento de archivos. Dado que cada formato y dispositivo es ligeramente diferente, este proceso suele ser complejo y complicado. Por otro lado, el streaming multimedia negocia automáticamente la transferencia y conversión de datos del origen a la aplicación. Las interfaces de streaming proporcionan un método uniforme y predecible de acceso y control de datos, lo que facilita a una aplicación la reproducción de los datos, independientemente de su origen o formato original.

En los pasos siguientes se muestra cómo implementar el streaming, desde el dispositivo de hardware hasta la reproducción representada.

1.  Un origen de datos de vídeo, como DirectShow, expone las interfaces de streaming.
2.  El desarrollador de aplicaciones usa las interfaces de streaming multimedia para controlar la conversión de formato de datos.
3.  El desarrollador de aplicaciones usa las interfaces de DirectDraw para representar los datos resultantes.

La especificación de los flujos multimedia consta de varias interfaces; cada interfaz incluye métodos que controlan un determinado aspecto del proceso de streaming o controlan un determinado tipo de datos. Consulte [Lista de interfaces de streaming multimedia](list-of-multimedia-streaming-interfaces.md) para obtener información adicional.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la arquitectura de streaming multimedia](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



