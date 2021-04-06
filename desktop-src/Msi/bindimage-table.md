---
description: La tabla BindImage contiene información sobre cada archivo ejecutable o DLL que debe estar enlazado a los archivos dll importados por él.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: Tabla BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001716"
---
# <a name="bindimage-table"></a>Tabla BindImage

La tabla BindImage contiene información sobre cada archivo ejecutable o DLL que debe estar enlazado a los archivos dll importados por él.

La tabla BindImage tiene las columnas siguientes.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Archivo\_ | [Identificador](identifier.md) | Y   | N        |
| Ruta   | [Paths](paths.md)           | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_
</dt> <dd>

Una clave externa para la columna uno de la [tabla de archivos](file-table.md). Debe ser un archivo ejecutable o un archivo DLL.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Camino
</dt> <dd>

Una lista de rutas de acceso, separadas por punto y coma, que representan las rutas de acceso en las que se van a buscar los archivos dll importados. La lista suele ser una lista de propiedades, con cada propiedad entre corchetes ( \[ \] ).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El instalador calcula la dirección virtual de cada una de las funciones que se importan desde todos los archivos dll, y la dirección virtual calculada se guarda en la tabla de direcciones de importación (IAT) de la imagen de importación.

Se hace referencia a esta tabla cuando se ejecuta la [acción BindImage](bindimage-action.md) .

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE76](ice76.md)  
</dl>

 

 



