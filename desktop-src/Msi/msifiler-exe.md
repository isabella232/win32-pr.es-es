---
description: MsiFiler.exe rellena la tabla File con versiones, idiomas y tamaños de archivo basados en un directorio de origen. También puede actualizar la tabla MsiFileHash con hashes de archivo.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d3306fdae929c3659baf07668486fdf8a828012ce3142e4285bde8ad7a6c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679645"
---
# <a name="msifilerexe"></a>Msifiler.exe

MsiFiler.exe rellena la tabla [File](file-table.md) con versiones de archivo, idiomas y tamaños basados en un directorio de origen. También puede actualizar la tabla [MsiFileHash con hashes](msifilehash-table.md) de archivo.

## <a name="syntax"></a>Syntax

**msifiler.exe -d** *{database}* **\[ -v \] \[ -h \] \[ -s ALTSOURCE \]**

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msifiler.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta las mayúsculas y minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guión.



| Opción | Parámetro   | Descripción                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -d     | *database*  | Base de datos (.msi archivo) que se va a actualizar.                                                                                                                              |
| -v     |             | Use el modo detallado.                                                                                                                                                            |
| -H     |             | Rellene la [tabla MsiFileHash](msifilehash-table.md). Esto crea la tabla si aún no existe. La tabla MsiFileHash solo se puede usar con archivos sin versión. |
| -S     | *ALTSOURCE* | ALTSOURCE especifica un directorio alternativo para buscar los archivos.                                                                                                              |



 

Esta herramienta solo está disponible en los componentes del [SDK de Windows para Windows programadores del instalador](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Uso de la tabla de directorios](using-the-directory-table.md)
</dt> <dt>

[Versiones, herramientas y redistribuibles publicados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



