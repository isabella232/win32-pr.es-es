---
title: Función glGenLists (Gl.h)
description: La función glGenLists genera un conjunto contiguo de listas de visualización vacías.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- Función glGenLists OpenGL
topic_type:
- apiref
api_name:
- glGenLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a916b163f2ec04e51da06263aed0f76f5e4dd6b51b7eca9fdbca8965644fdd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360402"
---
# <a name="glgenlists-function"></a>Función glGenLists

La **función glGenLists** genera un conjunto contiguo de listas de visualización vacías.

## <a name="syntax"></a>Sintaxis


```C++
GLuint WINAPI glGenLists(
   GLsizei range
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*range* 
</dt> <dd>

Número de listas de visualización vacías contiguas que se generarán.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | *el intervalo* era negativo.<br/>                                                                                                      |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glGenLists** tiene un argumento, *range*. Devuelve un entero *n* de forma que el intervalo *de listas* de visualización vacías contiguas, *denominadas n*, *n* + 1, . . Se crean *., n* + (*intervalo* - 1). Si *range* es cero, si  no hay ningún grupo de nombres contiguos de intervalo disponibles o si se genera algún error, no se genera ninguna lista de visualización y se devuelve cero.

La función siguiente recupera información relacionada con **glGenLists**:

[**glIsList**](glislist.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





