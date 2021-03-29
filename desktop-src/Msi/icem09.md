---
description: ICEM09 comprueba que el módulo de mezcla controla los directorios predefinidos de forma segura.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4b4d2d52c35d6dd3670daff5150a785e19d0b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277748"
---
# <a name="icem09"></a>ICEM09

ICEM09 comprueba que el módulo de mezcla controla los directorios predefinidos de forma segura. Para ello, comprueba que ningún componente del módulo instala un directorio en un directorio del sistema predefinido como "ProgramFilesFolder" o "StartMenuFolder". En su lugar, los módulos deben usar directorios con nombres únicos (creados con la Convención de nomenclatura del módulo de combinación) y usar acciones personalizadas para el directorio de destino adecuado. Este enfoque impide que los módulos entren en conflicto con una estructura de directorios existente en la base de datos final. ICEM09 comprueba que las acciones personalizadas necesarias para que funcione esta técnica no existan (para que la herramienta de combinación pueda generarlas) o que existan en el formato correcto (de modo que funcionen según lo esperado).

Si no se corrige una advertencia o un error informados por ICEM09, podrían producirse problemas en los clientes del módulo de combinación. Las filas de la tabla de directorio con claves principales como ProgramFilesFolder suelen existir en una base de datos; por lo tanto, si los componentes del módulo se instalan directamente en directorios predefinidos como ProgramFilesFolder, las entradas de directorio del módulo pueden entrar en conflicto con las filas ya existentes. Esta condición requeriría que el usuario del módulo dividira los archivos de origen del módulo para que coincidan con el directorio de origen existente.

## <a name="result"></a>Resultado

ICEM09 informa de un error o una advertencia cuando un componente de módulo instala un directorio en un directorio del sistema predefinido, lo que provoca un conflicto de nombres con la estructura de directorios existente.

## <a name="example"></a>Ejemplo

ICEM09 envía las siguientes advertencias para un módulo que contiene las entradas de base de datos que se muestran.

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

Cambie el nombre del directorio del módulo de combinación para que no coincida con una propiedad de Windows Installer y, por tanto, sea único. A continuación, establezca una propiedad con el mismo nombre en el valor del directorio Windows Installer. Cuando tiene lugar la resolución del directorio, el directorio tiene una propiedad con el mismo nombre, por lo que la ubicación de instalación del directorio es el valor de la propiedad. Los archivos se mueven de la ubicación de origen distinta a la misma ubicación de destino. Este proceso debe quitar por completo los conflictos de combinación.

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

Si la acción no tiene el número de secuencia 1, es posible que no se mezcle en la base de datos de destino lo suficientemente pronto en la secuencia para que funcione de forma eficaz.

Para corregir esta advertencia, establezca el número de secuencia en 1. Tenga en cuenta que la mayoría de las herramientas de combinación más recientes (pero no algunas versiones anteriores) generarán estas acciones personalizadas en el momento de la combinación, por lo que no siempre es necesario crear explícitamente las acciones en el módulo de combinación.

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

Dado que la columna CustomAction es la clave principal de la tabla CustomAction, algunas herramientas de combinación pueden generar acciones duplicadas porque el nombre de la acción previamente creada es diferente.

Para corregir esta advertencia, asigne a la acción el mismo nombre que el directorio de destino. Tenga en cuenta que la mayoría de las herramientas de combinación más recientes (pero no algunas versiones anteriores) generan estas acciones personalizadas en el momento de la combinación, por lo que no siempre es necesario crear explícitamente las acciones en el módulo de combinación.

[Tabla de directorio](directory-table.md)



| Directorio          | Directorio \_ primario | DefaultDir |
|--------------------|-------------------|------------|
| ProgramFilesFolder | Directory1        | A          |
| StartMenuFolder    | Directory2        | B:C        |
| AppDataFolder      | Directory3        | D          |
| MyPicturesFolder   | Directory4        | E          |



 

[Tabla de componentes](component-table.md)



| Componente               | Directorio          |
|-------------------------|--------------------|
| Component1.<GUID> | ProgramFilesFolder |
| Component2.<GUID> | StartMenuFolder    |
| Component3.<GUID> | AppDataFolder      |
| Component4.<GUID> | MyPicturesFolder   |



 

[Tabla CustomAction](customaction-table.md)



| CustomAction                 | Tipo | Source                       | Destino              |
|------------------------------|------|------------------------------|---------------------|
| StartMenuFolder.<GUID> | 51   | StartMenuFolder.<GUID> | \[StartMenuFolder\] |
| MyAppDataFolderAction        | 51   | AppDataFolder.<GUID>   | \[AppDataFolder\]   |



 

[Tabla ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Acción                       | Secuencia | BaseAction | Después | Condición |
|------------------------------|----------|------------|-------|-----------|
| StartMenuFolder.<GUID> | 100      |            |       |           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de módulo de combinación ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



