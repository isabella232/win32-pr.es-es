---
description: MsiFiler.exe rellena la tabla de archivos con versiones de archivo, idiomas y tamaños basados en un directorio de origen. También puede actualizar la tabla MsiFileHash con los hash de archivo.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666464"
---
# <a name="msifilerexe"></a>Msifiler.exe

MsiFiler.exe rellena la [tabla de archivos](file-table.md) con versiones de archivo, idiomas y tamaños basados en un directorio de origen. También puede actualizar la [tabla MsiFileHash](msifilehash-table.md) con los hash de archivo.

## <a name="syntax"></a>Sintaxis

**msifiler.exe-d** *{base de datos}* **\[ -v- \] \[ h \] \[ - \] s ALTSOURCE**

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msifiler.exe usa las siguientes opciones de la línea de comandos que no distinguen mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión.



| Opción | Parámetro   | Descripción                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -d     | *database*  | La base de datos (archivo. msi) que se va a actualizar.                                                                                                                              |
| -v     |             | Usar el modo detallado.                                                                                                                                                            |
| -H     |             | Rellene la [tabla MsiFileHash](msifilehash-table.md). Esto crea la tabla si aún no existe. La tabla MsiFileHash solo se puede usar con archivos sin versión. |
| -S     | *ALTSOURCE* | ALTSOURCE especifica un directorio alternativo para encontrar los archivos.                                                                                                              |



 

Esta herramienta solo está disponible en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Usar la tabla de directorio](using-the-directory-table.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



