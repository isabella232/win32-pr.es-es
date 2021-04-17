---
description: Los objetos de archivo funcionan como la interfaz lógica entre los procesos de kernel y de modo de usuario y los datos de archivo que residen en el disco físico.
ms.assetid: 53aabb35-4601-42d1-ac73-385473ff91e2
title: Objetos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e37793ad6c31ac86809047a3ec0d34afc3efc34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666842"
---
# <a name="file-objects"></a>Objetos de archivo

Los *objetos de archivo* funcionan como la interfaz lógica entre los procesos de kernel y de modo de usuario y los datos de archivo que residen en el disco físico. Un objeto de archivo contiene los datos escritos en el archivo y el siguiente conjunto de atributos mantenidos por el kernel.



| Tipo de información                                              | Propósito                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de archivo                                                     | Asigna un nombre al archivo físico correspondiente.                                                                                                                                                          |
| Desplazamiento de bytes actual                                           | Se usa en e/s de archivos sincrónicos (que se describe más adelante en esta sección) para identificar la ubicación de inicio actual de las operaciones de lectura y escritura.                                                          |
| Modo de uso compartido                                                    | Especifica si un segundo proceso puede abrir un archivo para el acceso de lectura, escritura o eliminación mientras el proceso inicial sigue teniendo acceso a él.                                                           |
| Modo de e/s                                                      | Especifica si el proceso inicial abrió el archivo para e/s [sincrónica o asincrónica](synchronous-and-asynchronous-i-o.md), en caché o sin almacenamiento en caché, e/s secuencial o aleatoria, etc. |
| Puntero a objeto de dispositivo                                      | Identifica el dispositivo físico en el que residen los datos del archivo.                                                                                                                                        |
| Puntero al bloque de parámetros de volumen o [ **VPB**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb) | Identifica el volumen o la partición en la que residen los datos del archivo.                                                                                                                                    |
| Puntero a los punteros de objeto de sección                            | Identifica una estructura raíz que describe un [archivo asignado](/windows/desktop/Memory/file-mapping).                                                                                                                  |
| Puntero a asignación de caché privada                                  | Identifica los datos de archivo que están almacenados actualmente en la memoria caché.                                                                                                                                              |



 

Estos atributos se definen como parte de la estructura del [**\_ objeto de archivo**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) en Ntddk. h. Consulte la definición de esta estructura en la documentación del kit de controladores de Windows (WDK) para ver las longitudes de los datos y los tipos de los valores.

 

 
