---
description: Los objetos WMContainer proporcionan un control de bajo nivel sobre el análisis y la escritura de un archivo de formato de sistema avanzado (ASF).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Componentes de WMContainer ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002099"
---
# <a name="wmcontainer-asf-components"></a>Componentes de WMContainer ASF

Los objetos WMContainer proporcionan un control de bajo nivel sobre el análisis y la escritura de un archivo de formato de sistema avanzado (ASF).

Los [componentes ASF de capa de canalización](pipeline-layer-asf-components.md) usan los objetos WMContainer internamente. La mayoría de las aplicaciones deben usar los componentes de canalización, en lugar de usar objetos WMContainer. Use WMContainer solo si necesita un control de bajo nivel sobre el análisis y la escritura de un archivo ASF.

El nivel WMContainer incluye los siguientes objetos:

-   [Perfil ASF](asf-profile.md)
-   [Objeto ContentInfo de ASF](asf-contentinfo-object.md)
-   [Divisor ASF](asf-splitter.md)
-   [Multiplexor ASF](asf-multiplexer.md)
-   [Indexador ASF](asf-index-object.md)

Los temas siguientes contienen instrucciones paso a paso sobre el uso de WMContainer para leer o escribir archivos ASF.

-   [Tutorial: lectura de un archivo ASF mediante objetos WMContainer](tutorial--reading-an-asf-file.md)
-   [Tutorial: copiar secuencias ASF mediante objetos WMContainer](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [Tutorial: escribir un archivo WMA con objetos WMContainer](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a>Acerca del contenedor de WM

Los objetos WMContainer interactúan directamente con los objetos de archivo ASF. En el diagrama siguiente se muestra la estructura de archivos ASF y los objetos WMContainer correspondientes.

![diagrama que muestra la estructura de archivos ASF y los objetos de Media Foundation correspondientes](images/asf-components01.png)

A excepción del divisor y multiplexador, cada uno de estos objetos admite tanto el análisis (lectura) como la escritura de archivos ASF. El divisor solo se utiliza para leer archivos ASF. El multiplexor solo se usa para crear nuevos archivos ASF.

Todas las operaciones realizadas por objetos WMContainer son sincrónicas, lo que significa que bloquean el subproceso que realiza la llamada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



