---
description: Los módulos de mezcla proporcionan un método estándar para entregar componentes compartidos Windows Installer y configurar la lógica a las aplicaciones.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Usar Automation para combinar un módulo de mezcla en una base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e28b8cfc1716cdbb296fd0a1410787ae55bb62
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254079"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a>Usar Automation para combinar un módulo de mezcla en una base de datos

[Los módulos](merge-modules.md) de mezcla proporcionan un método estándar para entregar componentes compartidos Windows [*Installer*](c-gly.md)y configurar la lógica a las aplicaciones.

Los módulos de mezcla se deben combinar en un paquete de instalación mediante una herramienta de combinación. El procedimiento recomendado es obtener una herramienta de combinación distribuida libremente o adquirir una de las herramientas de combinación que están disponibles para proveedores de software independientes, por ejemplo, puede usar [Mergemod.dll](merge-module-automation.md).

En el procedimiento siguiente se muestra cómo combinar un módulo de combinación en una base de Windows Installer mediante [Merge Module Automation](merge-module-automation.md).

**Para combinar un módulo en una base de datos**

1.  Abra un archivo de registro mediante el [**método OpenLog.**](merge-openlog.md)

    Este paso solo es necesario si necesita crear un archivo de registro o anexar un archivo de registro existente para el proceso de combinación.

2.  Abra la [.msi](windows-installer-file-extensions.md) de instalación mediante el método [**OpenDatabase**](merge-opendatabase.md) del [**objeto Merge**](merge-object.md).

    Este paso es obligatorio.

    La base de datos que se abre es la que desea recibir el módulo de combinación.

3.  Abra el [módulo de combinación .msm](windows-installer-file-extensions.md) mediante el [**método OpenModule.**](merge-openmodule.md)

    Este paso es obligatorio.

    Este es el módulo de combinación que se va a combinar en la base de datos. Se debe abrir un módulo para poder combinarlo con una base de datos de instalación.

4.  Combine el módulo en la base de datos de instalación mediante una llamada al [**método Merge**](merge-object.md) o al [**método MergeEx.**](merge-mergeex.md)

    Este paso es obligatorio.

    Solo [**se**](merge-object.md) puede llamar al método Merge o [**MergeEx**](merge-mergeex.md) una vez para combinar una combinación específica de archivos [.msi](windows-installer-file-extensions.md) y .msm.

    > [!Note]  
    > El [**método MergeEx**](merge-mergeex.md) solo está disponible enMergemod.dll [versión 2.0](merge-module-automation.md) o posterior, y solo cuando se usa la [**interfaz IMsmMerge2.**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2)

     

5.  Recupere la [**propiedad Errors**](merge-errors.md) y examine la colección de [**objetos Error**](error-object.md) que devuelve para conflictos de combinación u otros errores.

    Debe resolver los errores.

    La recuperación no es destructiva y se pueden recuperar varias instancias de la colección de errores leyendo repetidamente la [**propiedad Errors.**](merge-errors.md)

6.  Asocie los componentes del módulo de combinación con las características mediante el [**Conectar**](merge-connect.md) método .

    Este paso solo es necesario si tiene características existentes y desea agregar características para combinar en la base de datos de instalación.

    Debe existir una característica antes de llamar a este método. Para obtener más información, vea [Conectar un módulo de mezcla a varias características.](connecting-a-merge-module-to-multiple-features.md)

7.  Si es necesario, extraiga los archivos de código fuente del módulo mediante una o varias de las acciones siguientes:
    -   Use [**ExtractFiles**](merge-extractfiles.md) o [**ExtractFilesEx**](merge-extractfilesex.md) para extraer archivos de un archivo .cab incrustado y, a continuación, copiarlos en un directorio especificado.
        > [!Note]  
        > [**ExtractFilesEx**](merge-extractfilesex.md) requiere [Mergemod.dll versión 2.0](merge-module-automation.md) o posterior.

         

    -   Use [**ExtractCAB**](merge-extractcab.md) para extraer archivos de un archivo .cab y, a continuación, guárdelo en un archivo especificado.
    -   Use [**CreateSourceImage para**](merge-createsourceimage.md) extraer archivos de un módulo y, después de la combinación, copiar en una imagen de origen en el disco.
        > [!Note]  
        > [**CreateSourceImage**](merge-createsourceimage.md) solo está disponible en [Mergemod.dll versión 2.0](merge-module-automation.md) o posterior.

         
8.  Cierre el módulo de combinación abierto actual mediante el [**método CloseModule.**](merge-closemodule.md)

    Este paso es obligatorio.

9.  Cierre la base de datos de instalación abierta mediante el [**método CloseDatabase.**](merge-closedatabase.md)

    Este paso es obligatorio.

    El cierre de una base de datos borra toda la información de dependencia, pero no afecta a los errores que no se recuperan.

10. Cierre el archivo de registro actual mediante el [**método CloseLog.**](merge-closelog.md)

    Este paso es necesario si tiene un archivo de registro abierto.

Una vez que el módulo se ha combinado [](media-table.md) en la base de datos [medianteMergemod.dll](merge-module-automation.md), la tabla multimedia debe actualizarse para describir el diseño de la imagen de origen deseado. El proceso de combinación proporcionado por Mergemod.dll actualiza la tabla multimedia porque el consumidor del módulo de mezcla puede seleccionar varias maneras de diseño de la imagen de origen.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



