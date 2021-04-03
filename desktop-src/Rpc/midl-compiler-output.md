---
title: Salida del compilador MIDL
description: Con los archivos IDL y ACF como entrada, el compilador MIDL genera hasta cinco archivos de origen en lenguaje C.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075356"
---
# <a name="midl-compiler-output"></a>Salida del compilador MIDL

Con los archivos IDL y ACF como entrada, el compilador MIDL genera hasta cinco archivos de origen en lenguaje C. De forma predeterminada, el compilador MIDL usa el nombre de archivo base del archivo IDL como parte de los archivos de código auxiliar generados. Si hay más de seis caracteres en el nombre de archivo base, es posible que algunos sistemas de archivos no acepten el nombre completo del código auxiliar. En la tabla siguiente se muestran las convenciones que se usan para los nombres de archivo.



| Archivo        | Parte predeterminada del nombre del archivo base | Ejemplo      |
|-------------|-----------------------------------|--------------|
| Archivo IDL    | ---                               | Abcdefgh. idl |
| Encabezado      | .h                                | Abcdef. h     |
| Código auxiliar de cliente | \_c. c                             | Abcdef \_ c. c  |
| Código auxiliar de servidor | \_s. c                             | Abcdef \_ s. c  |



 

 

 




