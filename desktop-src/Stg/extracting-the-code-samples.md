---
title: Extracción de los ejemplos de código
description: Aunque los ejemplos de código se dividen en una serie de lecciones de tutorial, las agrupaciones de ejemplo adecuadas se pueden extraer fácilmente de la colección.
ms.assetid: f8e20e40-cfef-4844-8b28-5a11fdcd691a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67093f4cfbbfab2a3c1681462627f02b504124ed15d1483b9f9d91ec5551d0e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034955"
---
# <a name="extracting-the-code-samples"></a>Extracción de los ejemplos de código

Aunque los ejemplos de código se dividen en una serie de lecciones de tutorial, las agrupaciones de ejemplo adecuadas se pueden extraer fácilmente de la colección. La mayoría de los directorios de ejemplo individuales están diseñados para funcionar junto con al menos otro directorio de ejemplo. Los ejemplos relacionados con componentes constan de un par de cliente y servidor, con el servidor que requiere el uso de la utilidad de ejemplo REGISTER. Este es un resumen de las agrupaciones de ejemplo y cómo extraer cada grupo como una unidad que se puede compilar. Para cada agrupación de ejemplo, copie el contenido de los directorios mostrados. El directorio \[ de destino primario que se muestra no requiere ningún contenido de la rama de \] ejemplos. Sin embargo, los menús de ayuda de los ejemplos en ejecución suponen que el tutorial adecuado .HTM archivos de ayuda se encuentran en este directorio \[ de destino \] primario.

Para la aplicación ReadTUT de Win32:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    READTUT
```

Para la aplicación de esqueleto de Win32 EXE:

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

Para los ejemplos básicos de cliente y servidor de componentes DLL en proceso:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    DLLSERVE
    DLLCLIEN
```

Para los ejemplos de cliente/servidor del componente con licencia:

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

Para los ejemplos de cliente/servidor local fuera de proceso:

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

Para los ejemplos de cliente y servidor del modelo de apartamento:

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

Para los ejemplos de cliente y servidor DCOM (COM distribuido):

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

Para obtener los ejemplos gratuitos de cliente o servidor de subprocesos:

``` syntax
[destination]
    APPUTIL
    INC
    LIB
    REGISTER
    FRESERVE
    FRECLIEN
```

Para los ejemplos de cliente o servidor de objetos COM conectables:

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

Para los ejemplos de cliente/servidor de objetos persistentes:

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

Para los ejemplos de cliente o servidor de seguridad DCOM:

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

 

 




