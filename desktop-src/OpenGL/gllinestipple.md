---
title: función glLineStipple (GL. h)
description: La función glLineStipple especifica el patrón punteado de línea.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- glLineStipple (función) OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b47202b25c0779a3daa0bd801900b1d29e0b37b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800998"
---
# <a name="gllinestipple-function"></a>glLineStipple función)

La función **glLineStipple** especifica el patrón punteado de línea.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*diez* 
</dt> <dd>

Un multiplicador para cada bit en el patrón punteado de línea. Si *factor* es 3, por ejemplo, cada bit del patrón se usará tres veces antes de que se use el siguiente bit del patrón. El parámetro *factor* se fija en el intervalo \[ 1, 256 y el \] valor predeterminado es uno.

</dd> <dt>

*pattern* 
</dt> <dd>

Entero de 16 bits cuyo modelo de bits determina qué fragmentos de una línea se dibujarán cuando se rasteriza la línea. Primero se usa el bit cero y el patrón predeterminado es todos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glLineStipple** especifica el patrón punteado de línea. El punteado de línea oculta determinados fragmentos producidos por la rasterización; esos fragmentos no se dibujarán. El enmascaramiento se consigue con tres parámetros: el *patrón* de patrón punteado de línea de 16 bits, el *factor* de recuento de repetición y un contador de entero punteado *s*.

Counter *s* se restablece a cero cada vez que se llama a [**glBegin**](glbegin.md) y antes de que se genere cada segmento de línea de una secuencia de **glBegin**(líneas de contabilidad \_ )/**glEnd** . Se incrementa después de que se genere cada fragmento de un segmento de línea con alias de ancho de unidad, o después de que se generen todos los fragmentos *i* de un segmento de línea *i* width. Los fragmentos *i* asociados a los *recuentos* se enmascaran si el bit de *patrón* (*s*  /  *factor*) mod 16 es cero. De lo contrario, estos fragmentos se envían a fotogramas. El bit cero del *patrón* es el bit menos significativo.

Las líneas con suavizado de contorno se tratan como una secuencia de 1x rectángulos de *ancho* para los fines de este. Rectangle *s* se rasteriza o no se basa en la regla de fragmento descrita para las líneas con alias; cuenta los rectángulos en lugar de los grupos de fragmentos.

El punteado de líneas está habilitado o deshabilitado mediante [**glEnable**](glenable.md) y **glDisable** con el argumento de línea de contabilidad \_ \_ punteada. Cuando está habilitado, el patrón punteado de línea se aplica como se describió anteriormente. Cuando está deshabilitado, es como si el patrón fuera todo. Inicialmente, la línea punteada está deshabilitada.

Las siguientes funciones recuperan información relacionada con **glLineStipple**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ \_ patrón punteado de línea de contabilidad de argumento \_

**glGet** con argumento de \_ línea de contabilidad \_ punteada \_

[**glIsEnabled**](glisenabled.md) con el argumento \_ línea de contabilidad \_ punteada

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





