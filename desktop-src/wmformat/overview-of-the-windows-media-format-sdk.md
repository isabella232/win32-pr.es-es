---
title: Información general sobre el SDK de Windows Media Format
description: Información general sobre el SDK de Windows Media Format
ms.assetid: 9e5d6254-6261-4ca8-84d6-38050c93db22
keywords:
- SDK de Windows Media Format, creación y edición de archivos ASF
- Advanced Systems Format (ASF), creación y edición de archivos
- ASF (formato de sistemas avanzados), creación y edición de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4f58be5d377e44fc0f68c89ad580a554902c58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356788"
---
# <a name="overview-of-the-windows-media-format-sdk"></a>Información general sobre el SDK de Windows Media Format

El SDK de Windows Media Format contiene objetos para realizar tareas en tres puntos en la vida de un archivo ASF: creación, edición y reproducción. Algunas aplicaciones, especialmente las de edición de vídeo, utilizarán la amplia funcionalidad del SDK de Windows Media Format para leer el contenido de los archivos ASF, modificar el contenido y escribir los resultados en un archivo nuevo. Sin embargo, es más fácil pensar en este SDK en las tres fases de creación, edición y reproducción de archivos.

## <a name="asf-file-creation-with-the-windows-media-format-sdk"></a>Creación de archivos ASF con el SDK de Windows Media Format

El proceso de escritura de archivos ASF con el SDK de Windows Media Format es, de un nivel muy sencillo,. La creación de archivos es administrada por un objeto de escritura. Para indicar al objeto de escritura qué tipo de archivo desea crear, especifique un objeto de perfil para su uso. Cada objeto de perfil contiene la configuración de un archivo ASF. Algunos perfiles se incluyen en este SDK y la compatibilidad con la edición de perfiles se proporciona mediante una serie de objetos. Cuando haya establecido un perfil para que lo use el objeto de escritor, puede comenzar a pasar ejemplos al escritor para su procesamiento. En la mayoría de los casos, un ejemplo es un fragmento de audio o vídeo sin comprimir, pero un ejemplo puede ser cualquier tipo de datos.

Internamente, el escritor realiza tres tareas principales. En primer lugar, si se va a comprimir la secuencia a la que pertenece una muestra, el escritor se comunica con la parte de la codificación del códec (compresor/descompresor) para comprimir el ejemplo. Una vez que los ejemplos se encuentran en el formato especificado por el perfil, el escritor divide los ejemplos en paquetes de tamaño adecuado para transmitirlos a través de una red. Por último, los datos de las diversas secuencias se multiplexan, o intercalan, de modo que los ejemplos con tiempos de presentación similares en todas las secuencias están cerca unos de otros en la sección de datos del archivo ASF.

En realidad, el objeto de escritor no escribe un archivo en sí. Se comunica con uno o más objetos denominados receptores, que entregan los datos del escritor a su destino. En el caso de los archivos locales, un receptor de archivos administra la escritura de los datos en el archivo. También puede configurar receptores de red para proporcionar los datos ASF a través de una red. Normalmente, se usa más de un receptor. Por ejemplo, una aplicación puede transmitir un archivo a través de una red y guardar una copia como un archivo en un disco local simultáneamente. Mediante el uso de un receptor de envío, puede difundir contenido desde la aplicación de escritura a uno o varios servidores que ejecuten Windows Media Services, que distribuirá el contenido a los usuarios.

## <a name="asf-file-editing-with-the-windows-media-format-sdk-metadata-editing"></a>Edición de archivos ASF con el SDK de Windows Media Format (edición de metadatos)

La edición del contenido de la sección de datos de un archivo ASF implica volver a escribir el archivo. El SDK de Windows Media Format no proporciona ningún objeto que manipule la sección de datos en su lugar. En el caso de las ediciones simples, como la concatenación de dos archivos o la reducción de contenido desde un archivo, puede leer ejemplos sin descomprimirlos y, a continuación, escribirlos en un archivo nuevo con la misma información de encabezado. Las modificaciones más complicadas implican realizar cambios en el perfil que se usa para el nuevo archivo.

