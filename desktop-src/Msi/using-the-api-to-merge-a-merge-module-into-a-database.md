---
description: Los módulos de combinación proporcionan un método estándar para que los desarrolladores proporcionen componentes compartidos Windows Installer y la lógica de configuración a sus aplicaciones.
ms.assetid: 3eb087b1-0f44-40d8-a950-67d489f09408
title: Uso de la API para combinar un módulo de combinación en una base de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e68298671045825dda41ad120896fa22c89f068
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074279"
---
# <a name="using-the-api-to-merge-a-merge-module-into-a-database"></a>Uso de la API para combinar un módulo de combinación en una base de datos

[Los módulos de](merge-modules.md) combinación proporcionan un método estándar para que los desarrolladores entreguen componentes compartidos Windows [*Installer*](c-gly.md) y la lógica de configuración a sus aplicaciones. Los módulos de combinación deben combinarse en un paquete de instalación mediante una herramienta de combinación. La mejor alternativa es obtener una herramienta de combinación distribuida libremente o adquirir una de las herramientas de combinación disponibles de proveedores de software independientes. Por ejemplo, puede usar la funcionalidad proporcionada por [Mergemod.dll](merge-module-automation.md).

Use los pasos siguientes en secuencia para combinar un módulo de combinación en una base de datos de instalación Windows Installer mediante la API de [Mergemod.dll](merge-module-automation.md).

**Para combinar un módulo de combinación en una base de Windows de instalación del instalador**

1.  Abra un archivo de registro mediante [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog). Este paso solo es necesario si necesita crear un archivo de registro o anexar un archivo de registro existente para el proceso de combinación.
2.  Abra la base de datos de [ instalación,.msi archivo](windows-installer-file-extensions.md), que recibirá el módulo de combinación mediante [**OpenDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-opendatabase). Este paso es obligatorio.
3.  Abra el módulo merge, un [archivo .msm](windows-installer-file-extensions.md), que se va a combinar en la base de datos [**mediante OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule). Se debe abrir un módulo para poder combinarlo con una base de datos de instalación. Este paso es obligatorio.
4.  Combine el módulo en la base de datos de instalación mediante [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) o [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex). Tenga en **cuenta que solo** se puede llamar a Merge o **MergeEx** una vez para combinar una combinación determinada de archivos .msi y .msm. **MergeEx** solo está disponible cuando se [Mergemod.dll versión 2.0](merge-module-automation.md) o posterior y solo cuando se usa la [interfaz IMsmMerge2.](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Este paso es obligatorio.
5.  Llame [**a get \_ Errors**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) y examine la colección recuperada de errores en busca de conflictos de combinación u otros errores. La recuperación no es destructiva. Se pueden recuperar varias instancias de la colección de errores leyendo repetidamente una llamada **a get \_ Errors**. Deberá resolver los errores según corresponda en su caso.
6.  Asocie los componentes del módulo de combinación a las características adicionales que se hayan combinado o se combinarán en la base de datos de instalación [**Conectar**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect). La característica ya debe existir antes de llamar a este método. Este paso solo es necesario si tiene características adicionales. Para obtener más información, vea [Conectar un módulo de combinación a varias características.](connecting-a-merge-module-to-multiple-features.md)
7.  Si es necesario, extraiga los archivos de origen del módulo mediante una o varias de las acciones siguientes.

    Para extraer archivos de un archivo .cab y, a continuación, copiarlos en un directorio especificado, use [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) o [**ExtractFilesEx.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) Tenga en **cuenta que ExtractFilesEx** [Mergemod.dll versión 2.0](merge-module-automation.md) o posterior.

    Para extraer archivos de un archivo .cab y, a continuación, guardarlos en un archivo especificado, use [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab).

    Para extraer archivos de un módulo y, a continuación, copiarlos en una imagen de origen en el disco después de la combinación, use [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage). Tenga en **cuenta que CreateSourceImage** solo está disponible [Mergemod.dll versión 2.0](merge-module-automation.md) o posterior.

8.  Cierre el módulo de combinación abierto actual mediante [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule). Este paso es obligatorio.
9.  Cierre la base de datos de instalación abierta actual [**mediante CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase). Este paso es obligatorio. El cierre de una base de datos borra toda la información de dependencia, pero no afecta a los errores que no se han recuperado.
10. Cierre el archivo de registro actual mediante [**CloseLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closelog). Este paso es necesario si ha abierto un archivo de registro.

Una vez que el módulo se ha combinado en [](media-table.md) la base de [datos medianteMergemod.dll](merge-module-automation.md), la tabla multimedia debe actualizarse para describir el diseño de imagen de origen deseado. El proceso de combinación proporcionado por Mergemod.dll no actualiza la tabla multimedia porque el consumidor del módulo de combinación puede seleccionar varias maneras de diseño de la imagen de origen.

 

 
