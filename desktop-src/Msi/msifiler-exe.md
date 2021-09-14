---
description: MsiFiler.exe rellena la tabla Archivo con versiones de archivo, idiomas y tamaños basados en un directorio de origen. También puede actualizar la tabla MsiFileHash con hashes de archivo.
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071848"
---
# <a name="msifilerexe"></a>Msifiler.exe

MsiFiler.exe rellena la tabla [Archivo](file-table.md) con versiones de archivo, idiomas y tamaños basados en un directorio de origen. También puede actualizar la tabla [MsiFileHash con hashes](msifilehash-table.md) de archivo.

## <a name="syntax"></a>Sintaxis

**msifiler.exe -d** *{database}* **\[ -v \] \[ -h \] \[ -s \] ALTSOURCE**

## <a name="command-line-options"></a>Opciones de la línea de comandos

Msifiler.exe usa las siguientes opciones de línea de comandos que no tienen en cuenta mayúsculas de minúsculas. También se puede usar un delimitador de barra diagonal en lugar de un guion.



| Opción | Parámetro   | Descripción                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -d     | *database*  | Base de datos (.msi archivo) que se va a actualizar.                                                                                                                              |
| -v     |             | Use el modo detallado.                                                                                                                                                            |
| -H     |             | Rellene la [tabla MsiFileHash](msifilehash-table.md). Esto crea la tabla si aún no existe. La tabla MsiFileHash solo se puede usar con archivos sin versión. |
| -S     | *ALTSOURCE* | ALTSOURCE especifica un directorio alternativo para buscar los archivos.                                                                                                              |



 

Esta herramienta solo está disponible en los componentes Windows [SDK para desarrolladores Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
</dt> <dt>

[Uso de la tabla de directorios](using-the-directory-table.md)
</dt> <dt>

[Versiones publicadas, herramientas y redistribuibles](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



