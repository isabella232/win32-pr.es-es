---
description: Representación de dispositivos
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Representación de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497308"
---
# <a name="device-representation"></a>Representación de dispositivos

Los dispositivos tienen dos comportamientos principales que se resuelven mediante la arquitectura de dispositivos portátiles de Windows (WPD):

-   Acceder al contenido y almacenarlo. Por ejemplo, las aplicaciones deben poder agregar archivos de música a un reproductor de música portátil.
-   Programar el dispositivo. Esto incluye operaciones sencillas, como cambiar la configuración y preparar el dispositivo para la captura de datos o operaciones más complejas, como la carga de firmware. Entre los ejemplos se incluye la emisión de un comando "tomar imagen" a una cámara digital.

En WPD, estos comportamientos se describen mediante la representación del dispositivo como una jerarquía de objetos. En la ilustración siguiente se muestra una representación de objeto de WPD para un dispositivo de varias funciones, que en este caso es un teléfono móvil.

![Ilustración en la que se muestra la jerarquía de objetos de un teléfono móvil](images/wpd-overview-figure3.gif)

Esta jerarquía muestra la funcionalidad y el contenido siguientes.

Functional

-   Objeto de almacenamiento. Este dispositivo tiene almacenamiento de datos.
-   Servicio de contactos. Este servicio es un objeto funcional que se puede usar para sincronizar y almacenar contactos en el teléfono.
-   Servicio de SMS. Este servicio es un objeto funcional que se puede usar para enviar, recibir y almacenar mensajes SMS.

Contenido:

-   Objetos multimedia. Este dispositivo almacena imágenes, música y archivos de vídeo en carpetas en el objeto de almacenamiento. Aunque los archivos que se muestran en la ilustración se almacenan en una carpeta, un dispositivo puede subdividir el contenido en carpetas organizadas por el tipo de medios almacenados; por ejemplo, carpetas de imagen, carpetas de música y carpetas de vídeo.
-   Objetos de contacto. Este dispositivo almacena información de contacto (como el nombre, el número de teléfono y la dirección) como elemento secundario del servicio de contactos.
-   Objetos de mensaje. Este dispositivo almacena mensajes SMS como elementos secundarios del servicio SMS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general de la aplicación**](application-overview.md)
</dt> </dl>

 

 



