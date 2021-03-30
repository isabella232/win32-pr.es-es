---
description: ICEM07 comprueba que el orden de los archivos de la tabla de secuencia coincide con el orden de los archivos en MergeModule.CABinet.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696d5c92671c3a8347cb43714d43e646a3e14f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910385"
---
# <a name="icem07"></a>ICEM07

ICEM07 comprueba que el orden de los archivos de la tabla de secuencia coincide con el orden de los archivos en [MergeModule.CABinet](mergemodule-cabinet.md).

El módulo de combinación ICEs se almacena en un archivo. Cub de módulo de combinación denominado Mergemod. Cub y no en el archivo. Cub que contiene el ICEs usado para la validación del paquete.

## <a name="result"></a>Resultado

ICEM07 publica un error si el orden de los archivos de la tabla de archivos no coincide con el orden del archivo. cab.

## <a name="example"></a>Ejemplo

IC0M07 publicaría el mensaje de error siguiente para el ejemplo mostrado.

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[Tabla de archivos](file-table.md)



| Archivo          | Secuencia |
|---------------|----------|
| Archivoa. *GUID1* | 1        |
| FileB. *GUID1* | 8        |
| FileC. *GUID1* | 52       |



 

Embedded [MergeModule.CABinet](mergemodule-cabinet.md)



| Archivo          |
|---------------|
| Archivoa. *GUID1* |
| FileC. *GUID1* |
| Registrado. *GUID1* |
| FileB. *GUID1* |



 

Aunque los números de secuencia de archivos de la tabla de archivos no tienen que ser consecutivos, y los archivos adicionales pueden existir en el archivo. cab, la secuencia relativa de todos los archivos de la tabla de archivos debe coincidir con el orden en [MergeModule.CABinet](mergemodule-cabinet.md). Para corregir este error, cambie el número de secuencia de FileB para que aparezca después de FileC para que coincida con el orden de los archivos en el archivo. CAB o vuelva a generar el archivo. CAB con los archivos en el orden correcto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de módulo de combinación ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



