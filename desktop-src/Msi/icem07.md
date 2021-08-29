---
description: ICEM07 comprueba que el orden de los archivos de la tabla de secuencia coincide con el orden de los archivos MergeModule.CABconjunto de inet.
ms.assetid: 5778e0c5-2f8d-4562-9c93-d6f6890a74e9
title: ICEM07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef29ffc26658660e9acd09ba108779bf6902d1d0326963765f13b29c99b845ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894525"
---
# <a name="icem07"></a>ICEM07

ICEM07 comprueba que el orden de los archivos de la tabla de secuencia coincide con el orden de los archivos [MergeModule.CABconjunto de inet](mergemodule-cabinet.md).

Los ICE del módulo de mezcla se almacenan en un archivo .uu. del módulo de mezcla denominado Mergemod.pack y no en el archivo .uu. que contiene los ICE usados para la validación del paquete.

## <a name="result"></a>Resultado

ICEM07 publica un error si el orden de los archivos de la tabla File no coincide con el orden del archivo de archivador.

## <a name="example"></a>Ejemplo

IC0M07 publicaría el siguiente mensaje de error para el ejemplo mostrado.

``` syntax
The file 'FileB.GUID1' appears to be out of sequence. It has position 3 
in the CAB, but not when the file table is ordered by sequence number.
```

[Tabla de archivos](file-table.md)



| Archivo          | Secuencia |
|---------------|----------|
| ArchivoA. *GUID1* | 1        |
| FileB. *GUID1* | 8        |
| FileC. *GUID1* | 52       |



 

Conjunto [MergeModule.CABintegrado](mergemodule-cabinet.md)



| Archivo          |
|---------------|
| ArchivoA. *GUID1* |
| FileC. *GUID1* |
| Presentado. *GUID1* |
| FileB. *GUID1* |



 

Aunque los números de secuencia de archivo de la tabla de archivos no tienen que ser consecutivos y pueden existir archivos adicionales en el archivo archivador, la secuencia relativa de todos los archivos de la tabla File debe coincidir con el orden de [MergeModule.CABinet](mergemodule-cabinet.md). Para corregir este error, cambie el número de secuencia de FileB que va a ir después de FileC para que coincida con el orden de los archivos en cab o vuelva a generar la CAB con los archivos en el orden correcto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



