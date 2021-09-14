---
description: La tabla MsiFileHash se usa para almacenar un hash de 128 bits de un archivo de origen proporcionado por el paquete Windows Installer. El hash se divide en cuatro valores de 32 bits y se almacena en columnas independientes de la tabla.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Tabla MsiFileHash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86acb299e5d7f099a8d49affc64810d128e88369
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071854"
---
# <a name="msifilehash-table"></a>Tabla MsiFileHash

La **tabla MsiFileHash** se usa para almacenar un hash de 128 bits de un archivo de origen proporcionado por el paquete Windows Installer. El hash se divide en cuatro valores de 32 bits y se almacena en columnas independientes de la tabla.

Windows El instalador puede usar el hash de archivos como medio para detectar y eliminar copias de archivos innecesarias. Un hash de archivo almacenado en la tabla **MsiFileHash** se puede comparar con un hash de un archivo existente en el equipo del usuario obtenido mediante una llamada a [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha). La **tabla MsiFileHash** solo se puede usar con archivos sin versión.

La **tabla MsiFileHash** tiene las columnas siguientes.



| Columna    | Tipo                               | Clave | Nullable |
|-----------|------------------------------------|-----|----------|
| Archivo\_    | [Identificador](identifier.md)       | Y   | N        |
| Opciones   | [Entero](integer.md)             | N   | N        |
| HashPart1 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart2 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart3 | [DoubleInteger](doubleinteger.md) | N   | N        |
| Hashpart4 | [DoubleInteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Archivo\_
</dt> <dd>

Clave externa a [la tabla de archivos](file-table.md). Cadena de 72 caracteres.

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Opciones
</dt> <dd>

Esta columna debe ser 0 y está reservada para su uso futuro.

</dd> <dt>

<span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1
</dt> <dd>

Primeros 32 bits de hash. El hash de archivo especificado en este campo debe obtenerse mediante una llamada a [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o [**al método FileHash**](installer-filehash.md). No use otros métodos.

</dd> <dt>

<span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2
</dt> <dd>

Segundo 32 bits de hash. El hash de archivo especificado en este campo debe obtenerse mediante una llamada a [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o [**al método FileHash**](installer-filehash.md). No use otros métodos hash.

</dd> <dt>

<span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3
</dt> <dd>

Tercer 32 bits de hash. El hash de archivo especificado en este campo debe obtenerse mediante una llamada a [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o [**al método FileHash**](installer-filehash.md). No use otros métodos.

</dd> <dt>

<span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4
</dt> <dd>

Cuarto 32 bits de hash. El hash de archivo especificado en este campo debe obtenerse mediante una llamada a [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) o [**al método FileHash**](installer-filehash.md). No use otros métodos.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE60](ice60.md)  
[ICE66](ice66.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[Control de versiones de archivo predeterminado](default-file-versioning.md)
</dt> </dl>

 

 



