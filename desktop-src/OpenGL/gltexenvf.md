---
title: función glTexEnvf (GL. h)
description: La función glTexEnvf establece un parámetro de entorno de textura.
ms.assetid: 1b203240-a963-4dfe-96bc-735720e16122
keywords:
- glTexEnvf (función) OpenGL
topic_type:
- apiref
api_name:
- glTexEnvf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1566378b6dcd2f91a2e2cd445f0ec39c0f6f6a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801994"
---
# <a name="gltexenvf-function"></a>glTexEnvf función)

La función **glTexEnvf** establece un parámetro de entorno de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexEnvf(
   GLenum  target,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Entorno de textura. Debe ser un \_ \_ env Texture.

</dd> <dt>

*PName* 
</dt> <dd>

El nombre simbólico de un parámetro de entorno de textura de un solo valor. Debe ser el modo de textura de libro de contabilidad \_ \_ \_ .

</dd> <dt>

*param* 
</dt> <dd>

Una sola constante simbólica, una de GL \_ modulada, GL \_ Decal, GL \_ Blend o el reemplazo de contabilidad \_ .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino* o *PName* no era uno de los valores definidos aceptados o cuando los *parámetros* deberían tener un valor constante definido (basado en el valor de *PName*) y no lo hacían.<br/> |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>                                             |



## <a name="remarks"></a>Observaciones

Un entorno de textura especifica cómo se interpretan los valores de textura cuando se textura un fragmento. El parámetro de *destino* debe ser de \_ textura GL \_ env. El parámetro *PName* es el modo de textura del libro de contabilidad \_ \_ \_ . Se definen tres funciones de textura: libro de contabilidad general \_ , \_ Decal y GL \_ Blend.

Una función de textura actúa en el fragmento que se va a texturar mediante el valor de la imagen de textura que se aplica al fragmento (vea [**glTexParameter**](gltexparameter-functions.md)) y genera un color RGBA para ese fragmento. En la tabla siguiente se muestra cómo se genera el color RGBA para cada una de las tres funciones de textura que se pueden elegir. *C* es un triple de valores de color (RGB) *y es* el valor alfa asociado. Los valores RGBA extraídos de una imagen de textura están en el intervalo de \[ 0 a 1 \] . El subíndice *f* hace referencia al fragmento entrante, el subíndice *t* a la imagen de textura, el subíndice *c* al color del entorno de textura y el subíndice *v* indica un valor generado por la función de textura.

Una imagen de textura puede tener hasta cuatro componentes por elemento de textura (vea [**glTexImage1D**](glteximage1d.md) y [**glTexImage2D**](glteximage2d.md)). En una imagen de un componente, lt indica que se trata de un único componente. Una imagen de dos componentes usa *L?*  y *a?* . Una imagen de tres componentes solo tiene un valor de color, *C?* . Una imagen de cuatro componentes tiene un valor de color *C?*  y un valor alfa *a?* .



<table>
<thead>
<tr class="header">
<th>Número de componentes</th>
<th>GL_MODULATE</th>
<th>GL_DECAL</th>
<th>GL_BLEND</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2">1 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>¿L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">$ {REMOVE} $ sin definir<br />
</td>
<td><em>C</em> <em><sub>v</sub></em>  =  <em>(1</em> - <em>L?</em> <em>) C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>¿L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">$ {REMOVE} $ sin definir<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>) C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em></td>
<td rowspan="2">$ {REMOVE} $ sin definir<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em> </td>
<td><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4 $ {REMOVE} $<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1- <em>a?</em> <em>) C<sub>f</sub> </em> + <em>A?</em> <em>Unidad?</em></td>
<td rowspan="2">$ {REMOVE} $ sin definir<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>R?</em> <em><sub>F</sub></em> </td>
<td><em>A<sub>v</sub> </em>  =  <em><sub>F</sub> </em></td>


</tr>
</tbody>
</table>



 

\_De forma predeterminada, la textura de GL del \_ \_ modo env es el \_ modular GL.

La siguiente función recupera información relacionada con **glTexEnvf**:

[**glTexGetEnvfv**](glgettexenvfv.md)

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





