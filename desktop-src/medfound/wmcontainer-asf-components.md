---
description: Los objetos WMContainer proporcionan control de bajo nivel sobre el análisis y la escritura de un archivo de formato de sistemas avanzados (ASF).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Componentes de ASF de WMContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363595"
---
# <a name="wmcontainer-asf-components"></a>Componentes de ASF de WMContainer

Los objetos WMContainer proporcionan control de bajo nivel sobre el análisis y la escritura de un archivo de formato de sistemas avanzados (ASF).

Los [componentes de ASF de](pipeline-layer-asf-components.md) la capa de canalización usan internamente los objetos WMContainer. La mayoría de las aplicaciones deben usar los componentes de canalización, en lugar de usar objetos WMContainer. Use WMContainer solo si necesita un control de bajo nivel sobre el análisis y la escritura de un archivo ASF.

La capa WMContainer incluye los siguientes objetos:

-   [Perfil de ASF](asf-profile.md)
-   [Objeto ContentInfo de ASF](asf-contentinfo-object.md)
-   [Divisor de ASF](asf-splitter.md)
-   [Multiplexor de ASF](asf-multiplexer.md)
-   [Indexador de ASF](asf-index-object.md)

Los temas siguientes contienen instrucciones paso a paso sobre el uso de WMContainer para leer o escribir archivos ASF.

-   [Tutorial: Lectura de un archivo ASF mediante objetos WMContainer](tutorial--reading-an-asf-file.md)
-   [Tutorial: Copia de asf Secuencias mediante objetos WMContainer](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [Tutorial: Escritura de un archivo WMA mediante objetos WMContainer](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a>Acerca del contenedor wm

Los objetos WMContainer interactúan directamente con objetos de archivo ASF. En el diagrama siguiente se muestra la estructura de archivos ASF y los objetos WMContainer correspondientes.

![diagrama que muestra la estructura de archivos asf y los objetos de media foundation correspondientes](images/asf-components01.png)

Excepto el divisor y el multiplexor, cada uno de estos objetos admite el análisis (lectura) y la escritura de archivos ASF. El divisor solo se usa para leer archivos ASF. El multiplexor solo se usa para crear nuevos archivos ASF.

Todas las operaciones realizadas por objetos WMContainer son sincrónicas, lo que significa que bloquean el subproceso que realiza la llamada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



