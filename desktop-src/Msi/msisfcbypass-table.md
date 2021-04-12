---
description: La tabla MsiSFCBypass contiene una lista de archivos que deben omitir la protección de archivos de Windows cuando los archivos se instalan en Microsoft Windows me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Tabla MsiSFCBypass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361066"
---
# <a name="msisfcbypass-table"></a>Tabla MsiSFCBypass

La tabla MsiSFCBypass contiene una lista de archivos que deben omitir la protección de archivos de Windows cuando los archivos se instalan en Microsoft Windows me.

La tabla MsiSFCBypass tiene la siguiente columna.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Archivo\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_
</dt> <dd>

La clave externa de la [tabla de archivos](file-table.md) que especifica el archivo que debe omitir la protección de archivos de Windows cuando el archivo está instalado en Windows me.

</dd> </dl>

 

 



