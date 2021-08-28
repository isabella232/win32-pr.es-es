---
description: ICEM09 comprueba que el módulo de combinación controla de forma segura los directorios predefinidos.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30542ead9a47ab5e92074227b1ae47fa6de0e643
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887394"
---
# <a name="icem09"></a>ICEM09

ICEM09 comprueba que el módulo de combinación controla de forma segura los directorios predefinidos. Para ello, comprueba que ningún componente del módulo instala un directorio en un directorio del sistema predefinido, como "ProgramFilesFolder" o "StartMenuFolder". En su lugar, los módulos deben usar directorios con nombres únicos (creados con la convención de nomenclatura del módulo de mezcla) y usar acciones personalizadas para dirigirse al directorio de destino adecuado. Este enfoque evita que los módulos entren en conflicto con una estructura de directorios existente en la base de datos final. ICEM09 comprueba que las acciones personalizadas necesarias para que esta técnica funcione no existen (para que la herramienta de combinación pueda generarlas) o existen en el formato correcto (para que funcionen según lo previsto).

Si no se corrige una advertencia o un error notificado por ICEM09, podrían producirse problemas para los clientes del módulo de combinación. Las filas de la tabla de directorios con claves principales, como ProgramFilesFolder, suelen existir en una base de datos; Por lo tanto, si los componentes del módulo se instalan directamente en directorios predefinidos, como ProgramFilesFolder, las entradas de directorio del módulo pueden colisionar con las filas ya existentes. Esta condición requeriría que el usuario del módulo divida los archivos de origen del módulo para que coincidan con el directorio de origen existente.

## <a name="result"></a>Resultado

ICEM09 notifica un error o una advertencia cuando un componente de módulo instala un directorio en un directorio del sistema predefinido, lo que provoca un posible conflicto de nombres con la estructura de directorios existente.

## <a name="example"></a>Ejemplo

ICEM09 publica las siguientes advertencias para un módulo que contiene las entradas de base de datos mostradas.

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

Cambie el nombre del directorio del módulo de mezcla para que no coincida con una Windows installer y, por tanto, sea única. A continuación, establezca una propiedad del mismo nombre en el valor del directorio Windows Installer. Cuando se produce la resolución de directorios, el directorio tiene una propiedad del mismo nombre, por lo que la ubicación de instalación del directorio es el valor de la propiedad . Los archivos se mueven de la ubicación de origen distinta a la misma ubicación de destino. Este proceso debe quitar completamente los conflictos de combinación.

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

Si la acción no tiene el número de secuencia 1, es posible que no se combine en la base de datos de destino lo suficientemente pronto como para que funcione de forma eficaz.

Para corregir esta advertencia, establezca el número de secuencia en 1. Tenga en cuenta que la mayoría de las herramientas de combinación actuales (pero no algunas versiones anteriores) generarán estas acciones personalizadas en el momento de la combinación, por lo que no siempre es necesario crear explícitamente las acciones en el módulo de combinación.

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

Dado que la columna CustomAction es la clave principal de la tabla CustomAction, algunas herramientas de combinación pueden generar acciones duplicadas porque el nombre de acción previamente escrito es diferente.

Para corregir esta advertencia, asigne a la acción el mismo nombre que el directorio de destino. Tenga en cuenta que la mayoría de las herramientas de combinación actuales (pero no algunas versiones anteriores) generan estas acciones personalizadas en el momento de la combinación, por lo que no siempre es necesario crear explícitamente las acciones en el módulo de combinación.

[Tabla de directorios](directory-table.md)



| Directorio          | Elemento primario \_ del directorio | DefaultDir |
|--------------------|-------------------|------------|
| ProgramFilesFolder | Directory1        | A          |
| StartMenuFolder    | Directory2        | B:C        |
| AppDataFolder      | Directory3        | D          |
| MyPicturesFolder   | Directory4        | E          |



 

[Tabla de componentes](component-table.md)



| Componente               | Directorio          |
|-------------------------|--------------------|
| Component1. &lt; GUID&gt; | ProgramFilesFolder |
| Componente 2. &lt; GUID&gt; | StartMenuFolder    |
| Componente 3. &lt; GUID&gt; | AppDataFolder      |
| Componente 4. &lt; GUID&gt; | MyPicturesFolder   |



 

[Tabla CustomAction](customaction-table.md)



| CustomAction                 | Tipo | Source                       | Destino              |
|------------------------------|------|------------------------------|---------------------|
| StartMenuFolder. &lt; GUID&gt; | 51   | StartMenuFolder. &lt; GUID&gt; | \[StartMenuFolder\] |
| MyAppDataFolderAction        | 51   | AppDataFolder. &lt; GUID&gt;   | \[AppDataFolder\]   |



 

[ModuleInstallExecuteSequence (tabla)](moduleinstallexecutesequence-table.md)



| Acción                       | Secuencia | BaseAction | Después | Condición |
|------------------------------|----------|------------|-------|-----------|
| StartMenuFolder. &lt; GUID&gt; | 100      |            |       |           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



