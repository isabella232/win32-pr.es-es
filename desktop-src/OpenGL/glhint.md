---
title: Función glHint (Gl.h)
description: La función glHint especifica sugerencias específicas de la implementación.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- Función glHint OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260135"
---
# <a name="glhint-function"></a>Función glHint

La **función glHint** especifica sugerencias específicas de la implementación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Destino* 
</dt> <dd>

Constante simbólica que indica el comportamiento que se va a controlar. Se aceptan las siguientes constantes simbólicas, junto con la semántica sugerida.



| Value                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <dt>**SUGERENCIA \_ GL GL \_ GL**</dt> </dl>                                                           | Indica la precisión del cálculo de los cálculos de los cálculos. Si el cálculo de píxeles por píxel no es compatible de forma eficaz con la implementación de OpenGL, las sugerencias GL DONT CARE o GL FASTEST pueden dar lugar a un cálculo por vértice de efectos \_ de efecto en el \_ \_ vértice.<br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <dt>**GL \_ LINE \_ SMOOTH \_ HINT**</dt> </dl>                                  | Indica la calidad de muestreo de las líneas suavizadas. Las sugerencias DE GL NICEST pueden dar lugar a que se generen más fragmentos de píxeles durante la rasterización, si se aplica una función \_ de filtro mayor.<br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <dt>**SUGERENCIA DE \_ \_ CORRECCIÓN DE PERSPECTIVA \_ DE GL**</dt> </dl> | Indica la calidad de la interpolación de coordenadas de color y textura. Si la implementación de OpenGL no admite eficazmente la interpolación de parámetros con corrección de perspectiva, las sugerencias DE GL DONT CARE o GL FASTEST pueden dar lugar a una interpolación lineal simple de colores o coordenadas de \_ \_ \_ textura.<br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <dt>**GL \_ POINT \_ SMOOTH \_ HINT**</dt> </dl>                               | Indica la calidad de muestreo de los puntos suavizados. Las sugerencias DE GL NICEST pueden dar lugar a que se generen más fragmentos de píxeles durante la rasterización, si se aplica una función \_ de filtro mayor.<br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <dt>**GL \_ POLYGON \_ SMOOTH \_ HINT**</dt> </dl>                         | Indica la calidad de muestreo de los polígonos suavizados. Las sugerencias DE GL NICEST pueden dar lugar a que se generen más fragmentos de píxeles durante la rasterización, si se aplica una función \_ de filtro mayor.<br/>                                                                                                            |



 

</dd> <dt>

*mode* 
</dt> <dd>

Constante simbólica que indica el comportamiento deseado. Se aceptan las siguientes constantes simbólicas.



| Value                                                                                                                                                       | Significado                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <dt>**GL \_ FASTEST**</dt> </dl>        | Se debe elegir la opción más eficaz.<br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <dt>**GL \_ NICEST**</dt> </dl>           | Se debe elegir la opción más correcta o de mayor calidad.<br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <dt>**GL \_ DONT \_ CARE**</dt> </dl> | El cliente no tiene ninguna preferencia.<br/>                          |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *target* o *mode* no era un valor aceptado.<br/>                                                                              |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Cuando hay espacio para la interpretación, puede controlar ciertos aspectos del comportamiento de OpenGL con sugerencias. Especifique una sugerencia con dos argumentos. El *parámetro* de destino es una constante simbólica que indica el comportamiento que se va a controlar y *el* modo es otra constante simbólica que indica el comportamiento deseado.

Aunque los aspectos de implementación que se pueden dar están bien definidos, la interpretación de las sugerencias depende de la implementación.

La **función glHint** se puede omitir.

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
</dt> </dl>

 

 





