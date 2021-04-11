---
description: Multiplexor ASF
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: Multiplexor ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362a1e0be72e8bc516e37ec83c36446177816f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080335"
---
# <a name="asf-multiplexer"></a>Multiplexor ASF

El *multiplexor* de ASF es un objeto de capa WMContainer que funciona con el [objeto de datos ASF](asf-file-structure.md) y proporciona a una aplicación la capacidad de generar paquetes de datos para un contenedor ASF. El multiplexor acepta los datos multimedia en forma de [muestras de medios](media-samples.md) y genera ejemplos de medios basados en los parámetros de paquetes ASF y de transmisión por secuencias definidos en el [objeto de encabezado ASF](asf-file-structure.md). Los ejemplos de medios de salida contienen referencias a uno o varios búferes multimedia que contienen datos de medios digitales con paquetes. Puede usar este objeto en un escenario de codificación de archivos en el que reciba ejemplos de secuencias codificadas del codificador o para la transcodificación ASF-ASF (remuxing).

En el diagrama siguiente se ilustra la generación de paquetes de datos ASF para un archivo ASF mediante el multiplexor.

![diagrama que muestra la generación de paquetes de datos ASF](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

Para obtener información acerca de la estructura de un archivo ASF, consulte [ASF File Structure](asf-file-structure.md).

Esta sección contiene los siguientes temas:



| Tema                                                                  | Descripción                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Crear el objeto multiplexor](creating-the-multiplexer-object.md) | Cómo crear e inicializar el multiplexor.                     |
| [Generación de nuevos paquetes de datos ASF](generating-new-asf-data-packets.md) | Cómo generar paquetes de datos para constituir un nuevo objeto de datos ASF. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de WMContainer ASF](wmcontainer-asf-components.md)
</dt> <dt>

[Tutorial: copiar secuencias ASF de un archivo a otro](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Tutorial: escribir un archivo WMA con codificación CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



