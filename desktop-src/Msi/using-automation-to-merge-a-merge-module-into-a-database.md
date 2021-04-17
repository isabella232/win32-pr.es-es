---
description: Los módulos de combinación proporcionan un método estándar para proporcionar componentes compartidos de Windows Installer y la lógica de configuración para las aplicaciones.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Usar la automatización para combinar un módulo de combinación en una base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e28b8cfc1716cdbb296fd0a1410787ae55bb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677523"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a>Usar la automatización para combinar un módulo de combinación en una base de datos

Los [módulos de combinación](merge-modules.md) proporcionan un método estándar para proporcionar [*componentes*](c-gly.md)compartidos de Windows Installer y la lógica de configuración para las aplicaciones.

Los módulos de combinación se deben combinar en un paquete de instalación mediante una herramienta de combinación. El procedimiento recomendado es obtener una herramienta de combinación distribuida de forma gratuita o comprar una de las herramientas de combinación que están disponibles en proveedores de software independientes, por ejemplo, puede usar [Mergemod.dll](merge-module-automation.md).

En el procedimiento siguiente se muestra cómo combinar un módulo de combinación en una base de datos de Windows Installer mediante la [automatización del módulo de combinación](merge-module-automation.md).

**Para combinar un módulo en una base de datos**

1.  Abra un archivo de registro mediante el método [**openlog**](merge-openlog.md) .

    Este paso solo es necesario si necesita crear un archivo de registro o anexar un archivo de registro existente para el proceso de mezcla.

2.  Abra la base de datos de instalación [. msi](windows-installer-file-extensions.md) mediante el método [**OpenDatabase**](merge-opendatabase.md) del [**objeto Merge**](merge-object.md).

    Este paso es obligatorio.

    La base de datos que abre es aquella en la que desea recibir el módulo de combinación.

3.  Abra el módulo de combinación [. MSM](windows-installer-file-extensions.md) con el método [**OpenModule**](merge-openmodule.md) .

    Este paso es obligatorio.

    Éste es el módulo de combinación que se combina en la base de datos. Un módulo debe estar abierto antes de que se pueda combinar con una base de datos de instalación.

4.  Combine el módulo en la base de datos de instalación mediante una llamada al método [**Merge**](merge-object.md) o al método [**MergeEx**](merge-mergeex.md) .

    Este paso es obligatorio.

    Solo se puede llamar una vez al método [**Merge**](merge-object.md) o al método [**MergeEx**](merge-mergeex.md) para combinar una combinación específica de archivos [. msi](windows-installer-file-extensions.md) y. msm.

    > [!Note]  
    > El método [**MergeEx**](merge-mergeex.md) solo está disponible en [Mergemod.dll versión 2,0](merge-module-automation.md) o posterior, y solo cuando se usa la interfaz [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .

     

5.  Recupere la propiedad [**Errors**](merge-errors.md) y examine la colección de objetos de [**error**](error-object.md) que devuelve para conflictos de combinación u otros errores.

    Debe resolver los errores.

    La recuperación no es destructiva y se pueden recuperar varias instancias de la colección de errores mediante la lectura repetida de la propiedad [**errores**](merge-errors.md) .

6.  Asocie los componentes del módulo de combinación con las características de mediante el método [**Connect**](merge-connect.md) .

    Este paso solo es necesario si tiene características existentes y desea agregar características para combinarlas en la base de datos de instalación.

    Una característica debe existir antes de llamar a este método. Para obtener más información, vea [conectar un módulo de combinación a varias características](connecting-a-merge-module-to-multiple-features.md).

7.  Si es necesario, extraiga los archivos de origen del módulo mediante uno o varios de los siguientes procedimientos:
    -   Use [**ExtractFiles**](merge-extractfiles.md) o [**ExtractFilesEx**](merge-extractfilesex.md) para extraer archivos de un archivo. cab incrustado y, a continuación, cópielo en un directorio especificado.
        > [!Note]  
        > [**ExtractFilesEx**](merge-extractfilesex.md) requiere [Mergemod.dll versión 2,0](merge-module-automation.md) o posterior.

         

    -   Use [**ExtractCAB**](merge-extractcab.md) para extraer archivos de un archivo. cab incrustado y, a continuación, guárdelos en un archivo especificado.
    -   Use [**CreateSourceImage**](merge-createsourceimage.md) para extraer archivos de un módulo y, después de la fusión mediante combinación, cópielo en una imagen de origen en el disco.
        > [!Note]  
        > [**CreateSourceImage**](merge-createsourceimage.md) solo está disponible en [Mergemod.dll versión 2,0](merge-module-automation.md) o posterior.

         
8.  Cierre el módulo de combinación abierto actual mediante el método [**CloseModule**](merge-closemodule.md) .

    Este paso es obligatorio.

9.  Cierre la base de datos de instalación abierta con el método [**CerrarBaseDeDatos**](merge-closedatabase.md) .

    Este paso es obligatorio.

    Al cerrar una base de datos, se borra toda la información de dependencias, pero no se producen errores que no se recuperen.

10. Cierre el archivo de registro actual mediante el método [**closelog**](merge-closelog.md) .

    Este paso es necesario si tiene un archivo de registro abierto.

Una vez que el módulo se ha combinado en la base de datos mediante [Mergemod.dll](merge-module-automation.md), la [tabla de medios](media-table.md) debe actualizarse para describir el diseño de la imagen de origen deseada. El proceso de mezcla proporcionado por Mergemod.dll no actualiza la tabla de medios porque el consumidor del módulo de combinación puede seleccionar varias maneras de diseñar la imagen de origen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



