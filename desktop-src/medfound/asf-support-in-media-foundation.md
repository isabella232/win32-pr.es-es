---
description: Compatibilidad con ASF en Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Compatibilidad con ASF en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361185"
---
# <a name="asf-support-in-media-foundation"></a>Compatibilidad con ASF en Media Foundation

Media Foundation admite archivos multimedia en el formato de sistemas avanzados (ASF):

-   Windows Vídeo multimedia (archivos WMV)
-   Windows Audio multimedia (archivos WMA)

Media Foundation proporciona varios objetos para leer y escribir archivos ASF. Estos objetos se proporcionan en dos capas de arquitectura diferentes.

En primer lugar, *la capa* de canalización contiene objetos que funcionan dentro de la canalización [Media Foundation y](media-foundation-pipeline.md) se ajustan a las API definidas por la canalización. La capa de canalización de ASF contiene:

-   [Origen multimedia de ASF:](asf-media-source.md)analiza los archivos ASF y entrega los paquetes de datos de audio y vídeo.
-   [Windows códecs multimedia:](windows-media-codecs.md)descodificar o codificar Windows secuencias de audio o vídeo multimedia.
-   [Receptor multimedia de ASF:](asf-media-sinks.md)recibe paquetes de datos y escribe un archivo ASF.

En segundo lugar, la capa de contenedor wm proporciona control de bajo nivel sobre el análisis y la escritura de un archivo ASF. La capa de canalización usa WMContainer internamente. Las aplicaciones también pueden usar WMContainer para análisis y escritura de ASF de bajo nivel.

![diagrama que muestra los elementos de la capa de canalización y el contenedor wm](images/asf-components.png)

## <a name="in-this-section"></a>En esta sección



| Tema                                                                         | Descripción                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Estructura de archivos ASF](asf-file-structure.md)<br/>                       | Información general sobre la estructura de archivos de ASF y los objetos proporcionados por Media Foundation para trabajar con archivos ASF.<br/> |
| [Componentes de ASF de capa de canalización](pipeline-layer-asf-components.md)<br/> | Describe cómo analizar y crear archivos ASF mediante la capa de canalización.<br/>                                   |
| [Componentes de ASF de WMContainer](wmcontainer-asf-components.md)<br/>       | Describe cómo analizar y crear archivos ASF mediante la capa WMContainer.<br/>                                |



 

Para obtener información detallada sobre la estructura de un archivo ASF, consulte la especificación de ASF, que se puede descargar desde este sitio [web de Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation de programación](media-foundation-programming-guide.md)
</dt> </dl>

 

 




