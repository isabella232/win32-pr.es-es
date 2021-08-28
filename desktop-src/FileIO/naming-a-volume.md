---
description: Una etiqueta es un nombre descriptivo que se asigna a un volumen, normalmente por un usuario final, para facilitar el reconocimiento. Un volumen puede tener una etiqueta, una letra de unidad, ambas o ninguna. Para establecer la etiqueta de un volumen, use la función SetVolumeLabel.
ms.assetid: f640f42d-a703-4e2e-a6d3-09cbe989cd11
title: Asignación de nombres a un volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc0af7575f2fd6ad2f45fc5763666151c08e10f414e1b6e6610e163c4c811cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119533364"
---
# <a name="naming-a-volume"></a>Asignación de nombres a un volumen

Una etiqueta es un nombre descriptivo que se asigna a un volumen, normalmente por un usuario final, para facilitar el reconocimiento. Un volumen puede tener una etiqueta, una letra de unidad, ambas o ninguna. Para establecer la etiqueta de un volumen, use la [**función SetVolumeLabel.**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela)

Varios factores pueden dificultar la identificación de volúmenes específicos mediante solo letras de unidad y etiquetas. Una es que no es necesario que un volumen tenga una letra de unidad o una etiqueta. Otra es que dos volúmenes diferentes pueden tener la misma etiqueta, lo que los hace indistinguibles excepto por letra de unidad. Un tercer factor es que las asignaciones de letras de unidad pueden cambiar a medida que los volúmenes se agregan y quitan del equipo.

Para solucionar este problema, el sistema operativo usa rutas *de acceso GUID de volumen* para identificar volúmenes. Estas son cadenas de este formato:

"\\\\?\\ Volume{*GUID*} \\ "

donde *GUID* es un identificador único global (GUID) que identifica el volumen.

A veces se hace referencia *a* una ruta de acceso GUID de volumen como un nombre de volumen único, porque una ruta de acceso GUID de volumen solo puede hacer referencia a un volumen. Sin embargo, este término es engañoso, ya que un volumen puede tener más de una ruta de acceso GUID de volumen.

El prefijo " ? " deshabilita el análisis de rutas de acceso y no se considera \\ \\ parte de la ruta \\ de acceso. Para obtener más información sobre el prefijo " \\ \\ ? \\ ", vea [Asignar nombres a un archivo o directorio.](naming-a-file.md)

Debe especificar rutas de acceso completas al usar rutas de acceso GUID de volumen con el prefijo " \\ \\ ? \\ ".

Una *carpeta montada es una* asociación entre una carpeta de un volumen y otro volumen, por lo que se puede usar la ruta de acceso de la carpeta para acceder al volumen. Por ejemplo, si usa la función [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para crear una carpeta montada que asocie el volumen "D: " con la carpeta "C: MountD", puede usar cualquier ruta de acceso \\ \\ ("D: " o \\ "C: MountD") para acceder al volumen \\ \\ \\ "D: \\ ".

Un *punto de montaje de* volumen es cualquier ruta de acceso de modo de usuario que se puede usar para acceder a un volumen. Hay tres tipos de puntos de montaje de volumen:

-   Una letra de unidad, por ejemplo, "C: \\ ".
-   Una ruta de acceso GUID de volumen, por ejemplo, " \\ \\ ? \\ Volume{26a21bda-a627-11d7-9931-806e6f6e6963} \\ ".
-   Una carpeta montada, por ejemplo, "C: \\ \\ Montado".

Todas las funciones de volumen y carpeta montada que toman una ruta de acceso GUID de volumen como parámetro de entrada requieren la barra diagonal inversa final. Todas las funciones de volumen y carpeta montada que devuelven una ruta de acceso GUID de volumen proporcionan la barra diagonal inversa final, pero este no es el caso de la [**función CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Para abrir un volumen, llame a **CreateFile** y omita la barra diagonal inversa final del nombre del volumen que especifique. **CreateFile** procesa una ruta de acceso GUID de volumen con una barra diagonal inversa anexada como directorio raíz del volumen.

El sistema operativo asigna una ruta de acceso GUID de volumen a un volumen cuando el volumen se instala por primera vez y cuando se formatee el volumen. Las funciones de volumen y carpeta montada usan rutas de acceso GUID de volumen para acceder a los volúmenes. Para obtener la ruta de acceso GUID del volumen para un volumen, use la [**función GetVolumeNameForVolumeMountPoint.**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)

Las longitudes de ruta de acceso pueden ser un problema cuando se crea una carpeta montada que asocia un volumen que tiene un árbol de directorio profundo con un directorio de otro volumen. Esto se debe a que la ruta de acceso del volumen se concatena con la ruta de acceso del directorio. La constante definida globalmente **MAX \_ PATH** define el número máximo de caracteres que puede tener una ruta de acceso. (Para obtener más información sobre **MAX \_ PATH**, vea [Asignar nombres a un archivo o directorio).](naming-a-file.md) Puede evitar esta restricción realizando una de las siguientes acciones:

-   Consulte los volúmenes por sus rutas de acceso GUID de volumen.
-   Use las versiones Unicode (W) de las funciones de archivo, que admiten el \\ \\ prefijo ? \\ .

 

 



