---
description: La tabla MsiSFCBypass contiene una lista de archivos que deben omitir Windows File Protection cuando los archivos se instalan en Microsoft Windows Me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Tabla MsiSFCBypass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d233f09aa62b5f6d17112b1f5a98753e328f3a1746c452de5a5a1689a36f971f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042675"
---
# <a name="msisfcbypass-table"></a>Tabla MsiSFCBypass

La tabla MsiSFCBypass contiene una lista de archivos que deben omitir Windows File Protection cuando los archivos se instalan en Microsoft Windows Me.

La tabla MsiSFCBypass tiene la columna siguiente.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Archivo\_ | [Identificador](identifier.md) | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Archivo\_
</dt> <dd>

Clave externa de la [tabla de](file-table.md) archivos que especifica el archivo que debe omitir Windows File Protection cuando el archivo se instala en Windows Me.

</dd> </dl>

 

 



