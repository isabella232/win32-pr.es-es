---
description: En el modelo de canalización de Media Foundations, un origen multimedia está conectado a una transformación que está conectada aún más a un receptor multimedia.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Componentes de ASF de capa de canalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580249"
---
# <a name="pipeline-layer-asf-components"></a>Componentes de ASF de capa de canalización

En Media Foundation de canalización de , un origen multimedia está conectado a una transformación que se conecta aún más a un receptor de medios. Los datos contenidos en el origen fluyen a través de la transformación y generan muestras de medios de salida en el receptor con el fin de reproducir o codificar. Dependiendo de si la aplicación desea reproducir contenido de ASF o codificar en un archivo ASF, la aplicación debe compilar la canalización de forma diferente.

Los temas siguientes contienen información sobre los componentes de la capa de canalización.

-   [Origen de medios de ASF](asf-media-source.md)
-   [Windows Codificadores multimedia](windows-media-encoders.md)
-   [Receptores de medios de ASF](asf-media-sinks.md)

Los tres componentes principales de una canalización de ASF para la reproducción son los siguientes:

-   El origen de medios de ASF lo proporciona Media Foundation que representa un archivo ASF.
-   Muestreos de audio, cambiadores de tamaño de imágenes de vídeo, etc., (transformación)
-   Representador de audio y vídeo (receptores)

Para obtener información sobre cómo crear una canalización de reproducción, vea [Crear topologías de reproducción.](creating-playback-topologies.md)

Los tres componentes principales de una canalización de ASF para la codificación son los siguientes:

-   Origen de medios que representa los datos en un formato que debe convertirse. Este componente puede ser uno de los orígenes multimedia predeterminados proporcionados por Media Foundation o un origen personalizado que expone la [**interfaz IMFMediaSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   Windows Codificadores multimedia (transformación) que realizan la conversión de formato.
-   Receptores de medios DE ASF proporcionados por Media Foundation que escriben objetos ASF y ejemplos de medios en un archivo de salida especificado por la aplicación.

La canalización se representa en una topología y cada objeto de la canalización se representa mediante un nodo de topología. Tanto para la reproducción como para la codificación, la sesión multimedia controla todas las operaciones de canalización. Una de las responsabilidades de la sesión multimedia es asegurarse de que la canalización tiene todos los componentes necesarios para generar la salida. Por ejemplo, en una canalización de codificación, si el formato de origen de audio es diferente del formato de destino, la sesión multimedia inserta componentes de transformación adicionales, como el resampler que realiza las conversiones de frecuencia de muestreo adecuadas. El control de flujo de datos a través de la canalización también se administra mediante la sesión multimedia. En un escenario de reproducción, al iniciar la sesión multimedia, la sesión multimedia envía ejemplos a SAR y EVR, que los representa en el dispositivo de salida. Para la codificación, al iniciar la sesión multimedia se inicia el proceso de codificación. La sesión notifica de forma asincrónica a la aplicación cuando se completa la codificación.

El tema siguiente contiene instrucciones paso a paso sobre el uso de los componentes de la capa de canalización para crear una topología de codificación. componentes para leer y escribir archivos ASF.

-   [Tutorial: Codificación de medios Windows paso 1](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



