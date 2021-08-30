---
title: Función gluGetString (Glu.h)
description: La función gluGetString obtiene una cadena que describe el número de versión de GLU o las llamadas de extensión GLU admitidas.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- Función gluGetString OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a39dca7e03f934a67e2e6d80545e92d16e9a9d852e70405f24e2e089fc5559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777645"
---
# <a name="glugetstring-function"></a>Función gluGetString

La **función gluGetString** obtiene una cadena que describe el número de versión de GLU o las llamadas de extensión GLU admitidas.

## <a name="syntax"></a>Sintaxis


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*name* 
</dt> <dd>

El número de versión de GLU (VERSIÓN \_ DE GLU) o las llamadas de extensión específicas del proveedor disponibles \_ (EXTENSIONES DE GLU).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **función gluGetString** devuelve un puntero a una cadena estática terminada en NULL. Cuando *name* es GLU \_ VERSION, la cadena devuelta es un valor que representa el número de versión de GLU. El formato del número de versión es el siguiente:

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

El número de versión tiene el formato "número \_ principal.número \_ menor" o "número \_ principal.número \_ menor.número de \_ versión". La información específica del proveedor es opcional y el formato y el contenido dependen de la implementación.

Cuando *name* es GLU EXTENSIONS, la cadena devuelta contiene una lista de nombres de extensiones \_ GLU admitidas separadas por espacios. El formato de la lista de nombres devuelta es el siguiente:

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

Los nombres de extensión no pueden contener espacios.

La **función gluGetString** es válida para GLU versión 1.1 o posterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



 

 





