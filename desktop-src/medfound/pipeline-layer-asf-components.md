---
description: En el modelo de canalización de bases de medios, un origen multimedia se conecta a una transformación que se conecta aún más a un receptor de medios.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Componentes ASF de capa de canalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715511"
---
# <a name="pipeline-layer-asf-components"></a>Componentes ASF de capa de canalización

En el modelo de canalización de Media Foundation, un origen multimedia se conecta a una transformación que se conecta aún más a un receptor de medios. Los datos contenidos en el origen fluyen a través de la transformación y generan ejemplos de medios de salida en el receptor con el fin de reproducir o codificar. En función de si la aplicación desea reproducir contenido ASF o codificar en un archivo ASF, la aplicación debe compilar la canalización de forma diferente.

Los temas siguientes contienen información sobre los componentes de la capa de canalización.

-   [Origen de medios ASF](asf-media-source.md)
-   [Codificadores de Windows Media](windows-media-encoders.md)
-   [Receptores de medios ASF](asf-media-sinks.md)

Los tres componentes principales de una canalización ASF para la reproducción son los siguientes:

-   El origen de medios ASF lo proporciona Media Foundation que representa un archivo ASF.
-   Remuestreadores de audio, cambiar el tamaño de las imágenes de vídeo, etc., (transformación)
-   Representador de audio y vídeo (receptores)

Para obtener información sobre la creación de una canalización de reproducción, vea [crear topologías de reproducción](creating-playback-topologies.md).

Los tres componentes principales de una canalización ASF para la codificación son los siguientes:

-   Origen multimedia que representa los datos en un formato que debe convertirse. Este componente puede ser uno de los orígenes de medios predeterminados proporcionados por Media Foundation o un origen personalizado que exponga la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .
-   Codificadores de Windows Media (transformación) que realizan la conversión de formato.
-   Receptores de medios ASF proporcionados por Media Foundation que escriben objetos ASF y ejemplos de medios en un archivo de salida especificado por la aplicación.

La canalización se representa en una topología y cada objeto de la canalización se representa mediante un nodo de topología. Tanto para la reproducción como para la codificación, la sesión multimedia controla todas las operaciones de canalización. Una de las responsabilidades de la sesión multimedia es asegurarse de que la canalización tenga todos los componentes necesarios para generar la salida. Por ejemplo, en una canalización de codificación, si el formato de origen de audio es diferente del formato de destino, la sesión multimedia inserta componentes de transformación adicionales, como el remuestreador que realiza las conversiones de velocidad de muestra apropiadas. La sesión multimedia también administra el control de flujo de datos a través de la canalización. En un escenario de reproducción, al iniciar la sesión multimedia, la sesión multimedia envía muestras a SAR y EVR, que las representa en el dispositivo de salida. Para la codificación, el inicio de la sesión multimedia inicia el proceso de codificación. La sesión notifica de forma asincrónica a la aplicación cuando se completa la codificación.

El siguiente tema contiene instrucciones paso a paso sobre el uso de los componentes de la capa de canalización para crear una topología de codificación. componentes para leer y escribir archivos ASF.

-   [Tutorial: 1-pasar la codificación de Windows Media](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



