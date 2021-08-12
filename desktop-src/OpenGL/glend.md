---
title: Función glEnd (Gl.h)
description: Las funciones glBegin y glBegin delimitan los vértices de una primitiva o un grupo de primitivas similares. | Función glEnd (Gl.h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- Función glEnd OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0817bec7874b9a3a58e28653ff10497eb1e3f5e5170c57dbe2c26a6b20b64460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616557"
---
# <a name="glend-function"></a>función glEnd

Las [**funciones glBegin y glBegin**](glbegin.md) **delimitan** los vértices de una primitiva o un grupo de primitivas similares.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Una función que no sea **glVertex,** **glColor,** **glIndex,** **glNormal,** **glTexCoord,** **glEvalCoord,** **glEvalPoint,** **glMaterial,** **glEdgeFlag,** **glCallList** o **glCallLists** se llamó entre **glBegin** y el **glEnd correspondiente.** Se **llamó a la** función glEnd antes de llamar a **la glBegin** correspondiente, o bien se llamó a **glBegin** dentro de una **secuencia glBegin** / **glEnd.** <br/> |



## <a name="remarks"></a>Observaciones

Las [**funciones glBegin y glBegin**](glbegin.md) **delimitan** los vértices que definen una primitiva o un grupo de primitivas similares. La **función glBegin** acepta un único argumento que especifica cuál de diez primitivos componen los vértices. Tomando *n* como número entero a partir de uno y *N* como número total de vértices especificados, las interpretaciones son las siguientes:

-   Solo puede usar un subconjunto de funciones de OpenGL entre **glBegin** y **glEnd.** Las funciones que puede usar son:

    -   [**glVertex**](glvertex-functions.md)
    -   [**glColor**](glcolor-functions.md)
    -   [**glIndex**](glindex-functions.md)
    -   [**glNormal**](glnormal-functions.md)
    -   [**glTexCoord**](gltexcoord-functions.md)
    -   [**glEvalCoord**](glevalcoord-functions.md)
    -   [**glEvalPoint**](glevalpoint.md)
    -   [**glMaterial**](glmaterial-functions.md)
    -   [**glEdgeFlag**](gledgeflag-functions.md)

    También puede usar [**glCallList o**](glcalllist.md) [**glCallLists**](glcalllists.md) para ejecutar listas para mostrar que incluyan solo las funciones anteriores. Si se llama a cualquier otra función OpenGL entre **glBegin** y **glEnd,** se establece la marca de error y se omite la función.

-   Independientemente del valor  elegido para el modo en **glBegin,** no hay ningún límite en el número de vértices que se pueden definir entre **glBegin** y **glEnd.** No se dibujan líneas, triángulos, cuadráteros y polígonos que están especificados de forma incompleta. Resultados de especificación incompletos cuando se proporcionan demasiados vértices para especificar incluso una sola primitiva o cuando se especifica un múltiplo incorrecto de vértices. Se omite la primitiva incompleta; se dibujan las primitivas completas.
-   La especificación mínima de vértices para cada primitivo es: 

    | Número mínimo de vértices | Tipo de primitiva |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | triangle          |
    | 4                          | Cuadrilátero     |
    | 3                          | polygon           |

    

     

-   Los modos que requieren un determinado múltiplo de vértices son GL \_ LINES (2), GL \_ TRIANGLES (3), GL \_ QUADS (4) y GL \_ QUAD STRIP \_ (2).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

