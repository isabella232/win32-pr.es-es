---
title: función gluGetString (GLU. h)
description: La función gluGetString obtiene una cadena que describe el número de versión GLU o las llamadas de extensión GLU compatibles.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- gluGetString (función) OpenGL
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
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422214"
---
# <a name="glugetstring-function"></a>gluGetString función)

La función **gluGetString** obtiene una cadena que describe el número de versión Glu o las llamadas de extensión Glu compatibles.

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

El número de versión de GLU (versión de GLU \_ ) o las llamadas de extensión específicas del proveedor disponibles (extensiones de Glu \_ ).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función **gluGetString** devuelve un puntero a una cadena estática terminada en NULL. Cuando el *nombre* es Glu \_ version, la cadena devuelta es un valor que representa el número de versión de Glu. El formato del número de versión es el siguiente:

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

El número de versión tiene el formato " \_ número principal. \_ número secundario" o " \_ número principal. \_ número secundario. número de versión \_ ". La información específica del proveedor es opcional y el formato y el contenido dependen de la implementación.

Cuando *Name* es Glu \_ extensions, la cadena devuelta contiene una lista de nombres de las extensiones de Glu admitidas que están separadas por espacios. El formato de la lista de nombres devuelto es el siguiente:

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

Los nombres de extensión no pueden contener espacios.

La función **gluGetString** es válida para la versión 1,1 de Glu o posterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



 

 





