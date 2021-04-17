---
description: La sección de instalación de un archivo INF define los pasos del procedimiento de instalación.
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: Ejemplo de sección de instalación de INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667998"
---
# <a name="inf-install-section-example"></a>Ejemplo de sección de instalación de INF

La **sección de instalación de** un archivo INF define los pasos del procedimiento de instalación. Cada línea de una sección de **instalación** tiene dos partes. A la izquierda del signo igual (=) es la clave. En el lado derecho, es una lista de uno o varios títulos de sección. La clave especifica el tipo de las secciones que se enumeran a la derecha. Para obtener una descripción del formato de esta sección, vea las secciones y directivas del archivo INF del kit de desarrollo de controladores de Microsoft Windows 2000.

El siguiente es un ejemplo de una sección de **instalación** .

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

En este ejemplo, la clave **CopyFiles** se establece en los valores "files" y "ProgramFiles". Esto especifica dos secciones **copiar archivos** en el archivo INF que contienen los nombres de los archivos de origen utilizados por las operaciones de copia. El destino de los archivos copiados se especificaría en una sección **DestinationDirs** del archivo INF.

A la clave **Delfiles** se le asigna el valor "OldFiles". Esto especifica una sección **eliminar archivos** que contiene información pertinente para las operaciones de eliminación de archivos.

La clave **UpdateInis** especifica las secciones **Update ini File** que contienen información sobre la actualización de entradas en el archivo ini.

Las claves **AddReg** y **DelReg** especifican las secciones **Agregar registro** y **Eliminar registro** que contienen información acerca de cómo agregar o eliminar información del registro.

 

 



