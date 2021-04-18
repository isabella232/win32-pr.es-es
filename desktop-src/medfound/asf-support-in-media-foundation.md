---
description: Compatibilidad con ASF en Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Compatibilidad con ASF en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707549"
---
# <a name="asf-support-in-media-foundation"></a>Compatibilidad con ASF en Media Foundation

Media Foundation admite archivos multimedia en el formato de sistemas avanzados (ASF):

-   Windows Media Video (archivos WMV)
-   Windows Media Audio (archivos WMA)

Media Foundation proporciona varios objetos para leer y escribir archivos ASF. Estos objetos se proporcionan en dos capas arquitectónicas diferentes.

En primer lugar, la capa de *canalización* contiene objetos que funcionan dentro de la [canalización Media Foundation](media-foundation-pipeline.md) y que se ajustan a las API definidas por la canalización. La capa de canalización ASF contiene:

-   [Origen de medios ASF](asf-media-source.md): analiza los archivos ASF y entrega los paquetes de datos de audio y vídeo.
-   [Códecs de Windows Media](windows-media-codecs.md): descodificar o codificar secuencias de audio o vídeo de Windows Media.
-   [Receptor de medios ASF](asf-media-sinks.md): recibe paquetes de datos y escribe un archivo ASF.

En segundo lugar, la capa de contenedor de WM proporciona un control de bajo nivel sobre el análisis y la escritura de un archivo ASF. La capa de canalización usa WMContainer internamente. Las aplicaciones también pueden usar WMContainer para el análisis y la escritura de ASF de bajo nivel.

![diagrama que muestra los elementos de la capa de canalización y el contenedor de WM](images/asf-components.png)

## <a name="in-this-section"></a>En esta sección



| Tema                                                                         | Descripción                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Estructura de archivos ASF](asf-file-structure.md)<br/>                       | Información general de la estructura de archivos ASF y los objetos proporcionados por Media Foundation para trabajar con archivos ASF.<br/> |
| [Componentes ASF de capa de canalización](pipeline-layer-asf-components.md)<br/> | Describe cómo analizar y crear archivos ASF con la capa de canalización.<br/>                                   |
| [Componentes de WMContainer ASF](wmcontainer-asf-components.md)<br/>       | Describe cómo analizar y crear archivos ASF con el nivel WMContainer.<br/>                                |



 

Para obtener información detallada acerca de la estructura de un archivo ASF, consulte la especificación ASF, que se puede descargar desde este [sitio web de Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




