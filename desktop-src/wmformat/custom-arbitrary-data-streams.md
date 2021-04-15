---
title: Flujos de datos arbitrarios personalizados
description: Flujos de datos arbitrarios personalizados
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- SDK de Windows Media Format, flujos de datos arbitrarios personalizados
- Advanced Systems Format (ASF), flujos de datos arbitrarios personalizados
- ASF (formato de sistemas avanzados), flujos de datos arbitrarios personalizados
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- flujos de datos arbitrarios personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714255"
---
# <a name="custom-arbitrary-data-streams"></a>Flujos de datos arbitrarios personalizados

Puede crear una secuencia en un archivo ASF para que contenga cualquier tipo de datos. Si ninguno de los tipos de secuencia admitidos se adapta a sus necesidades, debe usar un flujo de datos arbitrario. El objeto de escritor controla un flujo de datos arbitrario tal como hace cualquier flujo sin comprimir; los ejemplos se agrupan y se combinan con los ejemplos de otras secuencias en la sección de datos del archivo. Por supuesto, solo una aplicación de lectura que se ha programado específicamente para tratar con su tipo arbitrario podrá controlar los datos después de que los entregue el objeto de lectura.

Un uso común de los flujos de datos arbitrarios es para los datos multimedia codificados con un códec de terceros. Dado que los objetos de este SDK no interactúan directamente con códecs de terceros, la aplicación de escritura debe procesar los ejemplos con la parte de codificación del códec y pasar los ejemplos comprimidos al escritor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Flujos arbitrarios**](arbitrary-streams.md)
</dt> <dt>

[**Configuración de secuencias arbitrarias personalizadas**](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




