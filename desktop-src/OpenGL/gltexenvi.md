---
title: Función glTexEnvi (Gl.h)
description: La función glTexEnvi establece un parámetro de entorno de textura.
ms.assetid: 3f4c10c4-524c-4cce-b42b-bc72fc3b9f31
keywords:
- Función glTexEnvi OpenGL
topic_type:
- apiref
api_name:
- glTexEnvi
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c013b0e4805042ed0967e02df83f143d8bcfd991
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074024"
---
# <a name="gltexenvi-function"></a>Función glTexEnvi

La **función glTexEnvi** establece un parámetro de entorno de textura.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexEnvi(
   GLenum target,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Un entorno de textura. Debe ser GL \_ TEXTURE \_ ENV.

</dd> <dt>

*pname* 
</dt> <dd>

Nombre simbólico de un parámetro de entorno de textura con un solo valor. Debe ser GL \_ TEXTURE \_ ENV \_ MODE.

</dd> <dt>

*param* 
</dt> <dd>

Una única constante simbólica, una de \_ GLMODULTE, GL \_ DECAL, GL \_ BLEND o GL \_ REPLACE.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *target* o *pname* no era uno de los valores definidos aceptados, o cuando *los parámetros* deberían haber tenido un valor constante definido (basado en el valor de *pname)* y no lo hizo.<br/> |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>                                             |



## <a name="remarks"></a>Observaciones

Un entorno de textura especifica cómo se interpretan los valores de textura cuando se textura un fragmento. El *parámetro de* destino debe ser GL TEXTURE \_ \_ ENV. El *parámetro pname* es GL \_ TEXTURE \_ ENV \_ MODE. Se definen tres funciones de textura: \_ GLMODULTE, GL \_ DECAL y GL \_ BLEND.

Una función de textura actúa sobre el fragmento que se va a texturar mediante el valor de imagen de textura que se aplica al fragmento (vea [**glTexParameter)**](gltexparameter-functions.md)y genera un color RGBA para ese fragmento. En la tabla siguiente se muestra cómo se genera el color RGBA para cada una de las tres funciones de textura que se pueden elegir. *C* es un triple de valores de color (RGB) y *A* es el valor alfa asociado. Los valores RGBA extraídos de una imagen de textura se encuentran en el \[ intervalo 0, 1 \] . El subíndice *f* hace referencia al fragmento entrante, el subíndice *t* a la imagen de textura, el subíndice *c* al color del entorno de textura y el subíndice *v* indica un valor generado por la función de textura.

Una imagen de textura puede tener hasta cuatro componentes por elemento de textura (vea [**glTexImage1D**](glteximage1d.md) y [**glTexImage2D).**](glteximage2d.md) En una imagen de un componente, Lt indica ese componente único. ¿Una imagen de dos componentes usa *L?*  y *A?* . ¿Una imagen de tres componentes solo tiene un valor de color, *C?* . ¿Una imagen de cuatro componentes tiene un valor de color *C?*  y un valor alfa *A?* .



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
<td rowspan="2">1${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>¿L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">2${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>¿L?</em> <em>C<sub>f</sub></em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>(1</em> - <em>L?</em> <em>)C<sub>f</sub> </em> + <em>L?</em> <em>C<sub>c</sub></em></td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">3${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>¿C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em>  =  <em>¿C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em> </td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
<tr class="odd">
<td rowspan="2">4${REMOVE}$<br />
</td>
<td><em>C<sub>v</sub> </em>  =  <em>¿C?</em> <em>C<sub>f</sub></em></td>
<td><em>C<sub>v</sub> </em> = (1 - <em>A?</em> <em>)C<sub>f</sub> </em> + <em>A?</em> <em>¿C?</em></td>
<td rowspan="2">undefined${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td><em>A<sub>v</sub> </em>  =  <em>¿A?</em> <em>A<sub>f</sub></em> </td>
<td><em>A<sub>v</sub> </em>  =  <em>A<sub>f</sub> </em></td>


</tr>
</tbody>
</table>



 

El \_ valor predeterminado del modo GL TEXTURE \_ ENV es \_ \_ GLMODULTE.

La función siguiente recupera información relacionada con **glTexEnvi**:

[**glTexGetEnviv**](glgettexenviv.md)

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





