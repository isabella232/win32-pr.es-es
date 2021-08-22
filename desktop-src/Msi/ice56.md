---
description: ICE56 valida que la estructura de directorios del archivo .msi tiene un único directorio raíz, que la raíz es la propiedad TARGETDIR y que el valor de la propiedad SourceDir está en la columna DefaultDir de la tabla Directory.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c1feb3e3dbab84a58809496b28a60d3a2436c3041d3a2d58f0ac8f2b5e47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528226"
---
# <a name="ice56"></a>ICE56

ICE56 valida que la estructura de directorios del archivo .msi tiene un único directorio raíz, que la raíz es la propiedad [**TARGETDIR**](targetdir.md) y que el valor de la propiedad [**SourceDir**](sourcedir.md) está en la columna DefaultDir de la tabla [Directory](directory-table.md).

Si un .msi tiene varias raíces o especifica una raíz distinta [](administrative-installation.md) de [**TARGETDIR**](targetdir.md), una instalación administrativa no crea una imagen administrativa correcta.

Tenga en cuenta que ICE56 no comprueba los directorios vacíos. La estructura de directorios pasa la validación con varios directorios raíz si los directorios adicionales están vacíos.

## <a name="result"></a>Resultado

ICE56 muestra un error si el .msi no tiene una sola raíz, [**TARGETDIR**](targetdir.md)o si [**SourceDir**](sourcedir.md) no se especifica en la columna DefaultDir de la tabla [Directory](directory-table.md).

## <a name="example"></a>Ejemplo

ICE56 notifica los siguientes errores para el ejemplo mostrado.

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[Tabla de directorios](directory-table.md)



| Directorio | Elemento primario \_ del directorio | DefaultDir |
|-----------|-------------------|------------|
| TARGETDIR |                   | Temp       |
| Root2     | Root2             | SourceDir  |



 

Para corregir el primer error, la raíz [**de TARGETDIR**](targetdir.md) debe tener un valor DefaultDir [**de SourceDir**](sourcedir.md). También se acepta SOURCEDIR. Es posible convertir **TARGETDIR** en el elemento primario de la segunda raíz y usar el valor "." en la columna DefaultDir. Consulte la [tabla Directorio para](directory-table.md) obtener más información.

Para corregir el segundo error, la estructura Directory solo debe tener una raíz denominada [**TARGETDIR.**](targetdir.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



