---
title: Extraer los ejemplos de código
description: Aunque los ejemplos de código están divididos en una serie de lecciones del tutorial, las agrupaciones de ejemplo adecuadas se pueden extraer fácilmente de la colección.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a593cf36b2fa235813c291eb35307153b28a2aa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418569"
---
# <a name="extracting-the-code-samples"></a>Extraer los ejemplos de código

Aunque los ejemplos de código están divididos en una serie de lecciones del tutorial, las agrupaciones de ejemplo adecuadas se pueden extraer fácilmente de la colección. La mayoría de los directorios de ejemplo individuales están diseñados para funcionar junto con al menos otro directorio de ejemplo. Los ejemplos relacionados con los componentes se componen de un par de cliente y servidor, con el servidor que requiere el uso de la utilidad de ejemplo REGISTER. A continuación se muestra un resumen de las agrupaciones de ejemplo y cómo extraer cada grupo como una unidad que se pueda compilar. Para cada agrupación de ejemplo, copie el contenido de los directorios mostrados. El \[ \] Directorio de destino primario que se muestra no requiere contenido de la rama samples. Sin embargo, los menús de ayuda de los ejemplos en ejecución suponen que se trata del tutorial adecuado. Los archivos de ayuda HTM se encuentran en este \[ Directorio de destino primario \] .

Para la aplicación READTUT de Win32:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

Para la aplicación esqueleto de Win32 EXE:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    EXESKEL
```

Para el esqueleto del archivo DLL de Win32:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    DLLSKEL
    DLLUSER
```

Para los ejemplos de objetos COM básicos:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    COMOBJ
    COMUSER
```

Para los ejemplos de cliente/servidor de componentes DLL básicos en proceso:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

Para los ejemplos de cliente/servidor de componente con licencia:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    LICSERVE
    LICCLIEN
```

Para los ejemplos de serialización estándar:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    MARSHAL2
```

Para los ejemplos de cliente/servidor locales fuera de proceso:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    LOCSERVE
    LOCCLIEN
```

Para los ejemplos de cliente/servidor de modelo de apartamento:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    APTCLIEN
```

Para los ejemplos de cliente/servidor DCOM (COM distribuido):

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    MARSHAL
    APTSERVE
    REMCLIEN
```

Para los ejemplos de cliente/servidor de subprocesamiento libre:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

Para los ejemplos de cliente/servidor de objetos COM conectables:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    CONSERVE
    CONCLIEN
```

Para los ejemplos de cliente/servidor de almacenamiento estructurado:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    STOSERVE
    STOCLIEN
```

Para los ejemplos de cliente/servidor de objeto persistente:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    PERSERVE
    PERTEXT
    PERDRAW
    PERCLIEN
```

Para los ejemplos de cliente/servidor de seguridad de DCOM:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DCDMARSH
    DCDSERVE
    DCOMDRAW
```

 

 




