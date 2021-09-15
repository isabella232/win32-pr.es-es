---
title: Función glMateriali (Gl.h)
description: La funciónglMateriali especifica parámetros de material para el modelo de iluminación.
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
keywords:
- Función glMateriali OpenGL
topic_type:
- apiref
api_name:
- glMateriali
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc4f1bf6628f1674cf9c3534b9f0c9d028246d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271999"
---
# <a name="glmateriali-function"></a>Función glMateriali

La **función glMateriali** especifica parámetros de material para el modelo de iluminación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMateriali(
   GLenum face,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cara* 
</dt> <dd>

La cara o las caras que se están actualizando. Debe ser uno de los siguientes: GL \_ FRONT, GL \_ BACK o GL FRONT y GL \_ \_ BACK.

</dd> <dt>

*pname* 
</dt> <dd>

Parámetro de material con un solo valor de la cara o las caras que se están actualizando. Debe ser \_ GLCULEINESS.



| Value                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ GLINESS**</dt> </dl> | El *parámetro param* es un único entero que especifica el exponente especular RGBA del material. Los valores enteros se asignan directamente. Solo se aceptan los valores \[ del intervalo 0, 128. \] El exponente especular predeterminado para los materiales orientados hacia delante y hacia atrás es 0. <br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Valor en el que se establecerá el \_ parámetro GLZCAINESS.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>  | Face *o* *pname no* era un valor aceptado.<br/>                |
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl> | Se especificó un exponente especular fuera del \[ intervalo de 0, 128. \]<br/> |



## <a name="remarks"></a>Observaciones

La **función glMateriali** asigna valores a parámetros de material. Hay dos conjuntos coincidentes de parámetros de material. Uno,  el conjunto de orientación frontal, se usa para sombrear puntos, líneas, mapas de bits y todos los polígonos (cuando la iluminación de dos lados está deshabilitada) o simplemente los polígonos orientados al frente (cuando la iluminación de dos lados está habilitada). El otro conjunto, *orientado hacia atrás,* se usa para sombrear polígonos orientados hacia atrás solo cuando la iluminación de dos lados está habilitada. Consulte [**glLightModel para**](gllightmodel-functions.md) obtener más información sobre los cálculos de iluminación de uno y dos lados.

La **función glMateriali** toma tres argumentos. La primera, *face*, especifica si se modificarán los materiales GL \_ FRONT, GL \_ BACK o GL FRONT Y \_ \_ \_ BACK. El segundo, *pname*, especifica cuál de varios parámetros de uno o ambos conjuntos se modificará. El tercer *parámetro, param*, especifica qué valor se asignará al parámetro especificado.

Los parámetros de material se usan en la ecuación de iluminación que se aplica opcionalmente a cada vértice. La ecuación se describe en [**glLightModel**](gllightmodel-functions.md).

Los parámetros de material se pueden actualizar en cualquier momento. En concreto, se puede llamar a **glMateriali** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). Si solo se va a cambiar un parámetro de material por vértice, se prefiere [**glColorMaterial**](glcolormaterial.md) en lugar **de glMateriali.**

La función siguiente recupera información relacionada con **glMateriali**:

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





