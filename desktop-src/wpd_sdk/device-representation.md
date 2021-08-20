---
description: Representación del dispositivo
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Representación del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a96b1144d1ae05ea08e036b4e6732c4e3ed46104628a67e7c83c8579919cecfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117652856"
---
# <a name="device-representation"></a>Representación del dispositivo

Los dispositivos tienen dos comportamientos principales que aborda la arquitectura Windows dispositivos portátiles (WPD):

-   Acceso y almacenamiento de contenido. Por ejemplo, las aplicaciones deben poder agregar archivos de música a un reproductor de música portátil.
-   Programar el dispositivo. Esto incluye operaciones sencillas, como cambiar la configuración y preparar el dispositivo para la captura de datos, o operaciones más complejas, como la carga de firmware. Algunos ejemplos son la emisión de un comando "Tomar imagen" a una cámara digital.

En WPD, estos comportamientos se describen mediante la representación del dispositivo como una jerarquía de objetos. En la ilustración siguiente se muestra una representación de objeto WPD para un dispositivo de varias funciones, que en este caso es un teléfono móvil.

![ilustración que muestra la jerarquía de objetos para un teléfono móvil](images/wpd-overview-figure3.gif)

Esta jerarquía muestra la siguiente funcionalidad y contenido.

Funcionalidad:

-   Storage objeto . Este dispositivo tiene almacenamiento de datos.
-   Servicio de contactos. Este servicio es un objeto funcional que se puede usar para sincronizar y almacenar contactos en el teléfono.
-   Servicio SMS. Este servicio es un objeto funcional que se puede usar para enviar, recibir y almacenar mensajes SMS.

Contenido:

-   Objetos multimedia. Este dispositivo almacena imágenes, música y archivos de vídeo en carpetas en Storage objeto. Aunque los archivos que se muestran en la ilustración se almacenan en una carpeta, un dispositivo puede subdividir el contenido en carpetas organizadas por el tipo de medio almacenado. por ejemplo, carpetas de imágenes, carpetas de música y carpetas de vídeo.
-   Objetos de contacto. Este dispositivo almacena información de contacto (como el nombre, el número de teléfono y la dirección) como secundarios del servicio de contactos.
-   Objetos de mensaje. Este dispositivo almacena mensajes SMS como secundarios del servicio SMS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción a la aplicación**](application-overview.md)
</dt> </dl>

 

 



