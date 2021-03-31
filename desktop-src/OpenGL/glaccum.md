---
title: función glAccum (GL. h)
description: La función glAccum funciona en el búfer de acumulación.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- glAccum (función) OpenGL
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
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802611"
---
# <a name="glaccum-function"></a>glAccum función)

La función **glAccum** funciona en el búfer de acumulación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*operador* 
</dt> <dd>

Operación de búfer de acumulación. Las constantes simbólicas aceptadas son las siguientes.



| Value                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <dt>**LIBRO \_ acumulado**</dt> </dl>    | Obtiene R, G, B y un valor del búfer seleccionado actualmente para lectura (vea [**glReadBuffer**](glreadbuffer.md)). Cada valor de componente se divide por 2 *n*  1, donde *n* es el número de bits asignados a cada componente de color en el búfer seleccionado actualmente. El resultado es un valor de punto flotante en el intervalo de \[ 0, 1 \] , que se multiplica por *valor* y se agrega al componente de píxel correspondiente en el búfer de acumulación, con lo que se actualiza el búfer de acumulación.<br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <dt>**carga en contab. \_**</dt> </dl>       | Similar a GL \_ acumulado, salvo que el valor actual en el búfer de acumulación no se utiliza en el cálculo del nuevo valor. Es decir, los valores R, G, B y a del búfer seleccionado actualmente se dividen entre 2 *n*  1, multiplicado por *valor* y, a continuación, se almacenan en la celda del búfer de acumulación correspondiente, sobrescribiendo el valor actual.<br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <dt>**\_Agregar GL**</dt> </dl>          | Agrega *valor* a cada R, G, B y a en el búfer de acumulación.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <dt>**\_mult**</dt> </dl>       | Multiplica cada R, G, B y A en el búfer de acumulación por *valor* y devuelve el componente escalado a su ubicación de búfer de acumulación correspondiente.<br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <dt>**devolución de GL \_**</dt> </dl> | Transfiere los valores del búfer de acumulación al búfer de color o a los búferes seleccionados actualmente para escritura. Cada R, G, B y un componente se multiplica por *valor* y, a continuación, se multiplica por 2 *n*  1, se fija al rango \[ 0, 2 *n*  1 \] y se almacena en la celda del búfer de presentación correspondiente. Las únicas operaciones de fragmento que se aplican a esta transferencia son la propiedad de píxeles, las tijeras, la interpolación y el color writemasks.<br/>                                                                        |



 

</dd> <dt>

*value* 
</dt> <dd>

Un valor de punto flotante que se usa en la operación de búfer de acumulación. El parámetro *OP* determina cómo se usa *Value* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *OP* no era un valor aceptado.<br/>                                                                                                                                            |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | No había ningún búfer de acumulación o se llamó a la función **glAccum** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

El búfer de acumulación es un búfer de color de intervalo extendido. Las imágenes no se representan en ella. En su lugar, las imágenes representadas en uno de los búferes de color se agregan al contenido del búfer de acumulación después de la representación. Puede crear efectos como el suavizado de contorno (de puntos, líneas y polígonos), el desenfoque de movimiento y la profundidad de campo mediante la acumulación de las imágenes generadas con matrices de transformación diferentes.

Cada píxel del búfer de acumulación consta de valores rojo, verde, azul y alfa. El número de bits por componente en el búfer de acumulación depende de la implementación. Puede examinar este número llamando a [**glGetIntegerv**](glgetintegerv.md) cuatro veces, con los argumentos los bits de color rojo acumulados en la contabilidad, los bits verdes de la acumulación de contabilidad, los bits azules acumulados en el libro de contabilidad \_ y los \_ \_ \_ \_ \_ \_ \_ \_ \_ bits alfa acumulados en el libro superior \_ \_ , respectivamente. Sin embargo, independientemente del número de bits por componente, el intervalo de valores almacenados por cada componente es \[ 1,? 1 \] . Los píxeles del búfer de acumulación se asignan uno a uno con fotogramas píxeles.

La función **glAccum** funciona en el búfer de acumulación. El primer argumento, *OP*, es una constante simbólica que selecciona una operación de búfer de acumulación. El segundo argumento, *Value*, es un valor de punto flotante que se va a usar en esa operación. Se especifican cinco operaciones: \_ Amort, GL \_ upload, GL \_ Add, GL \_ MULT y GL \_ Return.

Todas las operaciones de búfer de acumulación se limitan al área del cuadro de tijeras actual y se aplican de forma idéntica a los componentes rojo, verde, azul y alfa de cada píxel. El contenido de un componente de píxel del búfer de acumulación no está definido si la operación **glAccum** da como resultado un valor fuera del intervalo de \[ 1 a 1 \] .

Para borrar el búfer de acumulación, utilice la función [**glClearAccum**](glclearaccum.md) para especificar R, G, B y un valor para establecerlo en, y emita una función [**glClear**](glclear.md) con el búfer de acumulación habilitado.

Los píxeles que se encuentren en el cuadro tijeras actuales se actualizarán con cualquier operación de **glAccum** .

Las siguientes funciones recuperan información relacionada con la función **glAccum** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ bytes rojos acumulados por el libro de contabilidad \_

**glGet** con el argumento \_ los \_ \_ bits verdes del libro de contabilidad

**glGet** con los \_ \_ bits azules acumulados en el libro de contabilidad \_

**glGet** con el argumento \_ \_ bytes alfa acumulados en el libro de contabilidad \_

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

 

 





