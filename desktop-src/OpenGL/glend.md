---
title: función glEnd (GL. h)
description: Las funciones glBegin y glend delimitan los vértices de un primitivo o un grupo de primitivos similares. | función glEnd (GL. h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- glEnd (función) OpenGL
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
ms.openlocfilehash: d9bb41395b3ed2e38a64094506e07e2a69ad1d52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670135"
---
# <a name="glend-function"></a>glEnd función)

Las funciones [**glBegin**](glbegin.md) y **glend** delimitan los vértices de un primitivo o un grupo de primitivos similares.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a una función que no sea **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **GlEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList** o **glCallLists** entre **glBegin** y el **glEnd** correspondiente. Se llamó a la función **glEnd** antes de que se llamara al **glBegin** correspondiente, o bien se llamó a **glBegin** dentro de una secuencia **glBegin** / **glEnd** . <br/> |



## <a name="remarks"></a>Observaciones

Las funciones [**glBegin**](glbegin.md) y **glend** delimitan los vértices que definen un primitivo o un grupo de primitivos similares. La función **glBegin** acepta un solo argumento que especifica los diez primitivos que componen los vértices. Tomando *n* como un recuento entero a partir de uno, y *n* como el número total de vértices especificado, las interpretaciones son las siguientes:

-   Solo se puede usar un subconjunto de funciones de OpenGL entre **glBegin** y **glEnd**. Las funciones que puede usar son:

    -   [**glVertex**](glvertex-functions.md)
    -   [**glColor**](glcolor-functions.md)
    -   [**glIndex**](glindex-functions.md)
    -   [**glNormal**](glnormal-functions.md)
    -   [**glTexCoord**](gltexcoord-functions.md)
    -   [**glEvalCoord**](glevalcoord-functions.md)
    -   [**glEvalPoint**](glevalpoint.md)
    -   [**glMaterial**](glmaterial-functions.md)
    -   [**glEdgeFlag**](gledgeflag-functions.md)

    También puede usar [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) para ejecutar listas de presentación que incluyen solo las funciones anteriores. Si se llama a cualquier otra función de OpenGL entre **glBegin** y **glEnd**, se establece la marca de error y se omite la función.

-   Independientemente del valor elegido para el *modo* en **glBegin**, no hay ningún límite en el número de vértices que puede definir entre **glBegin** y **glEnd**. No se dibujan líneas, triángulos, quadrilaterals ni polígonos que se hayan especificado de una vez incompleta. Resultados de especificación incompletos cuando se proporcionan muy pocos vértices para especificar incluso un único primitivo o cuando se especifica un múltiplo incorrecto de vértices. Se omite el primitivo incompleto; se dibujan los primitivos completos.
-   La especificación mínima de los vértices para cada primitiva es: 

    | Número mínimo de vértices | Tipo de primitivo |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | triangle          |
    | 4                          | cuadrangular     |
    | 3                          | polygon           |

    

     

-   Los modos que requieren un determinado múltiplo de vértices son \_ las líneas de libro de contabilidad (2), los \_ triángulos de contabilidad (3), los \_ cuatro cuádruples (4) y la \_ franja cuádruple de GL \_ (2).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
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

 

