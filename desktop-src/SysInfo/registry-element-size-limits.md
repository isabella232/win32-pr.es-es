---
description: En la tabla siguiente se identifican los límites de tamaño de los distintos elementos del registro.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Límites de tamaño de elementos del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 262609a64e60536dcfc41f29e5d94ea499158861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667594"
---
# <a name="registry-element-size-limits"></a>Límites de tamaño de elementos del registro

En la tabla siguiente se identifican los límites de tamaño de los distintos elementos del registro.



| Elemento Registry | Límite de tamaño                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de clave         | 255 caracteres. El nombre de clave incluye la ruta de acceso absoluta de la clave en el registro, que siempre comienza en una clave base, por ejemplo, HKEY \_ local \_ Machine. |
| Nombre del valor       | 16.383 caracteres **Windows 2000:** 260 caracteres ANSI o 16.383 caracteres Unicode.<br/>                                                       |
| Value            | Memoria disponible (formato más reciente) 1 MB (formato estándar)<br/>                                                                                     |
| Árbol             | Un árbol del registro puede tener un nivel de 512 niveles de profundidad. Puede crear hasta 32 niveles a la vez a través de una única llamada API del registro.                                  |



 

Los valores largos (más de 2.048 bytes) deben almacenarse en un archivo y la ubicación del archivo debe estar almacenada en el registro. Esto ayuda a que el registro funcione de forma eficaz.

La ubicación del archivo puede ser el nombre de un valor o los datos de un valor. Cada barra diagonal inversa de la cadena de ubicación debe ir precedida de otra barra diagonal inversa como carácter de escape. Por ejemplo, especifique "C: \\ \\ myDir mi \\ \\ archivo" para almacenar la cadena "c: \\ myDir \\ . Una ubicación de archivo también puede ser el nombre de una clave si está dentro del límite de 255 caracteres para los nombres de clave y no contiene barras diagonales inversas, que no se permiten en los nombres de clave.

 

 




