---
description: En el núcleo de cualquier instalador se encuentra la instalación real de archivos.
ms.assetid: e6f6d6a5-bdb0-4866-8d2c-56313d92c94c
title: Reglas de control de versiones de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8dfda6a909450ba45cc213016a159bbbc8f9a54b958c7d4e37d051fd86935ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828985"
---
# <a name="file-versioning-rules"></a>Reglas de control de versiones de archivos

En el núcleo de cualquier instalador se encuentra la instalación real de archivos. Determinar si se debe instalar un archivo es un proceso complejo. En el nivel más alto, esta determinación depende de si el componente al que pertenece un archivo está marcado para la instalación. Una vez determinado que se debe copiar un archivo, el proceso es complicado si existe otro archivo con el mismo nombre en la carpeta de destino. En tales situaciones, realizar la determinación requiere un conjunto de reglas que implican las siguientes propiedades:

-   Versión
-   Date
-   Lenguaje

El instalador solo usa estas reglas al intentar instalar un archivo en una ubicación que ya contiene un archivo con el mismo nombre. En este caso, el Windows usa las siguientes reglas, todas las demás iguales, para determinar si se debe instalar.

La versión más alta gana: todas las demás cosas son iguales, el archivo con la versión más alta gana, incluso si el archivo del equipo tiene la versión más alta.

Archivos con control de versiones: se instala un archivo con versiones en un archivo sin versiones.

Favorezca el idioma del producto: si el archivo que se está instalando tiene un idioma diferente al del equipo, favorezca el archivo con el idioma que coincida con el producto que se está instalando. Los archivos con idioma neutro se tratan como un idioma más, por lo que el producto que se está instalando se favorece de nuevo.

Varios idiomas no coincidentes: después de tener en cuenta los idiomas comunes entre el archivo que se va a instalar y el archivo en el equipo, los idiomas restantes se favorecen según lo que necesita el producto que se está instalando.

Conservar idiomas de superconjunto: conserve el archivo que admite varios idiomas, independientemente de si ya está en el equipo o si se está instalando.

Los archivos sin versiones son datos de usuario: si la fecha de modificación es posterior a la fecha de creación del archivo en el equipo, no instale el archivo porque se eliminarían las personalizaciones de usuario. Si las fechas Modified y Create son las mismas, instale el archivo. Si la fecha de creación es posterior a la fecha de modificación, el archivo se considera sin modificar, instale el archivo.

La instalación de un [archivo complementario](companion-files.md) no depende de su propia información de control de versiones de archivo, sino del control de versiones de su elemento primario complementario. En el caso de los archivos complementarios, la instalación solo se omite si el archivo primario tiene una versión superior. Tenga en cuenta que un archivo que sea la ruta de acceso de clave para su componente no debe ser un archivo complementario, ya que esto da como resultado que el archivo primario complementario determine la lógica de control de versiones del archivo de ruta de acceso de clave.

Archivos sin versiones [](companion-files.md)mediante archivos complementarios: un archivo sin versiones asociado a un archivo con versiones que usa el mecanismo complementario se rige por las reglas del archivo con versión. La única excepción es si el archivo con control de versiones del equipo y el archivo con versión que se está instalando tienen la misma versión y el mismo idioma, pero falta el archivo complementario en el equipo. En este caso, se usa el archivo complementario que se va a instalar aunque se utilice el archivo con control de versiones en el equipo. Además, se instala un archivo sin versiones que usa un archivo complementario si la propiedad [**REINSTALLMODE**](reinstallmode.md) incluye las opciones de sobrescritura de versiones anteriores ("o" o "e") y la versión del archivo complementario es igual a un archivo que ya está en la máquina.

Reglas globales: las reglas para determinar cuándo instalar un archivo residen en un solo lugar dentro del instalador y son globales, lo que significa que se aplican a todos los archivos por igual.

Para obtener ejemplos del formato usado para las versiones de archivo, consulte el [tipo de datos](version.md) Version. Para obtener información más específica, vea [Reemplazar archivos existentes o](replacing-existing-files.md) Control de versiones de archivo [predeterminado.](default-file-versioning.md)

 

 



