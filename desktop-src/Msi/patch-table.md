---
description: La tabla patch especifica el archivo que va a recibir una revisión determinada y la ubicación física de los archivos de revisión en las imágenes multimedia.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Tabla de revisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061b2082f88a8c7c3967652900bb6bf6e1c29802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818558"
---
# <a name="patch-table"></a>Tabla de revisión

La tabla patch especifica el archivo que va a recibir una revisión determinada y la ubicación física de los archivos de revisión en las imágenes multimedia.

La tabla patch tiene las columnas siguientes.



| Columna      | Tipo                               | Clave | Nullable |
|-------------|------------------------------------|-----|----------|
| Archivo\_      | [Identificador](identifier.md)       | Y   | N        |
| Secuencia    | [Entero](integer.md)             | Y   | N        |
| PatchSize   | [DoubleInteger](doubleinteger.md) | N   | N        |
| Atributos  | [Entero](integer.md)             | N   | N        |
| Encabezado      | [Binario](binary.md)               | N   | Y        |
| StreamRef\_ | [Identificador](identifier.md)       | N   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_
</dt> <dd>

La revisión se aplica al archivo especificado por el identificador en esta columna. Se trata de una clave principal para la tabla y es una clave externa de la [tabla de archivos](file-table.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>SPRJ
</dt> <dd>

Esta es la posición del archivo de revisión en el orden de secuencia de archivos en las imágenes multimedia. El orden de secuencia debe corresponder al orden de los archivos en el archivo contenedor del paquete de revisión. Esta es una clave principal de esta tabla. El límite máximo es de 32767 archivos, para crear un paquete de Windows Installer con más archivos, consulte crear [un paquete de gran tamaño](authoring-a-large-package.md).

</dd> <dt>

<span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize
</dt> <dd>

Esta columna proporciona el tamaño de la revisión en bytes escritos como un entero largo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Sus
</dt> <dd>

Entero que contiene los marcadores de bits que representan los atributos de la revisión. Inserte un valor de 1 en esta columna para indicar que no se ha producido un error grave al aplicar esta revisión.



| Constante                         | Hexadecimal | Decimal | Descripción                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| (ninguno)                           | 0x000       | 0       | Un error grave no se pudo aplicar a esta revisión.                        |
| **msidbPatchAttributesNonVital** | 0x001       | 1       | Indica que no se ha producido un error grave al aplicar esta revisión. |



 

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Encabezado
</dt> <dd>

Esta columna es el encabezado de revisión de la secuencia binaria que se utiliza para la validación de revisiones. Esta columna debe ser null si la \_ columna StreamRef no es NULL. En este caso, la secuencia de encabezado Patch se almacena en la [tabla MsiPatchHeaders](msipatchheaders-table.md) para superar la limitación de nombre de flujo descrita en [limitaciones OLE en las secuencias](ole-limitations-on-streams.md).

</dd> <dt>

<span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_
</dt> <dd>

Clave externa en la tabla MsiPatchHeaders que especifica la fila que contiene la secuencia de encabezado patch.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [acción PatchFiles](patchfiles-action.md)procesa esta tabla. Normalmente se agrega al paquete de instalación mediante una transformación de un paquete de revisión. Normalmente no se crea directamente en un paquete de instalación.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE45](ice45.md)  
</dl>

 

 



