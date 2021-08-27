---
description: En la tabla siguiente se identifican los límites de tamaño de los distintos elementos del Registro.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Límites de tamaño de elemento del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76a11abc80f80a13e0643d7745d211168ecba8bcf06446af9ac842f8351567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885238"
---
# <a name="registry-element-size-limits"></a>Límites de tamaño de elemento del Registro

En la tabla siguiente se identifican los límites de tamaño de los distintos elementos del Registro.



| Elemento Registry | Límite de tamaño                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de clave         | 255 caracteres. El nombre de clave incluye la ruta de acceso absoluta de la clave en el Registro, empezando siempre en una clave base, por ejemplo, HKEY \_ LOCAL \_ MACHINE. |
| Nombre del valor       | 16 383 **caracteres Windows 2000:** 260 caracteres ANSI o 16 383 caracteres Unicode.<br/>                                                       |
| Valor            | Memoria disponible (formato más reciente)1 MB (formato estándar)<br/>                                                                                     |
| Árbol             | Un árbol del Registro puede tener 512 niveles de profundidad. Puede crear hasta 32 niveles a la vez a través de una única llamada API del registro.                                  |



 

Los valores largos (más de 2048 bytes) deben almacenarse en un archivo y la ubicación del archivo debe almacenarse en el Registro. Esto ayuda a que el registro se realice de forma eficaz.

La ubicación del archivo puede ser el nombre de un valor o los datos de un valor. Cada barra diagonal inversa de la cadena de ubicación debe ir precedida de otra barra diagonal inversa como carácter de escape. Por ejemplo, especifique "C: mydir myfile" para almacenar \\ \\ la cadena \\ \\ "C: \\ mydir \\ myfile". Una ubicación de archivo también puede ser el nombre de una clave si está dentro del límite de 255 caracteres para los nombres de clave y no contiene barras diagonales inversas, que no se permiten en los nombres de clave.

 

 




