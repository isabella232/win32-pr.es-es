---
title: función glHint (GL. h)
description: La función glHint especifica sugerencias específicas de la implementación.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- glHint (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150052"
---
# <a name="glhint-function"></a>glHint función)

La función **glHint** especifica sugerencias específicas de la implementación.

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
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <dt>**\_sugerencia de niebla de GL \_**</dt> </dl>                                                           | Indica la precisión del cálculo de niebla. Si el cálculo de la niebla por píxel no se admite de forma eficaz en la implementación de OpenGL, la sugerencia de libro de contabilidad no se tiene \_ \_ en cuenta o la \_ más rápida puede dar lugar a un cálculo por vértices de los efectos de niebla.<br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <dt>**\_sugerencia de \_ suavizado de línea de contabilidad \_**</dt> </dl>                                  | Indica la calidad de muestreo de las líneas con suavizado de contorno. \_La sugerencia de libro de contabilidad puede dar lugar a que se generen más fragmentos de píxeles durante la rasterización, si se aplica una función de filtro más grande.<br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <dt>**\_sugerencia de \_ corrección de perspectiva de GL \_**</dt> </dl> | Indica la calidad de la interpolación de coordenadas de color y textura. Si la implementación de OpenGL no admite la interpolación de parámetros corregidos por perspectiva de forma eficaz, la sugerencia del libro de contabilidad no se tiene \_ \_ en cuenta o la \_ más rápida puede producir una interpolación lineal simple de colores y/o coordenadas de textura.<br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <dt>**\_ \_ sugerencia Smooth de punto de contabilidad \_**</dt> </dl>                               | Indica la calidad de muestreo de los puntos antialias. \_La sugerencia de libro de contabilidad puede dar lugar a que se generen más fragmentos de píxeles durante la rasterización, si se aplica una función de filtro más grande.<br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <dt>**\_ \_ sugerencia Smooth de polígono de GL \_**</dt> </dl>                         | Indica la calidad de muestreo de los polígonos con suavizado de contorno. \_La sugerencia de libro de contabilidad puede dar lugar a que se generen más fragmentos de píxeles durante la rasterización, si se aplica una función de filtro más grande.<br/>                                                                                                            |



 

</dd> <dt>

*mode* 
</dt> <dd>

Constante simbólica que indica el comportamiento deseado. Se aceptan las siguientes constantes simbólicas.



| Value                                                                                                                                                       | Significado                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <dt>**GL \_ más rápido**</dt> </dl>        | Se debe elegir la opción más eficaz.<br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <dt>**libro \_ de contabilidad**</dt> </dl>           | Se debe elegir la opción más adecuada o de mayor calidad.<br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <dt>**no importa el libro de contabilidad \_ \_**</dt> </dl> | El cliente no tiene ninguna preferencia.<br/>                          |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *destino* o el *modo* no era un valor aceptado.<br/>                                                                              |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Cuando hay espacio para la interpretación, puede controlar ciertos aspectos del comportamiento de OpenGL con sugerencias. Especifique una sugerencia con dos argumentos. El parámetro de *destino* es una constante simbólica que indica el comportamiento que se va a controlar y el *modo* es otra constante simbólica que indica el comportamiento deseado.

Aunque los aspectos de implementación que se pueden sugerir están bien definidos, la interpretación de las sugerencias depende de la implementación.

La función **glHint** se puede omitir.

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
</dt> </dl>

 

 





