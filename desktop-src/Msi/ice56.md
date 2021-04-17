---
description: ICE56 valida que la estructura de directorios del archivo. msi tiene un único directorio raíz, que la raíz es la propiedad TARGETDIR y que el valor de la propiedad SourceDir está en la columna DefaultDir de la tabla de directorio.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0b83dc20c8463b80375d325dd9225de8524742
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668129"
---
# <a name="ice56"></a>ICE56

ICE56 valida que la estructura de directorios del archivo. msi tiene un único directorio raíz, que la raíz es la propiedad [**targetDir**](targetdir.md) y que el valor de la propiedad [**SourceDir**](sourcedir.md) está en la columna DefaultDir de la [tabla de directorio](directory-table.md).

Si un archivo. msi tiene varias raíces o especifica una raíz distinta de [**targetDir**](targetdir.md), una [instalación administrativa](administrative-installation.md) no crea una imagen administrativa correcta.

Tenga en cuenta que los directorios vacíos no se comprueban con ICE56. La estructura de directorios pasa la validación con varios directorios raíz si los directorios adicionales están vacíos.

## <a name="result"></a>Resultado

ICE56 publica un error si el archivo. msi no tiene una sola raíz, [**targetDir**](targetdir.md)o si [**SourceDir**](sourcedir.md) no se especifica en la columna DefaultDir de la [tabla de directorio](directory-table.md).

## <a name="example"></a>Ejemplo

ICE56 notifica los siguientes errores para el ejemplo que se muestra.

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[Tabla de directorio](directory-table.md)



| Directorio | Directorio \_ primario | DefaultDir |
|-----------|-------------------|------------|
| TARGETDIR |                   | Temp       |
| Root2     | Root2             | SourceDir  |



 

Para corregir el primer error, la raíz de [**targetDir**](targetdir.md) debe tener un valor de DefaultDir de [**SourceDir**](sourcedir.md). También se acepta SOURCEDIR. Puede convertir el **targetDir** en el elemento primario de la segunda raíz y usar el valor '. ' en la columna DefaultDir. Vea la [tabla de directorios](directory-table.md) para obtener más información.

Para corregir el segundo error, la estructura de directorios solo debe tener una raíz denominada [**targetDir**](targetdir.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



