---
description: Una etiqueta es un nombre descriptivo que se asigna a un volumen, normalmente por un usuario final, para que sea más fácil de reconocer. Un volumen puede tener una etiqueta, una letra de unidad, ambas o ninguna de ellas. Para establecer la etiqueta de un volumen, utilice la función SetVolumeLabel.
ms.assetid: f640f42d-a703-4e2e-a6d3-09cbe989cd11
title: Asignar un nombre a un volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6435b6b5c7283cf2fb9a98951698f79646dfdffa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911933"
---
# <a name="naming-a-volume"></a>Asignar un nombre a un volumen

Una etiqueta es un nombre descriptivo que se asigna a un volumen, normalmente por un usuario final, para que sea más fácil de reconocer. Un volumen puede tener una etiqueta, una letra de unidad, ambas o ninguna de ellas. Para establecer la etiqueta de un volumen, utilice la función [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .

Varios factores pueden dificultar la identificación de volúmenes específicos con solo Letras de unidad y etiquetas. Uno es que no es necesario que un volumen tenga una letra de unidad o una etiqueta. Otro es que dos volúmenes diferentes pueden tener la misma etiqueta, lo que los hace indistinguibles excepto por la letra de unidad. Un tercer factor es que las asignaciones de Letras de unidad pueden cambiar a medida que los volúmenes se agregan al equipo y se quitan del mismo.

Para solucionar este problema, el sistema operativo usa *rutas* de acceso de GUID de volumen para identificar volúmenes. Estas son cadenas de este tipo:

"\\\\?\\ Volumen {*GUID*} \\ "

donde *GUID* es un identificador único global (GUID) que identifica el volumen.

A veces, se hace referencia a una ruta de acceso de GUID de volumen como un *nombre de volumen único*, porque una ruta de acceso de GUID de volumen solo puede hacer referencia a un volumen. Sin embargo, este término es engañoso, porque un volumen puede tener más de una ruta de acceso de GUID de volumen.

El \\ \\ \\ prefijo "?" deshabilita el análisis de rutas de acceso y no se considera parte de la ruta de acceso. Para obtener más información sobre el \\ \\ \\ prefijo "?", vea [asignar un nombre a un archivo o un directorio](naming-a-file.md).

Debe especificar rutas de acceso completas al usar las rutas de acceso de GUID de volumen con el \\ \\ \\ prefijo "?".

Una *carpeta montada* es una asociación entre una carpeta de un volumen y otro volumen, por lo que se puede usar la ruta de acceso de la carpeta para tener acceso al volumen. Por ejemplo, si usa la función [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para crear una carpeta montada que asocia el volumen "d: \\ " con la carpeta "c: \\ mounted \\ ", puede utilizar cualquiera de las rutas de acceso ("d: \\ " o "c: \\ mountd \\ ") para acceder al volumen "D: \\ ".

Un *punto de montaje de volumen* es cualquier ruta de acceso de modo de usuario que se pueda usar para tener acceso a un volumen. Hay tres tipos de puntos de montaje de volumen:

-   Una letra de unidad, por ejemplo, "C: \\ ".
-   Una ruta de acceso de GUID de volumen, por ejemplo, " \\ \\ ? \\ Volumen {26a21bda-a627-11d7-9931-806e6f6e6963} \\ ".
-   Una carpeta montada, por ejemplo, "C: \\ mounted \\ ".

Todas las funciones de volumen y de carpeta montada que toman una ruta de acceso de GUID de volumen como parámetro de entrada requieren la barra diagonal inversa final. Todas las funciones de volumen y de carpeta montada que devuelven una ruta de acceso de GUID de volumen proporcionan la barra diagonal inversa final, pero no es el caso de la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Para abrir un volumen, puede llamar a **CreateFile** y omitir la barra diagonal inversa final del nombre de volumen que especifique. **CreateFile** procesa una ruta de acceso de GUID de volumen con una barra diagonal inversa anexada como el directorio raíz del volumen.

El sistema operativo asigna una ruta de acceso de GUID de volumen a un volumen cuando el volumen se instala por primera vez y cuando se da formato al volumen. Las funciones de volumen y de carpeta montada usan rutas de acceso de GUID de volumen para acceder a los volúmenes. Para obtener la ruta de acceso de GUID de volumen de un volumen, utilice la función [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .

Las longitudes de ruta de acceso pueden ser un problema cuando se crea una carpeta montada que asocia un volumen que tiene un árbol de directorios profundo con un directorio en otro volumen. Esto se debe a que la ruta de acceso del volumen se concatena con la ruta de acceso del directorio. La **\_ ruta de acceso máxima** constante definida globalmente define el número máximo de caracteres que puede tener una ruta de acceso. (Para obtener más información sobre la **\_ ruta de acceso máxima**, vea [asignar un nombre a un archivo o un directorio](naming-a-file.md)). Para evitar esta restricción, realice una de las acciones siguientes:

-   Consulte los volúmenes por sus rutas de acceso de GUID de volumen.
-   Use las versiones Unicode (W) de las funciones de archivo, que admiten el \\ \\ \\ prefijo?.

 

 



