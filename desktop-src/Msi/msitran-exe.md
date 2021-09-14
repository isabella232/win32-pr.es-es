---
description: Msitran.exe usa MsiDatabaseGenerateTransform, MsiCreateTransformSummaryInfo y MsiDatabaseApplyTransform para generar o aplicar un archivo de transformación. Esta herramienta solo está disponible en los componentes Windows SDK para desarrolladores Windows Installer.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074349"
---
# <a name="msitranexe"></a>Msitran.exe

Msitran.exe usa [**MsiDatabaseGenerateTransform,**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)y [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) para generar o aplicar un archivo de transformación.

Esta herramienta solo está disponible en los componentes Windows [SDK para desarrolladores Windows Instalador.](platform-sdk-components-for-windows-installer-developers.md)

## <a name="syntax"></a>Sintaxis

Use la sintaxis siguiente para generar una transformación.

**msitran -g** *{base db}{ref db}{nombre de archivo de transformación} \[ {condiciones de error/condiciones de validación} \]*

Use la sintaxis siguiente para aplicar una transformación

**msitran -a** *{transform}{database} \[ {error conditions} \]*

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msitran.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guion.



| Opción | Descripción            |
|--------|------------------------|
| -g     | Generación de transformaciones.  |
| -a     | Transformar aplicación. |



 

Los siguientes errores se pueden suprimir al aplicar una transformación. Para suprimir un error, incluya el carácter adecuado en el argumento {error conditions}. Las condiciones especificadas con -g se colocan en la información de resumen de la transformación, pero no se usan al aplicar una transformación con -a. Para obtener información, [**vea MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).



| Opción | Error suprimido           |
|--------|----------------------------|
| a      | Agregue una fila existente.          |
| b      | Eliminar fila no existente.   |
| c      | Agregue una tabla existente.        |
| d      | Eliminar tabla no existente. |
| e      | Modifique la fila existente.       |
| f      | Cambiar la página de códigos.           |



 

Las siguientes condiciones de validación se pueden usar para indicar cuándo se puede aplicar una transformación a un paquete. Estas condiciones se pueden especificar con -g, pero no con -a.



| Opción | Condición de validación                                  |
|--------|-------------------------------------------------------|
| e      | Compruebe el código de actualización.                                   |
| l      | Compruebe el idioma.                                       |
| p      | Compruebe la plataforma.                                       |
| r      | Compruebe el producto.                                        |
| s      | Compruebe solo la versión principal.                             |
| t      | Compruebe solo las versiones principales y secundarias.                  |
| u      | Compruebe las versiones principales, secundarias y de actualización.             |
| v      | Versión de base de datos < base de datos base.  |
| w      | Versión de base de datos <= Versión base de la base de datos. |
| x      | Versión de base de datos aplicada = versión de base de datos base.     |
| y      | Versión de base de datos >= Versión base de la base de datos. |
| z      | Versión de base de datos > base de datos base.  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Transformaciones de base de datos](database-transforms.md)
</dt> <dt>

[Ejemplo de transformación de personalización](a-customization-transform-example.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



