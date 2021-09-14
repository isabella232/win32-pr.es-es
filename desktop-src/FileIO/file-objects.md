---
description: Los objetos de archivo funcionan como la interfaz lógica entre los procesos de kernel y modo de usuario y los datos de archivo que residen en el disco físico.
ms.assetid: 53aabb35-4601-42d1-ac73-385473ff91e2
title: Objetos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e37793ad6c31ac86809047a3ec0d34afc3efc34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069951"
---
# <a name="file-objects"></a>Objetos de archivo

*Los objetos de* archivo funcionan como la interfaz lógica entre los procesos de kernel y modo de usuario y los datos de archivo que residen en el disco físico. Un objeto de archivo contiene los datos escritos en el archivo y el siguiente conjunto de atributos mantenidos por kernel.



| Tipo de información                                              | Propósito                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de archivo                                                     | Denomina el archivo físico correspondiente.                                                                                                                                                          |
| Desplazamiento de bytes actual                                           | Se usa en E/S de archivos sincrónicas (descrita más adelante en esta sección) para identificar la ubicación inicial actual de las operaciones de lectura y escritura.                                                          |
| Modo de recurso compartido                                                    | Especifica si un segundo proceso puede abrir un archivo para el acceso de lectura, escritura o eliminación mientras el proceso inicial sigue accediendo a él.                                                           |
| Modo de E/S                                                      | Especifica si el proceso inicial abrió el archivo para E/S sincrónicas o asincrónicas, [E/S](synchronous-and-asynchronous-i-o.md)almacenadas en caché o sin almacenar en caché, E/S secuenciales o aleatorias, y así sucesivamente. |
| Puntero al objeto de dispositivo                                      | Identifica el dispositivo físico en el que residen los datos del archivo.                                                                                                                                        |
| Puntero al bloque de parámetros de volumen o [ **VPB**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb) | Identifica el volumen o la partición en la que residen los datos del archivo.                                                                                                                                    |
| Puntero a punteros de objeto de sección                            | Identifica una estructura raíz que describe un [archivo asignado.](/windows/desktop/Memory/file-mapping)                                                                                                                  |
| Puntero al mapa de caché privada                                  | Identifica los datos de archivo almacenados actualmente en caché.                                                                                                                                              |



 

Estos atributos se definen como parte de la estructura [**FILE \_ OBJECT**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) en Ntddk.h. Consulte la definición de esta estructura en la documentación de Windows Driver Kit (WDK) para ver las longitudes de datos y los tipos de los valores.

 

 
