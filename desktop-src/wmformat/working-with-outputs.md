---
title: Trabajar con salidas
description: Trabajar con salidas
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- SDK de Windows Media Format, trabajar con salidas
- Advanced Systems Format (ASF), trabajar con salidas
- ASF (formato de sistemas avanzados), trabajar con salidas
- Formato de sistemas avanzados (ASF), números y formatos de salida
- ASF (formato de sistemas avanzados), números y formatos de salida
- números y formatos de salida, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788733"
---
# <a name="working-with-outputs"></a>Trabajar con salidas

De forma predeterminada, cada ejemplo que recibe de cualquier objeto de lector está asociado a un número de salida. Cada número de salida corresponde a una secuencia del archivo ASF. El lector asigna los números de salida a las secuencias del archivo cuando se abre el archivo. Normalmente, hay una salida para cada flujo en un archivo. Sin embargo, si el archivo usa la exclusión mutua, se asigna un único número de salida a cada grupo de flujos mutuamente excluyentes. La secuencia que se corresponde con el número de salida de las secuencias mutuamente excluyente viene determinada por el lector, en el caso de varios archivos de velocidad de bits (MBR) o por la aplicación, si se usa la selección de flujo manual.

Dado que el nombre de conexión establecido en el perfil no se conserva en el archivo, el lector crea un nombre de conexión predeterminado para cada salida que es simplemente una representación de cadena del número de salida, por ejemplo, "1", "2", "3", etc. Los nombres de conexión permiten a las aplicaciones y al propio lector correlacionar las salidas con las secuencias. En un archivo de velocidad de bits múltiple, varios flujos comparten un nombre de conexión. Esto no importa al lector, porque las propiedades de salida de cada flujo MBR son idénticas.

Cada salida tiene uno o más formatos de salida admitidos. Un formato de salida es el formato que usan los ejemplos sin comprimir proporcionados por el lector. Cuando el lector abre un archivo, establece el formato de cada salida en el valor predeterminado para el subtipo de medio. El número y el tipo de formatos de salida admitidos viene determinado por el códec que descomprime los datos multimedia.

En los temas siguientes se explica cómo trabajar con resultados:

-   [Para identificar los números de salida](to-identify-output-numbers.md)
-   [Asignar formatos de salida](assigning-output-formats.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interfaz IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Leer archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




