---
description: Orca.exe es un editor de tablas de base de datos para crear y editar Windows Installer paquetes y módulos de combinación.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f17874e08fcdbfdbab38c480219579897b9896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082064"
---
# <a name="orcaexe"></a>Orca.exe

Orca.exe es un editor de tablas de base de datos para crear y editar Windows Installer paquetes y módulos de combinación. La herramienta proporciona una interfaz gráfica para la validación, resaltando las entradas concretas en las que se producen errores o advertencias de validación.

Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Se proporciona como un archivo de Orca.msi. Después de instalar los componentes de Windows SDK para Windows Installer desarrolladores, haga doble clic en Orca.msi para instalar el archivo de Orca.exe.

## <a name="syntax"></a>Sintaxis

**Orca***\[<options>\]\[<source file>\]*

## <a name="command-line-options"></a>Opciones de la línea de comandos

Orca.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión.



| Opción | Descripción                                                 |
|--------|-------------------------------------------------------------|
| -q     | Modo silencioso                                                  |
| -S     | < base \[ de datos de esquema de> de bases de datos "orca. dat": predeterminado\] |
| -?     | Cuadro de diálogo de ayuda                                                 |



 

Orca.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas con los módulos de combinación. También se puede usar un delimitador de barra diagonal en lugar de un guión. Al realizar una combinación, se necesitan los>-f,-m y <*SourceFile* .



| Opción     | Descripción                                                                |
|------------|----------------------------------------------------------------------------|
| -c         | Confirme la combinación en la base de datos si no hay errores.                                     |
| -!         | Confirme la fusión mediante combinación en una base de datos, incluso si hay errores.                       |
| -M         | <*módulo*> módulo de combinación que se va a combinar en la base de datos.                      |
| -f         | Característica \[ : característica2 \] características para conectarse al módulo de combinación.                |
| -r         | <*identificador de directorio*> entrada de directorio para la redirección raíz del módulo.    |
| -X         | <*directorio*> extraer archivos en una imagen en el directorio.         |
| -g         | <*lenguaje> lenguaje* usado para abrir un módulo.                         |
| -l         | <archivo de *registro*> archivo que se va a usar como registro; Anexe si ya existe.      |
| -i         | <*directorio*> Extraiga los archivos a la imagen de origen en el directorio. |
| -CAB       | <*nombre* de archivo> Extraiga el archivo. cab de MSM en el archivo.                        |
| -lfn       | Use nombres de archivo largos durante la extracción.                                 |
| -configurar | <*nombre* de archivo> configurar el módulo mediante datos de un archivo.            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



