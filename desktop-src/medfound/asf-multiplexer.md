---
description: Multiplexor de ASF
ms.assetid: 007a6da5-47cf-476a-b0f7-566a68ad19ce
title: Multiplexor de ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e1577f005004dbbe6bbb27e1ce7af346e56e134aff2b3201f5670175b015c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035572"
---
# <a name="asf-multiplexer"></a>Multiplexor de ASF

El *multiplexor* de ASF es un objeto de capa WMContainer que funciona con el objeto de datos [ASF](asf-file-structure.md) y ofrece a una aplicación la capacidad de generar paquetes de datos para un contenedor de ASF. El multiplexor acepta datos multimedia [](media-samples.md) en forma de ejemplos multimedia y genera ejemplos multimedia basados en los parámetros de paquetes de streaming y ASF definidos en el objeto de [encabezado asf](asf-file-structure.md). Los ejemplos de medios de salida contienen referencias a uno o varios búferes multimedia que contienen datos multimedia digitales en paquetes. Puede usar este objeto en un escenario de codificación de archivos en el que recibe muestras de secuencia codificadas del codificador o para la transcodificación de ASF-ASF (reuxing).

En el diagrama siguiente se muestra la generación de paquetes de datos de ASF para un archivo ASF mediante el multiplexor.

![diagrama que muestra la generación de paquetes de datos asf](images/bb2da6a9-5e50-4dea-9b79-ae32759ac48a.gif)

Para obtener información sobre la estructura de un archivo ASF, vea [ASF File Structure](asf-file-structure.md).

Esta sección contiene los siguientes temas:



| Tema                                                                  | Descripción                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Crear el objeto multiplexor](creating-the-multiplexer-object.md) | Cómo crear e inicializar el multiplexor.                     |
| [Generación de nuevos paquetes de datos de ASF](generating-new-asf-data-packets.md) | Cómo generar paquetes de datos para que conste de un nuevo objeto de datos de ASF. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de ASF de WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Tutorial: Copia de asf Secuencias de un archivo a otro](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Tutorial: Escritura de un archivo WMA mediante la codificación CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



