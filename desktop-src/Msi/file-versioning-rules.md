---
description: En el núcleo de cualquier instalador se encuentra la instalación real de los archivos.
ms.assetid: e6f6d6a5-bdb0-4866-8d2c-56313d92c94c
title: Reglas de control de versiones de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c6f8e59b4f15774f898217690dbb1c4d57b1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687184"
---
# <a name="file-versioning-rules"></a>Reglas de control de versiones de archivo

En el núcleo de cualquier instalador se encuentra la instalación real de los archivos. Determinar si se debe instalar un archivo es un proceso complejo. En el nivel más alto, esta determinación depende de si el componente al que pertenece un archivo está marcado para su instalación. Una vez que haya determinado que se debe copiar un archivo, el proceso es complicado si existe otro archivo con el mismo nombre en la carpeta de destino. En estas situaciones, la realización de la determinación requiere un conjunto de reglas que impliquen las siguientes propiedades:

-   Versión
-   Fecha
-   Idioma

El instalador solo utiliza estas reglas al intentar instalar un archivo en una ubicación que ya contiene un archivo con el mismo nombre. En este caso, el Windows Installer usa las siguientes reglas, todas las demás cosas son iguales, para determinar si se debe instalar.

La versión más alta gana, es decir, el archivo con la versión más alta gana, aunque el archivo del equipo tenga la versión más alta.

Archivos con versiones Win: un archivo con versiones se instala en un archivo que no tiene versiones.

Favorecer el idioma del producto: Si el archivo que se está instalando tiene un idioma diferente al del archivo en el equipo, favorece el archivo con el idioma que coincida con el producto que se va a instalar. Los archivos independientes del idioma se tratan como un solo otro idioma, por lo que el producto que se está instalando se vuelve a favorecer.

Varios idiomas no coincidentes: después de factorizar los idiomas comunes entre el archivo que se está instalando y el archivo en el equipo, se favorece el resto de idiomas según lo que necesite el producto que se está instalando.

Conservar idiomas de superconjunto: conserva el archivo que admite varios idiomas, independientemente de si ya está en el equipo o se está instalando.

Los archivos sin versión son datos de usuario: Si la fecha modificada es posterior a la fecha de creación del archivo en el equipo, no instale el archivo porque se eliminarán las personalizaciones de usuario. Si las fechas de creación y modificación son las mismas, instale el archivo. Si la fecha de creación es posterior a la fecha de modificación, el archivo se considera no modificado, instálelo.

La instalación de un [archivo complementario](companion-files.md) no depende de su propia información de versión del archivo, sino de la versión de su complemento principal. En el caso de los archivos complementarios, la instalación se omite solo si el archivo primario tiene una versión superior. Tenga en cuenta que un archivo que es la ruta de acceso de la clave de su componente no debe ser un archivo complementario porque esto da como resultado la lógica de control de versiones del archivo de ruta de acceso de la clave que está determinando el archivo principal complementario.

Archivos sin control de versiones con [archivos complementarios](companion-files.md): un archivo sin versión que está asociado a un archivo con versión que usa el mecanismo complementario se atiene a las reglas del archivo con versión. La única excepción es que el archivo con versión del equipo y el archivo con versión que se está instalando tienen la misma versión y el mismo idioma, pero el archivo complementario falta en el equipo. En este caso, se usa el archivo complementario que se está instalando aunque se use el archivo con versión del equipo. Además, se instala un archivo sin versión mediante un archivo complementario si la propiedad [**REINSTALLMODE**](reinstallmode.md) incluye las opciones sobrescribir versiones anteriores ("o" o "e") y la versión del archivo complementario es igual a un archivo que ya está en el equipo.

Las reglas son globales: las reglas para determinar cuándo instalar un archivo residen en un solo lugar dentro del instalador y son globales, lo que significa que se aplican a todos los archivos de forma equitativa.

Para obtener ejemplos del formato utilizado para las versiones de archivo, vea el tipo de datos [version](version.md) . Para obtener información más específica, vea [reemplazar archivos existentes](replacing-existing-files.md) o [versiones de archivo predeterminadas](default-file-versioning.md).

 

 



