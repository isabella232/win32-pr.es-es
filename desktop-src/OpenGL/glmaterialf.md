---
title: función glMaterialf (GL. h)
description: La función glMaterialf especifica los parámetros de material para el modelo de iluminación.
ms.assetid: c6d183c4-2d1f-4fb9-b24f-c132ebfc708d
keywords:
- glMaterialf (función) OpenGL
topic_type:
- apiref
api_name:
- glMaterialf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c77cb1be5595f4a872988bbc6480d4cd6f65aae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686216"
---
# <a name="glmaterialf-function"></a>glMaterialf función)

La función **glMaterialf** especifica los parámetros de material para el modelo de iluminación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glMaterialf(
   GLenum  face,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Portada* 
</dt> <dd>

La cara o caras que se están actualizando. Debe ser uno de los siguientes: GL \_ Front, GL \_ back o GL \_ Front y GL \_ back.

</dd> <dt>

*PName* 
</dt> <dd>

Parámetro de material de valor único de la cara o caras que se están actualizando. Debe ser brillo de contabilidad \_ .



| Value                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**brillo de GL \_**</dt> </dl> | El parámetro *param* es un valor de punto flotante único que especifica el exponente especular RGBA del material. Los valores enteros se asignan directamente. Solo se aceptan los valores del intervalo comprendido entre \[ 0 y 128 \] . El exponente especular predeterminado para el material orientado hacia delante y hacia atrás es 0. <br/> |



 

</dd> <dt>

*param* 
</dt> <dd>

Valor al que se establecerá el parámetro de brillo de contabilidad \_ .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                              | Significado                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>  | Cualquiera de las *caras* o *PName* no era un valor aceptado.<br/>                |
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl> | Se especificó un exponente especular fuera del intervalo de \[ 0, 128 \] .<br/> |



## <a name="remarks"></a>Observaciones

La función **glMaterialf** asigna valores a los parámetros de material. Hay dos conjuntos de parámetros de material coincidentes. Uno, el conjunto *frontal* , se usa para sombrear puntos, líneas, mapas de bits y todos los polígonos (cuando está deshabilitada la iluminación dos caras) o simplemente polígonos frontales (cuando está habilitada la iluminación de dos caras). El otro conjunto, *orientado hacia atrás*, se usa para sombrear polígonos de cara a la inversa solo cuando está habilitada la iluminación de dos caras. Consulte [**glLightModel**](gllightmodel-functions.md) para obtener más información sobre los cálculos de iluminación de una cara y dos caras.

La función **glMaterialf** toma tres argumentos. La primera, *cara*, especifica si se modificarán los materiales de la contabilidad general \_ , los materiales traseros de la contabilidad general o los materiales de la \_ \_ parte delantera y trasera del libro de contabilidad \_ \_ . La segunda, *PName*, especifica cuál de los diversos parámetros de uno o ambos conjuntos se modificarán. El *tercer parámetro especifica* el valor que se asignará al parámetro especificado.

Los parámetros de material se usan en la ecuación de iluminación que se aplica opcionalmente a cada vértice. La ecuación se describe en [**glLightModel**](gllightmodel-functions.md).

Los parámetros de material se pueden actualizar en cualquier momento. En concreto, se puede llamar a **glMaterialf** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md). Sin embargo, si solo se va a cambiar un parámetro de material por vértice, se prefiere [**glColorMaterial**](glcolormaterial.md) a **glMaterialf**.

La siguiente función recupera información relacionada con **glMaterialf**:

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





