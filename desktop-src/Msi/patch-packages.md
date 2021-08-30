---
description: Una Windows installer (archivo .msp) es un archivo que se usa para entregar actualizaciones a Windows Installer.
ms.assetid: f59736d7-0b5a-466c-ab60-f210ccccb07f
title: Paquetes de revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c933ff632774652c7c2a6f23a57ea94ebfff20ac5ac263006a567f66e628ac0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074835"
---
# <a name="patch-packages"></a>Paquetes de revisión

Una Windows installer (archivo .msp) es un archivo que se usa para entregar actualizaciones a Windows Installer. La revisión es un paquete independiente que contiene toda la información necesaria para actualizar la aplicación. Un paquete de revisión (archivo .msp) puede ser mucho más pequeño que el paquete Windows Installer (.msi archivo) para toda la aplicación actualizada. Para obtener más información sobre cómo entregar actualizaciones más pequeñas a las aplicaciones, vea [Reducción del tamaño de revisión.](reducing-patch-size.md)

Un paquete de revisión contiene las actualizaciones reales de la aplicación y describe qué versiones de la aplicación pueden recibir la revisión. Las revisiones contienen como mínimo dos transformaciones de base de datos. Una transformación actualiza la información de la base de datos de instalación de la aplicación. La otra transformación agrega información que el instalador usa para aplicar revisiones a los archivos. El instalador usa la información proporcionada por las transformaciones para aplicar los archivos de revisión almacenados en el flujo de archivos de archivo del paquete de revisión. Un paquete de revisión no tiene una base de datos como un paquete de instalación (.msi archivo).

A partir de Windows Installer versión 3.0, los paquetes de revisión pueden contener información que describe la secuencia de aplicación de revisiones de la revisión con respecto a otras actualizaciones de la tabla [MsiPatchSequence](msipatchsequence-table.md) e información descriptiva adicional en [la tabla MsiPatchMetadata.](msipatchmetadata-table.md)

Los usuarios pueden instalar aplicaciones y actualizaciones desde una imagen administrativa de red. Aunque los paquetes de revisión se pueden aplicar a instalaciones administrativas, el método recomendado para entregar actualizaciones es hacer que los usuarios instalen la aplicación original y, a continuación, aplicar las revisiones a la instancia local de la aplicación en su equipo. Esto mantiene a los usuarios en sincronización con la imagen administrativa. Si se aplica una revisión a la instalación administrativa, todos los clientes de esa instalación administrativa deben volver a almacenar en caché y reinstalar la aplicación para recibir la actualización. Hasta que un usuario vuelva a almacenar en caché y reinstalar, el usuario no podrá instalar instalaciones a petición y reparar desde la instalación administrativa con revisión.

A partir de Windows Installer 3.0, los usuarios que no son administradores pueden aplicar revisiones a las aplicaciones administradas por usuario después de que un administrador haya aprobado la revisión como de confianza. Para obtener más información sobre cómo hacerlo, vea Aplicación de revisiones [Per-User aplicaciones administradas.](patching-per-user-managed-applications.md) Otro método consiste en usar la aplicación de revisiones de cuentas de usuario con privilegios mínimos.

> [!Note]  
> Si se ha establecido la directiva [AllowLockdownPatch,](allowlockdownpatch.md) los usuarios que no son administradores pueden aplicar una revisión a una aplicación existente mientras ejecutan una instalación con privilegios elevados. Este método no se recomienda porque permite aplicar revisiones que no son de confianza a una aplicación que se puede ejecutar con privilegios elevados.

 

Los paquetes de revisión se componen de las siguientes partes. Para obtener más información sobre la construcción de paquetes de revisión, vea [Creating a Patch Package](creating-a-patch-package.md).

## <a name="summary-information-stream"></a>Secuencia de información de resumen

El flujo de información de resumen del paquete de revisión proporciona información sobre la identidad y el propósito de la revisión.

El flujo de información de resumen contiene un mínimo de lo siguiente:

-   GUID que identifica de forma única la revisión. El GUID de esta revisión se anexa con una lista de GUID para revisiones anteriores que se reemplazan por esta revisión.
-   Lista delimitada por punto y coma de códigos de producto para destinos válidos para esta revisión.
-   Lista delimitada por punto y coma de nombres de subalmacenamiento de transformación en el orden en que se van a procesar.
-   Una lista delimitada por punto y coma de orígenes para esta revisión.

## <a name="transform-substorage"></a>Transformación de subalmacenamiento

Un paquete de revisión contiene transformaciones que pueden agregar o quitar archivos, entradas del Registro, interfaces de usuario y personalizaciones. Las transformaciones se incluyen como subalmacenamientos en el paquete. Un paquete de revisión contiene dos transformaciones para cada base de datos de destino. Una transformación son las actualizaciones reales de la base de datos de instalación y se genera a partir de las diferencias entre las imágenes originales y actualizadas del paquete de instalación. La otra transformación agrega entradas a las tablas [Patch](patch-table.md), [PatchPackage](patchpackage-table.md), [Media,](media-table.md) [InstallExecuteSequence](installexecutesequence-table.md)y [AdminExecuteSequence.](adminexecutesequence-table.md) La información del subalmacenamiento la vincula a un [**UpgradeCode,**](upgradecode.md) [**ProductCode,**](productcode.md) [**ProductVersion**](productversion.md)y [**ProductLanguage específicos.**](productlanguage.md) Un paquete de revisión que se puede aplicar a varios destinos contiene más de un par de estas transformaciones.

## <a name="cabinet-file-stream"></a>Flujo de archivos de archivo de archivado

El flujo de archivos del archivador incluido en una revisión puede contener estos tipos de archivos:

-   Aplicar revisiones a los archivos que contienen la información necesaria para cambiar la versión anterior del archivo a la nueva versión. Se puede usar un único archivo de revisión para actualizar una o varias versiones anteriores de un archivo.
-   Archivos adicionales que se agregan a la aplicación que no están presentes en la versión anterior.
-   Un archivo de reemplazo completo. En el raras ocasiones en que la nueva versión de un archivo es menor que la revisión necesaria para actualizar la versión anterior de ese archivo, el nuevo archivo se puede incluir en su totalidad. Se trata de archivos nuevos que se instalan en sus versiones anteriores.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de un paquete de revisión](creating-a-patch-package.md)
</dt> </dl>

 

 



