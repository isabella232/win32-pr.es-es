---
description: Msitran.exe usa MsiDatabaseGenerateTransform, MsiCreateTransformSummaryInfo y MsiDatabaseApplyTransform para generar o aplicar un archivo de transformación. Esta herramienta solo está disponible en los componentes de Windows SDK para los desarrolladores de Windows Installer.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678248"
---
# <a name="msitranexe"></a>Msitran.exe

Msitran.exe usa [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)y [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) para generar o aplicar un archivo de transformación.

Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintaxis

Use la siguiente sintaxis para generar una transformación.

**MsiTran-g** *{base dB} {Ref dB} {Transform File name} \[ {condiciones de error/condiciones de \] validación}*

Use la siguiente sintaxis para aplicar una transformación

**MsiTran-a** *{Transform} {Database} \[ {condiciones de error \] }*

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msitran.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión.



| Opción | Descripción            |
|--------|------------------------|
| -g     | Generación de transformación.  |
| -a     | Aplicación de transformación. |



 

Los errores siguientes se pueden suprimir al aplicar una transformación. Para suprimir un error, incluya el carácter apropiado en el argumento {error conditions}. Las condiciones especificadas con-g se colocan en la información de Resumen de la transformación, pero no se usan al aplicar una transformación con-a. Para obtener información, consulte [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).



| Opción | Error suprimido           |
|--------|----------------------------|
| a      | Agregar fila existente.          |
| b      | Elimina una fila no existente.   |
| c      | Agregar tabla existente.        |
| d      | Eliminar tabla no existente. |
| h      | Modifique la fila existente.       |
| f      | Cambiar página de códigos.           |



 

Se pueden usar las siguientes condiciones de validación para indicar cuándo se puede aplicar una transformación a un paquete. Estas condiciones se pueden especificar con-g, pero no con-a.



| Opción | Condición de validación                                  |
|--------|-------------------------------------------------------|
| e      | Compruebe el código de actualización.                                   |
| l      | Compruebe el idioma.                                       |
| p      | Compruebe la plataforma.                                       |
| r      | Compruebe el producto.                                        |
| s      | Compruebe solo la versión principal.                             |
| t      | Compruebe solo las versiones principal y secundaria.                  |
| u      | Compruebe las versiones principal, secundaria y de actualización.             |
| v      | Versión de base de datos aplicada < versión de base de datos base.  |
| w      | Versión de base de datos aplicada <= versión de base de datos base. |
| x      | Versión de base de datos aplicada = versión de base de datos base.     |
| y      | Versión de base de datos aplicada >= versión de base de datos base. |
| z      | Versión de base de datos aplicada > versión de base de datos base.  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Transformaciones de base de datos](database-transforms.md)
</dt> <dt>

[Ejemplo de transformación de personalización](a-customization-transform-example.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



