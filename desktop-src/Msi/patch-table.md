---
description: La tabla Patch especifica el archivo que va a recibir una revisión determinada y la ubicación física de los archivos de revisión en las imágenes multimedia.
ms.assetid: 1b624702-de25-4b1a-9dac-21f359ee97f7
title: Tabla de revisiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061b2082f88a8c7c3967652900bb6bf6e1c29802
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173673"
---
# <a name="patch-table"></a>Tabla de revisiones

La tabla Patch especifica el archivo que va a recibir una revisión determinada y la ubicación física de los archivos de revisión en las imágenes multimedia.

La tabla Patch tiene las columnas siguientes.



| Columna      | Tipo                               | Clave | Nullable |
|-------------|------------------------------------|-----|----------|
| Archivo\_      | [Identificador](identifier.md)       | Y   | No        |
| Secuencia    | [Entero](integer.md)             | Y   | No        |
| PatchSize   | [DoubleInteger](doubleinteger.md) | No   | No        |
| Atributos  | [Entero](integer.md)             | No   | No        |
| Encabezado      | [Binario](binary.md)               | No   | Y        |
| StreamRef\_ | [Identificador](identifier.md)       | No   | Y        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Archivo\_
</dt> <dd>

La revisión se aplica al archivo especificado por el identificador de esta columna. Se trata de una clave principal para la tabla y es una clave externa para la [tabla File](file-table.md).

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Secuencia
</dt> <dd>

Esta es la posición del archivo de revisión en el orden de secuencia de los archivos en las imágenes multimedia. El orden de secuencia debe corresponder al orden de los archivos del archivo de archivador del paquete de revisión. Se trata de una clave principal para esta tabla. El límite máximo es de 32767 archivos. Para crear un paquete de Windows Installer con más archivos, consulte Creación de [un paquete grande.](authoring-a-large-package.md)

</dd> <dt>

<span id="PatchSize"></span><span id="patchsize"></span><span id="PATCHSIZE"></span>PatchSize
</dt> <dd>

Esta columna proporciona el tamaño de la revisión en bytes escritos como un entero largo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Entero que contiene marcas de bits que representan atributos de revisión. Inserte un valor de 1 en esta columna para indicar que el error al aplicar esta revisión no es un error irresal.



| Constante                         | Hexadecimal | Decimal | Descripción                                                          |
|----------------------------------|-------------|---------|----------------------------------------------------------------------|
| (ninguno)                           | 0x000       | 0       | Si no se aplica esta revisión, es un error irresal.                        |
| **msidbPatchAttributesNonVital** | 0x001       | 1       | Indica que el error al aplicar esta revisión no es un error grave. |



 

</dd> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>Rúbrica
</dt> <dd>

Esta columna es el encabezado de revisión de flujo binario usado para la validación de revisiones. Esta columna debe ser NULL si la columna StreamRef \_ no es NULL. En este caso, el flujo de encabezado de revisión se almacena en la tabla [MsiPatchHeaders](msipatchheaders-table.md) para superar la limitación de nombre de flujo descrita en [Limitaciones](ole-limitations-on-streams.md)ole Secuencias .

</dd> <dt>

<span id="StreamRef_"></span><span id="streamref_"></span><span id="STREAMREF_"></span>StreamRef\_
</dt> <dd>

Clave externa en la tabla MsiPatchHeaders que especifica la fila que contiene el flujo de encabezado de revisión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta tabla se procesa mediante la [acción PatchFiles](patchfiles-action.md). Normalmente se agrega al paquete de instalación mediante una transformación de un paquete de revisión. Normalmente no se ha escrito directamente en un paquete de instalación.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE45](ice45.md)  
</dl>

 

 