El SDK de Windows Media Format admite la edición de partes de la sección de encabezado sin tener que volver a escribir el archivo. El encabezado de un archivo ASF contiene muchos tipos diferentes de datos. Normalmente, los atributos de metadatos se editan, que son pares de nombre y valor que describen aspectos del contenido y las personas implicadas en su realización. Puede editar los metadatos mediante el objeto editor de metadatos del SDK de Windows Media Format. Este objeto abrirá un archivo ASF, le permitirá cambiar parte del contenido del encabezado, escribir los cambios en el archivo y cerrar el archivo. La edición de metadatos es muy sencilla, con llamadas a métodos simples para recuperar y establecer valores.

## <a name="asf-file-reading-with-the-windows-media-format-sdk"></a>Lectura de archivos ASF con el SDK de Windows Media Format

El SDK de Windows Media Format proporciona dos objetos distintos para leer archivos ASF: el objeto lector y el objeto lector sincrónico. El objeto lector está disponible en todas las versiones del SDK, mientras que el objeto lector sincrónico requiere el SDK de Windows Media Format 9 series o una versión posterior. La principal diferencia entre los dos es que el objeto de lector proporciona ejemplos a la aplicación mediante la activación de eventos en un método de devolución de llamada, mientras que el lector sincrónico proporciona ejemplos individuales en respuesta a llamadas a métodos.

Para usar el objeto lector, debe implementar varios métodos de devolución de llamada para reaccionar ante los mensajes de ejemplo y de estado del objeto lector. Configure el lector para que entregue el contenido como desee, inicie el lector y espere a que se muestren los mensajes de ejemplo. El proceso de recuperación de muestras de un archivo ASF es básicamente el inverso del proceso de escritura. El objeto de lector se comunica con los códecs necesarios para descodificar cualquier flujo comprimido y entrega datos sin comprimir a la aplicación. También puede configurar el objeto lector para proporcionar ejemplos en su estado comprimido, de modo que pueda incluir una secuencia codificada previamente en un archivo nuevo.

El objeto de lector sincrónico funciona prácticamente de la misma manera que el objeto de lector. Pero en lugar de configurar las devoluciones de llamada, debe solicitar cada ejemplo del lector sincrónico individualmente. El uso del lector sincrónico solo requiere un único subproceso, mientras que el uso del lector requiere varios subprocesos. El objeto lector sincrónico tiene varias ventajas sobre el objeto lector en determinadas circunstancias, principalmente para las aplicaciones de edición de contenido que necesitan tener acceso rápidamente a diferentes partes de un archivo y copiar datos entre archivos. El objeto de lector sincrónico es mucho más sencillo de usar y facilita la búsqueda de lugares específicos en la sección de datos. Sin embargo, el lector sincrónico no admite la lectura de archivos a través de una red y no admite la administración de derechos digitales.

## <a name="other-operations-with-the-windows-media-format-sdk"></a>Otras operaciones con el SDK de Windows Media Format

Además de las tres áreas funcionales principales que se acaban de describir, el SDK de Windows Media Format tiene objetos para realizar otras operaciones relacionadas con los archivos ASF. El objeto de administrador de perfiles se usa para crear y obtener acceso a los perfiles y guardarlos. El objeto de indexador crea objetos de índice en archivos ASF que permiten la búsqueda en archivos de vídeo. Por último, el objeto lector y el objeto escritor admiten la administración de derechos digitales para proteger los derechos intelectuales de los creadores de contenido.

**Nota:** La intención de la estructura de archivos ASF y este SDK en general es generar archivos multimedia digitales que contienen audio y vídeo, y esta documentación se escribe teniendo en cuenta este fin. Sin embargo, la estructura de archivos ASF también funcionará para otros tipos de contenido. Puede encontrar muchas aplicaciones para archivos ASF que no están relacionadas con audio y vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK de Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




