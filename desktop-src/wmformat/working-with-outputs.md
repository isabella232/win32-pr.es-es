---
title: Trabajar con salidas
description: Trabajar con salidas
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows SDK de formato multimedia, trabajar con salidas
- Formato de sistemas avanzados (ASF), trabajar con salidas
- ASF (formato de sistemas avanzados), trabajar con salidas
- Formato de sistemas avanzados (ASF), números de salida y formatos
- ASF (formato de sistemas avanzados), números de salida y formatos
- números y formatos de salida, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247172"
---
# <a name="working-with-outputs"></a>Trabajar con salidas

De forma predeterminada, cada ejemplo que recibe de cualquier objeto de lector está asociado a un número de salida. Cada número de salida corresponde a una secuencia en el archivo ASF. El lector asigna números de salida a las secuencias del archivo cuando se abre el archivo. Normalmente, hay una salida para cada secuencia de un archivo. Sin embargo, si el archivo usa la exclusión mutua, a cada grupo de flujos mutuamente excluyentes se le asigna un único número de salida. La secuencia que corresponde al número de salida de las secuencias mutuamente excluyentes viene determinada por el lector, en el caso de varios archivos de velocidad de bits (MBR) o por la aplicación, si usa la selección manual de secuencias.

Dado que el nombre de conexión establecido en el perfil no se conserva en el archivo, el lector crea un nombre de conexión predeterminado para cada salida que es simplemente una representación de cadena del número de salida, por ejemplo, "1", "2", "3", y así sucesivamente. Los nombres de conexión permiten a las aplicaciones y al propio lector correlacionar las salidas con secuencias. En un archivo de velocidad de bits múltiple, varias secuencias comparten un nombre de conexión. Esto no importa para el lector, ya que las propiedades de salida de cada secuencia mbr son idénticas.

Cada salida tiene uno o varios formatos de salida admitidos. Un formato de salida es el formato que usan los ejemplos sin comprimir entregados por el lector. Cuando el lector abre un archivo, establece el formato de cada salida en el valor predeterminado para el subtipo de medio. El número y el tipo de formatos de salida admitidos viene determinado por el códec que descomprime los datos multimedia.

En los temas siguientes se explica cómo trabajar con salidas:

-   [Para identificar números de salida](to-identify-output-numbers.md)
-   [Asignar formatos de salida](assigning-output-formats.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMReader (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMSyncReader (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




