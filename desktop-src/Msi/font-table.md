---
description: La tabla Font contiene la información para registrar archivos de fuentes con el sistema.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Tabla de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002269"
---
# <a name="font-table"></a>Tabla de fuentes

La tabla Font contiene la información para registrar archivos de fuentes con el sistema.

La tabla de fuentes tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Archivo\_    | [Identificador](identifier.md) | Y   | N        |
| FontTitle | [Texto](text.md)             | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_
</dt> <dd>

Clave externa en la entrada de la [tabla de archivos](file-table.md) para el archivo de fuente. Se recomienda que el componente que contiene el archivo de fuente tenga el valor de FontsFolder especificado en la \_ columna directorio de la [tabla de componentes](component-table.md).

</dd> <dt>

<span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle
</dt> <dd>

Nombre de la fuente. Se recomienda dejar esta columna null para las fuentes TrueType y las colecciones TrueType porque el instalador puede registrar la fuente después de leer el título de fuente correcto del archivo de fuente. Si se escribe el nombre de la fuente, debe ser idéntico al título de fuente del archivo de fuente. Debe especificar un título para las fuentes que no tengan nombres incrustados, como los archivos. fon.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a esta tabla cuando se ejecuta la acción [RegisterFonts](registerfonts-action.md) o la [acción UnregisterFonts](unregisterfonts-action.md) .

Si el campo FontTitle es null, el nombre de la fuente se lee directamente desde el archivo de fuente especificado. Si el nombre de fuente grabado en el campo FontTitle difiere del nombre de fuente interno registrado en el archivo de fuente, la fuente se registra dos veces en la [acción RegisterFonts](registerfonts-action.md).

Los archivos de fuentes no deben crearse con un identificador de idioma, ya que las fuentes no tienen un recurso de identificador de idioma incrustado. Por lo tanto, la columna de idioma de la [tabla de archivos](file-table.md) debe dejarse como null para los archivos de fuentes.

Dado que el instalador no rerefcount los archivos de fuentes de forma predeterminada, los archivos de fuentes preexistentes se pueden quitar con su componente al desinstalar una aplicación. Para asegurarse de que no se quita un archivo de fuente, los autores pueden establecer las marcas de bits **msidbComponentAttributesSharedDllRefCount** o **msidbComponentAttributesPermanent** en la columna Attributes de la tabla componente MSI del componente de tabla del componente \_ \_ \_ que contiene el archivo de fuente.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE32](ice32.md)  
[ICE51](ice51.md)  
[ICE60](ice60.md)  
</dl>

 

 



