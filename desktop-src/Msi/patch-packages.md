---
description: Una revisión de Windows Installer (archivo. msp) es un archivo que se usa para proporcionar actualizaciones a Windows Installer aplicaciones.
ms.assetid: f59736d7-0b5a-466c-ab60-f210ccccb07f
title: Paquetes de revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b4bb5b7e182c8118f5a40c45be440784b92099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812859"
---
# <a name="patch-packages"></a>Paquetes de revisión

Una revisión de Windows Installer (archivo. msp) es un archivo que se usa para proporcionar actualizaciones a Windows Installer aplicaciones. La revisión es un paquete independiente que contiene toda la información necesaria para actualizar la aplicación. Un paquete de revisión (archivo. msp) puede ser mucho más pequeño que el paquete de Windows Installer (archivo. msi) de toda la aplicación actualizada. Para obtener más información acerca de cómo entregar actualizaciones más pequeñas a las aplicaciones, consulte [reducir el tamaño](reducing-patch-size.md)de la revisión.

Un paquete de revisión contiene las actualizaciones reales de la aplicación y describe qué versiones de la aplicación pueden recibir la revisión. Las revisiones contienen como mínimo dos transformaciones de base de datos. Una transformación actualiza la información en la base de datos de instalación de la aplicación. La otra transformación agrega información que el instalador utiliza para aplicar revisiones a los archivos. El instalador usa la información proporcionada por las transformaciones para aplicar archivos de revisión que se almacenan en la secuencia del archivo. cab del paquete de revisión. Un paquete de revisión no tiene una base de datos como un paquete de instalación (archivo. msi).

A partir de Windows Installer versión 3,0, los paquetes de revisión pueden contener información que describe la secuencia de revisión de la revisión relativa a otras actualizaciones de la tabla [MsiPatchSequence](msipatchsequence-table.md) e información adicional descriptiva en la tabla [MsiPatchMetadata](msipatchmetadata-table.md) .

Los usuarios pueden instalar aplicaciones y actualizaciones de una imagen administrativa de red. Aunque los paquetes de revisión pueden aplicarse a las instalaciones administrativas, el método recomendado para proporcionar actualizaciones consiste en que los usuarios instalen la aplicación original y, a continuación, apliquen las revisiones a la instancia local de la aplicación en su equipo. Esto impide que los usuarios se sincronizan con la imagen administrativa. Si se aplica una revisión a la instalación administrativa, todos los clientes de esa instalación administrativa deben volver a almacenar en caché la aplicación para recibir la actualización. Hasta que un usuario se vuelve a almacenar en caché y se vuelve a instalar, el usuario no puede instalar las instalaciones a petición y reparar desde la instalación administrativa revisada.

A partir de Windows Installer 3,0, los usuarios que no son administradores pueden aplicar revisiones a las aplicaciones administradas por el usuario después de que un administrador haya aprobado la revisión como de confianza. Para obtener más información sobre cómo hacerlo, consulte [aplicación de revisiones Per-User aplicaciones administradas](patching-per-user-managed-applications.md). Otro método consiste en usar la revisión de cuentas de usuario con privilegios mínimos.

> [!Note]  
> Si se ha establecido la directiva [AllowLockdownPatch](allowlockdownpatch.md) , los usuarios que no sean administradores pueden aplicar una revisión a una aplicación existente mientras se ejecuta una instalación con privilegios elevados. No se recomienda este método porque permite aplicar revisiones que no son de confianza a una aplicación que se puede ejecutar con privilegios elevados.

 

Los paquetes de revisión se componen de las siguientes partes. Para obtener más información sobre la construcción de paquetes de revisión, consulte [crear un paquete de revisión](creating-a-patch-package.md).

## <a name="summary-information-stream"></a>Flujo de información de Resumen

La secuencia de información de resumen del paquete de revisión proporciona información acerca de la identidad y el propósito de la revisión.

La secuencia de información de Resumen contiene un mínimo de lo siguiente:

-   GUID que identifica de forma única la revisión. El GUID de esta revisión se anexa con una lista de GUID para las revisiones anteriores que se sustituyen por esta revisión.
-   Una lista delimitada por signos de punto y coma de códigos de producto para los destinos válidos para esta revisión.
-   Una lista delimitada por signos de punto y coma de nombres de subalmacenamiento de transformación en el orden en que se van a procesar.
-   Una lista delimitada por signos de punto y coma de orígenes para esta revisión.

## <a name="transform-substorage"></a>Transformación del subalmacenamiento

Un paquete de revisión contiene transformaciones que pueden agregar o quitar archivos, entradas del registro, interfaces de usuario y personalizaciones. Las transformaciones se incluyen como subalmacenamientos en el paquete. Un paquete de revisión contiene dos transformaciones para cada base de datos de destino. Una transformación es las actualizaciones reales de la base de datos de instalación y se genera a partir de las diferencias entre las imágenes originales y actualizadas del paquete de instalación. La otra transformación agrega entradas a las tablas [patch](patch-table.md), [PatchPackage](patchpackage-table.md), [media](media-table.md), [InstallExecuteSequence](installexecutesequence-table.md)y [AdminExecuteSequence](adminexecutesequence-table.md) . La información del subalmacenamiento lo vincula a un [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md)y [**ProductLanguage**](productlanguage.md)específicos. Un paquete de revisión que se puede aplicar a varios destinos contiene más de un par de estas transformaciones.

## <a name="cabinet-file-stream"></a>Secuencia de archivos. cab

La secuencia del archivo. cab incluida en una revisión puede contener estos tipos de archivos:

-   Archivos de revisión que contienen la información necesaria para cambiar la versión anterior del archivo a la nueva versión. Se puede usar un solo archivo de revisión para actualizar una o más versiones anteriores de un archivo.
-   Archivos adicionales que se agregan a la aplicación que no están presentes en la versión anterior.
-   Un archivo de reemplazo completo. En el caso excepcional en el que la nueva versión de un archivo es menor que la revisión necesaria para actualizar la versión anterior de ese archivo, el nuevo archivo se puede incluir en su totalidad. Se trata de archivos nuevos que se instalan con sus versiones anteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear un paquete de revisión](creating-a-patch-package.md)
</dt> </dl>

 

 



