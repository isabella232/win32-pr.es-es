---
title: Introducción al SDK Windows Media Format
description: Introducción al SDK Windows Media Format
ms.assetid: 9e5d6254-6261-4ca8-84d6-38050c93db22
keywords:
- Windows SDK de formato multimedia, creación y edición de archivos ASF
- Formato de sistemas avanzados (ASF), creación y edición de archivos
- ASF (formato de sistemas avanzados), creación y edición de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4f58be5d377e44fc0f68c89ad580a554902c58
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360930"
---
# <a name="overview-of-the-windows-media-format-sdk"></a>Introducción al SDK Windows Media Format

El SDK Windows Media Format contiene objetos para realizar tareas en tres puntos de la vida de un archivo ASF: creación, edición y reproducción. Algunas aplicaciones, especialmente las de edición de vídeo, usarán la amplia funcionalidad del SDK de formato multimedia de Windows para leer el contenido de los archivos ASF, modificar ese contenido y escribir los resultados en un archivo nuevo. Sin embargo, es más fácil pensar en este SDK en las tres fases de creación, edición y reproducción de archivos.

## <a name="asf-file-creation-with-the-windows-media-format-sdk"></a>Creación de archivos ASF con el SDK Windows Media Format

El proceso de escritura de archivos ASF con Windows SDK de formato multimedia es, en un nivel alto, bastante sencillo. La creación de archivos se administra mediante un objeto de escritor. Para indicar al objeto de escritor qué tipo de archivo desea crear, especifique un objeto de perfil para que lo use. Cada objeto de perfil contiene la configuración de un archivo ASF. Algunos perfiles se incluyen con este SDK y la compatibilidad con la edición de perfiles la proporcionan varios objetos. Cuando haya establecido un perfil para el objeto de escritor que se va a usar, puede empezar a pasar ejemplos al escritor para su procesamiento. En la mayoría de los casos, un ejemplo es un fragmento de audio o vídeo sin comprimir, pero una muestra puede ser cualquier tipo de datos.

Internamente, el escritor realiza tres tareas principales. En primer lugar, si la secuencia a la que pertenece una muestra se va a comprimir, el escritor se comunica con la parte de codificación del códec (descomprimidor o descomprimidor) para comprimir la muestra. Una vez que los ejemplos tienen el formato especificado por el perfil, el escritor divide las muestras en paquetes de tamaño adecuado para transmitirlos a través de una red. Por último, los datos de las distintas secuencias se multiplexa o se intercalan para que las muestras con tiempos de presentación similares en todos los flujos estén cerca unas de otras en la sección de datos del archivo ASF.

El objeto de escritor no escribe realmente un archivo en sí. Se comunica con uno o varios objetos denominados receptores, que entregan los datos del escritor a su destino. En el caso de los archivos locales, un receptor de archivos administra la escritura de los datos en el archivo. También puede configurar receptores de red para entregar los datos de ASF a través de una red. Normalmente, se usa más de un receptor. Por ejemplo, una aplicación puede transmitir un archivo a través de una red y guardar una copia como un archivo en un disco local simultáneamente. Mediante el uso de un receptor de inserción, puede difundir contenido desde la aplicación de escritura a uno o varios servidores que ejecutan Servicios de Windows Media, que distribuirá el contenido a los usuarios.

## <a name="asf-file-editing-with-the-windows-media-format-sdk-metadata-editing"></a>Edición de archivos ASF con el SDK Windows media format (edición de metadatos)

La edición del contenido de la sección de datos de un archivo ASF implica volver a escribir el archivo. El SDK Windows media format no proporciona ningún objeto que manipule la sección de datos en su lugar. Para realizar modificaciones sencillas, como concatenar dos archivos o cortar contenido de un archivo, puede leer ejemplos sin descomprimirlos y, a continuación, escribirlos en un archivo nuevo con la misma información de encabezado. Las modificaciones más complicadas implican realizar cambios en el perfil usado para el nuevo archivo.

El SDK Windows Media Format admite la edición de partes de la sección de encabezado sin volver a escribir el archivo. El encabezado de un archivo ASF contiene muchos tipos diferentes de datos. Los más editados son los atributos de metadatos, que son pares nombre-valor que describen aspectos del contenido y las personas implicadas en su elaboración. Puede editar metadatos mediante el objeto editor de metadatos del SDK Windows Media Format. Este objeto abrirá un archivo ASF, le permitirá cambiar parte del contenido del encabezado, escribir los cambios en el archivo y cerrar el archivo. La edición de metadatos es muy sencilla, con llamadas a métodos simples para recuperar y establecer valores.

## <a name="asf-file-reading-with-the-windows-media-format-sdk"></a>Lectura de archivos ASF con el SDK Windows Media Format

El SDK Windows media format proporciona dos objetos distintos para leer archivos ASF: el objeto reader y el objeto de lector sincrónico. El objeto lector está disponible en todas las versiones del SDK, mientras que el objeto de lector sincrónico requiere el SDK de la serie Windows Media Format 9 o una versión posterior. La diferencia principal entre los dos es que el objeto reader entrega ejemplos a la aplicación mediante la activación de eventos en un método de devolución de llamada, mientras que el lector sincrónico proporciona ejemplos individuales en respuesta a llamadas de método.

Para usar el objeto reader, debe implementar varios métodos de devolución de llamada para reaccionar ante el estado y los mensajes de ejemplo del objeto reader. Configure el lector para que entregue el contenido como quiera, inicie el lector y espere los mensajes de ejemplo. El proceso de recuperación de ejemplos de un archivo ASF es básicamente el inverso del proceso de escritura. El objeto lector se comunica con los códecs necesarios para descodificar los flujos comprimidos y entrega datos sin comprimir a la aplicación. También puede configurar el objeto de lector para entregar ejemplos en su estado comprimido, de modo que pueda incluir una secuencia codificada previamente en un nuevo archivo.

El objeto de lector sincrónico funciona de la misma manera que el objeto de lector. Pero en lugar de configurar las devoluciones de llamada, debe solicitar cada ejemplo del lector sincrónico individualmente. El uso del lector sincrónico requiere solo un subproceso, mientras que el uso del lector requiere varios subprocesos. El objeto de lector sincrónico tiene varias ventajas con respecto al objeto de lector en determinadas circunstancias, principalmente para las aplicaciones de edición de contenido que necesitan acceder rápidamente a diferentes partes de un archivo y copiar datos entre archivos. El objeto de lector sincrónico es mucho más sencillo de usar y facilita la búsqueda en lugares específicos de la sección de datos. Sin embargo, el lector sincrónico no admite la lectura de archivos a través de una red y no admite la administración de derechos digitales.

## <a name="other-operations-with-the-windows-media-format-sdk"></a>Otras operaciones con el SDK Windows Media Format

Además de las tres áreas funcionales principales que se han descrito, el SDK Windows Media Format tiene objetos para realizar otras operaciones relacionadas con los archivos ASF. El objeto del administrador de perfiles se usa para crear perfiles y acceder a ellos y guardarlos. El objeto indexador crea objetos de índice en archivos ASF que permiten la búsqueda en archivos de vídeo. Por último, el objeto lector y el objeto de escritor admiten la administración de derechos digitales para proteger los derechos intelectuales de los creadores de contenido.

**Nota** La intención de la estructura de archivos de ASF y de este SDK en general es generar archivos multimedia digitales que contengan audio y vídeo, y esta documentación se escribe con ese fin en mente. Sin embargo, la estructura de archivos asf también funcionará para otros tipos de contenido. Puede encontrar muchas aplicaciones para archivos ASF que no están relacionadas con audio y vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




