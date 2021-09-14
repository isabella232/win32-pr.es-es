---
description: La tabla FileSFPCatalog asocia los archivos especificados con los archivos de catálogo utilizados por la protección de archivos del sistema.
ms.assetid: 70c8b64a-cf15-411c-8388-4a7e3051f45c
title: Tabla FileSFPCatalog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2300b73cc1639d8a54e206ea609043cf657c91f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074778"
---
# <a name="filesfpcatalog-table"></a>Tabla FileSFPCatalog

La tabla FileSFPCatalog asocia los archivos especificados con los archivos de catálogo utilizados por la protección de archivos del sistema.

**Windows Vista, Windows Server 2003 y Windows XP:** No se admite.

La tabla FileSFPCatalog tiene las columnas siguientes.



| Columna       | Tipo                         | Clave | Nullable |
|--------------|------------------------------|-----|----------|
| Archivo\_       | [Identificador](identifier.md) | Y   | N        |
| SFPCatalog\_ | [Nombre de archivo](filename.md)     | Y   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Archivo\_
</dt> <dd>

Clave externa a la [tabla File](file-table.md).

</dd> <dt>

<span id="SFPCatalog_"></span><span id="sfpcatalog_"></span><span id="SFPCATALOG_"></span>SFPCatalog\_
</dt> <dd>

Clave externa a la [tabla SFPCatalog](sfpcatalog-table.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [acción InstallSFPCatalogFile](installsfpcatalogfile-action.md) consulta la tabla [Component](component-table.md), la [tabla File,](file-table.md)la tabla FileSFPCatalog y [la tabla SFPCatalog](sfpcatalog-table.md).

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE76](ice76.md)  
</dl>

 

 



