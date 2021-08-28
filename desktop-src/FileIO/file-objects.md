---
description: Los objetos de archivo funcionan como la interfaz lógica entre los procesos de kernel y modo de usuario y los datos de archivo que residen en el disco físico.
ms.assetid: 53aabb35-4601-42d1-ac73-385473ff91e2
title: Objetos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263eae282f76195cc125848f13f43f5ee3d8f676cc6328b2d03db443e6f1deec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107475"
---
# <a name="file-objects"></a>Objetos de archivo

*Los objetos de* archivo funcionan como la interfaz lógica entre los procesos de kernel y modo de usuario y los datos de archivo que residen en el disco físico. Un objeto de archivo contiene los datos escritos en el archivo y el siguiente conjunto de atributos mantenidos por kernel.



| Tipo de información                                              | Propósito                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de archivo                                                     | Denomina el archivo físico correspondiente.                                                                                                                                                          |
| Desplazamiento de bytes actual                                           | Se usa en la E/S de archivos sincrónica (descrita más adelante en esta sección) para identificar la ubicación inicial actual de las operaciones de lectura y escritura.                                                          |
| Modo de recurso compartido                                                    | Especifica si un segundo proceso puede abrir un archivo para el acceso de lectura, escritura o eliminación mientras el proceso inicial sigue accediendo a él.                                                           |
| Modo de E/S                                                      | Especifica si el proceso inicial abrió el archivo para E/S sincrónica o asincrónica, [E/S](synchronous-and-asynchronous-i-o.md)almacenada en caché o sin almacenar en caché, E/S secuencial o aleatoria, y así sucesivamente. |
| Puntero al objeto de dispositivo                                      | Identifica el dispositivo físico en el que residen los datos de archivo.                                                                                                                                        |
| Puntero al bloque de parámetros de volumen o [ **VPB**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_vpb) | Identifica el volumen o partición en el que residen los datos del archivo.                                                                                                                                    |
| Puntero a punteros de objeto de sección                            | Identifica una estructura raíz que describe un [archivo asignado.](/windows/desktop/Memory/file-mapping)                                                                                                                  |
| Puntero al mapa de caché privada                                  | Identifica los datos de archivo que se almacenan actualmente en caché.                                                                                                                                              |



 

Estos atributos se definen como parte de la estructura [**FILE \_ OBJECT**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_file_object) en Ntddk.h. Consulte la definición de esta estructura en la documentación de Windows Driver Kit (WDK) para obtener información sobre las longitudes de datos y los tipos de los valores.

 

 
