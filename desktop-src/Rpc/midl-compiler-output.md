---
title: Salida del compilador MIDL
description: Con los archivos IDL y ACF como entrada, el compilador MIDL genera hasta cinco archivos de código fuente del lenguaje C.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aea74b77d8e709d8a71d3c84f457d301bb38d8c35bdccaa77e9e3033d08ed70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019695"
---
# <a name="midl-compiler-output"></a>Salida del compilador MIDL

Con los archivos IDL y ACF como entrada, el compilador MIDL genera hasta cinco archivos de código fuente del lenguaje C. De forma predeterminada, el compilador MIDL usa el nombre de archivo base del archivo IDL como parte de los archivos de código auxiliar generados. Cuando hay más de seis caracteres en el nombre de archivo base, es posible que algunos sistemas de archivos no acepten el nombre de código auxiliar completo. En la tabla siguiente se muestran las convenciones usadas para los nombres de archivo.



| Archivo        | Parte predeterminada del nombre de archivo base | Ejemplo      |
|-------------|-----------------------------------|--------------|
| Archivo IDL    | ---                               | Abcdefgh.idl |
| Header      | .h                                | Abcdef.h     |
| Código auxiliar de cliente | \_c.c                             | Abcdef \_ c.c  |
| Código auxiliar del servidor | \_S.c                             | Abcdef \_ s.c  |



 

 

 




