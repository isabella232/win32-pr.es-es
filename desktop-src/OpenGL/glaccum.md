---
title: Función glAccum (Gl.h)
description: La función glAccum funciona en el búfer de acumulación.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- Función glAccum OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0820d27bf6aff05916eb179e4dfd0b51a0746e2c6e5a6f4e5f3bdfe8f3e6d91a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082265"
---
# <a name="glaccum-function"></a>función glAccum

La **función glAccum** funciona en el búfer de acumulación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*op* 
</dt> <dd>

Operación de búfer de acumulación. Las constantes simbólicas aceptadas son las siguientes.



| Value                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <dt>**GL \_ ACCUM**</dt> </dl>    | Obtiene los valores R, G, B y A del búfer seleccionado actualmente para lectura [**(consulte glReadBuffer**](glreadbuffer.md)). Cada valor de componente se divide entre 2 *n*  1, donde *n* es el número de bits asignados a cada componente de color en el búfer seleccionado actualmente. El resultado es un valor de punto flotante en el intervalo 0,1 , que se multiplica por valor y se agrega al componente de píxel correspondiente en el búfer de acumulación, actualizando así el búfer de \[ \] acumulación. <br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <dt>**CARGA \_ DE GL**</dt> </dl>       | Similar a GL ACCUM, salvo que el valor actual del búfer de acumulación no se usa en el \_ cálculo del nuevo valor. Es decir, los valores R, G, B y A del búfer seleccionado actualmente se dividen entre 2 *n* 1, se multiplican por valor y, a continuación, se almacenan en la celda de búfer de acumulación correspondiente, sobrescribiendo el valor actual.<br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <dt>**GL \_ ADD**</dt> </dl>          | Agrega *valor* a cada R, G, B y A en el búfer de acumulación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <dt>**GL \_ MULT**</dt> </dl>       | Multiplica cada R, G, B y A  en el búfer de acumulación por valor y devuelve el componente escalado a su ubicación de búfer de acumulación correspondiente.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <dt>**GL \_ RETURN**</dt> </dl> | Transfiere los valores del búfer de acumulación al búfer de color o a los búferes seleccionados actualmente para escritura. Cada componente R, G, B y A se multiplica por valor *y,* a continuación, se multiplica por 2 *n*  1, se fija en el intervalo \[ 0, 2 *n*  1 y se almacena en la celda de búfer para mostrar \] correspondiente. Las únicas operaciones de fragmentos que se aplican a esta transferencia son la propiedad de píxeles, el relleno, el dithering y las máscaras de escritura de color.<br/>                                                                        |



 

</dd> <dt>

*value* 
</dt> <dd>

Valor de punto flotante utilizado en la operación de búfer de acumulación. El *parámetro op* determina cómo se *usa* value.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *op* no era un valor aceptado.<br/>                                                                                                                                            |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | No había ningún búfer de acumulación o se llamó a la función **glAccum** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

El búfer de acumulación es un búfer de color de intervalo extendido. Las imágenes no se representan en él. En su lugar, las imágenes que se representan en uno de los búferes de color se agregan al contenido del búfer de acumulación después de la representación. Puede crear efectos como suavizado de contorno (de puntos, líneas y polígonos), desenfoque de movimiento y profundidad de campo mediante la acumulación de imágenes generadas con matrices de transformación diferentes.

Cada píxel del búfer de acumulación consta de valores rojo, verde, azul y alfa. El número de bits por componente en el búfer de acumulación depende de la implementación. Puede examinar este número llamando a [**glGetIntegerv**](glgetintegerv.md) cuatro veces, con los argumentos GL \_ ACCUM \_ RED \_ BITS, GL \_ ACCUM \_ GREEN BITS, GL ACCUM BLUE BITS y GL \_ \_ \_ \_ \_ ACCUM ALPHA \_ \_ BITS, respectivamente. Sin embargo, independientemente del número de bits por componente, el intervalo de valores almacenados por cada componente es \[ 1,?1 \] . Los píxeles del búfer de acumulación se asignan uno a uno con píxeles de búfer de fotogramas.

La **función glAccum** funciona en el búfer de acumulación. El primer argumento, *op*, es una constante simbólica que selecciona una operación de búfer de acumulación. El segundo argumento, *value*, es un valor de punto flotante que se usará en esa operación. Se especifican cinco operaciones: GL \_ ACCUM, GL \_ LOAD, GL \_ ADD, GL \_ MULT y GL \_ RETURN.

Todas las operaciones de búfer de acumulación están limitadas al área del cuadro de resarro actual y se aplican de forma idéntica a los componentes rojo, verde, azul y alfa de cada píxel. El contenido de un componente de píxeles de búfer de acumulación no está definido si la operación **glAccum** da como resultado un valor fuera del \[ intervalo de 1,1 \] .

Para borrar el búfer de acumulación, use la función [**glClearAccum**](glclearaccum.md) para especificar los valores R, G, B y A para establecerlo en y emita una función [**glClear**](glclear.md) con el búfer de acumulación habilitado.

Todas las operaciones **glAccum** solo actualizan esos píxeles dentro del cuadro de resaciente actual.

Las siguientes funciones recuperan información relacionada con **la función glAccum:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ GL ACCUM \_ RED \_ BITS

**glGet** con el argumento \_ GL ACCUM \_ GREEN \_ BITS

**glGet** con el argumento \_ GL ACCUM \_ BLUE \_ BITS

**glGet** con el argumento \_ GL ACCUM \_ ALPHA \_ BITS

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClear**](glclear.md)
</dt> <dt>

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadBuffer**](glreadbuffer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





