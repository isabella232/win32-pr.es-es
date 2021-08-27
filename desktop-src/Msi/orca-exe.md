---
description: Orca.exe es un editor de tablas de base de datos para crear y editar paquetes Windows instalador y módulos de combinación.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f1b0d31936bf81e60efd8eb9799ddb30b4d5a6f78363e2ff5d3d638ae40c4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082685"
---
# <a name="orcaexe"></a>Orca.exe

Orca.exe es un editor de tablas de base de datos para crear y editar paquetes Windows instalador y módulos de combinación. La herramienta proporciona una interfaz gráfica para la validación, resaltando las entradas concretas donde se producen errores o advertencias de validación.

Esta herramienta solo está disponible en los componentes del [SDK de Windows para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md). Se proporciona como un archivo Orca.msi datos. Después de instalar los componentes Windows SDK para desarrolladores Windows Installer, haga doble clic en Orca.msi para instalar el archivo Orca.exe.

## <a name="syntax"></a>Syntax

**orca***\[\<options>\]\[\<source file>\]*

## <a name="command-line-options"></a>Opciones de la línea de comandos

Orca.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta las mayúsculas y minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión.



| Opción | Descripción                                                 |
|--------|-------------------------------------------------------------|
| -q     | Modo silencioso                                                  |
| -S     | <*base*> de datos \[ de esquema "orca.dat": valor predeterminado\] |
| -?     | Cuadro de diálogo de ayuda                                                 |



 

Orca.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta las mayúsculas y minúsculas con los módulos de combinación. También se puede usar un delimitador de barra diagonal en lugar de un guión. Al realizar una combinación, se requieren las propiedades -f, -m <*sourcefile*>.



| Opción     | Descripción                                                                |
|------------|----------------------------------------------------------------------------|
| -c         | Confirme la combinación en la base de datos si no hay errores.                                     |
| -!         | Confirme la combinación en una base de datos incluso si hay errores.                       |
| -M         | <*módulo>* Módulo de combinación para combinar en la base de datos.                      |
| -f         | \[Característica:Características 2 para conectarse al módulo de \] mezcla.                |
| -r         | <*id. de* directorio> directory para el redireccionamiento raíz del módulo.    |
| -X         | <*directorio*> extraer archivos a una imagen en el directorio .         |
| -g         | <*language*> Language usado para abrir un módulo.                         |
| -l         | <*archivo de*> archivo que se va a usar como registro, anexe si ya existe.      |
| -i         | <*directorio*> extraer archivos en la imagen de origen en el directorio . |
| -cab       | <*nombre*> extraer el archivo del archivo del archivo.                        |
| -lfn       | Use nombres de archivo largos durante la extracción.                                 |
| -configure | <*nombre*> configurar el módulo mediante datos de un archivo.            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



