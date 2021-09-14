---
title: Función glLineStipple (Gl.h)
description: La función glLineStipple especifica el patrón detippla de línea.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- Función glLineStipple OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253808"
---
# <a name="gllinestipple-function"></a>Función glLineStipple

La **función glLineStipple** especifica el patrón detippla de línea.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Factor* 
</dt> <dd>

Multiplicador para cada bit del patrón detippla de línea. Si *el factor* es 3, por ejemplo, cada bit del patrón se usará tres veces antes de que se utilice el siguiente bit del patrón. El parámetro de *factor* se fija en el intervalo \[ 1, 256 y el \] valor predeterminado es uno.

</dd> <dt>

*pattern* 
</dt> <dd>

Entero de 16 bits cuyo patrón de bits determina qué fragmentos de una línea se dibujarán cuando se rasteriza la línea. El bit cero se usa primero y el patrón predeterminado son todos los.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glLineStipple** especifica el patrón detippla de línea. El enmascaramiento de líneas enmascara determinados fragmentos generados por la rasterización; esos fragmentos no se dibujarán. El enmascaramiento se logra mediante tres parámetros: el patrón detippla de línea de 16 bits *,* el *factor* de recuento de repeticiones y un contador detippla *de enteros.*

Los *contadores se* restablecen a cero cada vez que se llama a [**glBegin**](glbegin.md) y antes de que se genere cada segmento de línea de una **secuencia glBegin**(GL \_ LINES)/glEnd. Se incrementa después de generar cada fragmento de un segmento de línea con alias de ancho de unidad, o después de generar cada *fragmento de i* de un segmento de línea de ancho de *i.* Los *fragmentos de i* asociados a count *s* se enmascaran si *el* bit de patrón (*s*  /  *factor*) mod 16 es cero. De lo contrario, estos fragmentos se envían al búfer de fotogramas. El bit cero *del patrón* es el bit menos significativo.

Las líneas con suavizado de contorno se tratan como una secuencia de rectángulos de ancho 1x con el fin de paralizar. Los *rectángulos se* rasterizan o no se basan en la regla de fragmento descrita para las líneas con alias; cuenta rectángulos en lugar de grupos de fragmentos.

El contrabando de líneas está habilitado o deshabilitado mediante [**glEnable**](glenable.md) y **glDisable** con el argumento GL \_ LINE \_ STIPPLE. Cuando se habilita, el patrón detippla de línea se aplica como se ha descrito anteriormente. Cuando se deshabilita, es como si el patrón fuera todos. Inicialmente, el contrabando de líneas está deshabilitado.

Las siguientes funciones recuperan información relacionada **con glLineStipple**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ LINE \_ \_ STIPPLE PATTERN

**glGet con** el argumento GL \_ LINE \_ STIPPLE \_ REPEAT

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ LINE \_ STIPPLE

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[**glEnd**](glend.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





