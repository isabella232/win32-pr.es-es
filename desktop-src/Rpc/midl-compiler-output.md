---
title: Salida del compilador MIDL
description: Con los archivos IDL y ACF como entrada, el compilador midl genera hasta cinco archivos de código fuente en lenguaje C.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071416"
---
# <a name="midl-compiler-output"></a>Salida del compilador MIDL

Con los archivos IDL y ACF como entrada, el compilador midl genera hasta cinco archivos de código fuente en lenguaje C. De forma predeterminada, el compilador midl usa el nombre de archivo base del archivo IDL como parte de los archivos de código auxiliar generados. Cuando hay más de seis caracteres en el nombre de archivo base, es posible que algunos sistemas de archivos no acepten el nombre de código auxiliar completo. En la tabla siguiente se muestran las convenciones usadas para los nombres de archivo.



| Archivo        | Parte predeterminada del nombre de archivo base | Ejemplo      |
|-------------|-----------------------------------|--------------|
| Archivo IDL    | ---                               | Abcdefgh.idl |
| Encabezado      | .h                                | Abcdef.h     |
| Código auxiliar de cliente | \_c.c                             | Abcdef \_ c.c  |
| Código auxiliar del servidor | \_S.c                             | Abcdef \_ s.c  |



 

 

 




