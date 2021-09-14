---
description: La tabla Fuente contiene la información para registrar archivos de fuente en el sistema.
ms.assetid: 5ddff430-a6f8-473b-8006-ac0124469a99
title: Tabla de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10208c7b9a14ca7f311aff71653a53a3da9ed0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074768"
---
# <a name="font-table"></a>Tabla de fuentes

La tabla Fuente contiene la información para registrar archivos de fuente en el sistema.

La tabla Font tiene las columnas siguientes.



| Columna    | Tipo                         | Clave | Nullable |
|-----------|------------------------------|-----|----------|
| Archivo\_    | [Identificador](identifier.md) | Y   | N        |
| FontTitle | [Texto](text.md)             | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Archivo\_
</dt> <dd>

Clave externa en la [entrada de la tabla Archivo](file-table.md) para el archivo de fuente. Se recomienda que el componente que contiene el archivo de fuente tenga el elemento FontsFolder especificado en la columna \_ Directory de la tabla [Component](component-table.md).

</dd> <dt>

<span id="FontTitle"></span><span id="fonttitle"></span><span id="FONTTITLE"></span>FontTitle
</dt> <dd>

Nombre de fuente. Se recomienda dejar esta columna en null para las fuentes TrueType y las colecciones TrueType, ya que el instalador puede registrar la fuente después de leer el título de fuente correcto del archivo de fuente. Si se introduce el nombre de fuente, debe ser idéntico al título de fuente del archivo de fuente. Debe especificar un título para las fuentes que no tienen nombres incrustados, como archivos .fon.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a esta tabla cuando se ejecuta [la acción RegisterFonts](registerfonts-action.md) o la acción [UnregisterFonts.](unregisterfonts-action.md)

Si el campo FontTitle se deja como Null, el nombre de fuente se lee directamente desde el archivo de fuente especificado. Si el nombre de fuente registrado en el campo FontTitle difiere del nombre de fuente interno registrado en el archivo de fuente, la fuente se registra dos veces mediante la [acción RegisterFonts](registerfonts-action.md).

Los archivos de fuente no deben crearse con un identificador de idioma, ya que las fuentes no tienen un recurso de identificador de idioma incrustado. Por lo tanto, la columna Language de [la tabla File](file-table.md) debe dejar null para los archivos de fuente.

Dado que el instalador no cuenta los archivos de fuente de forma predeterminada, los archivos de fuente preexistente se pueden quitar con su componente al desinstalar una aplicación. Para asegurarse de que no se quita un archivo de fuente, los autores pueden establecer las marcas de bits **msidbComponentAttributesSharedDllRefCount** o **msidbComponentAttributesPermanent** en la columna Atributos de la tabla de componentes msi Component Table para el componente que contiene el archivo de \_ \_ \_ fuente.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE07](ice07.md)  
[ICE32](ice32.md)  
[ICE51](ice51.md)  
[ICE60](ice60.md)  
</dl>

 

 



