---
title: Función glFrontFace (Gl.h)
description: La función glFrontFace define polígonos orientados hacia delante y hacia atrás.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- Función glFrontFace OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d288b4e6380ab845af9a05381963444e28ddf50739ecd3f5563d9f2dc729fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580165"
---
# <a name="glfrontface-function"></a>función glFrontFace

La **función glFrontFace** define polígonos orientados hacia delante y hacia atrás.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Orientación de los polígonos orientados al frente. Se \_ aceptan GL CW y GL \_ CCW. El valor predeterminado es GL \_ CCW.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *el modo* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

En una escena compuesta completamente de superficies opacas cerradas, los polígonos orientados hacia atrás nunca son visibles. La eliminación de estos polígonos invisibles tiene la ventaja obvia de acelerar la representación de la imagen. Habilite y deshabilite la eliminación de polígonos orientados hacia atrás con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) mediante el argumento GL \_ CULL \_ FACE.

Se dice que la proyección de un polígono a las coordenadas de ventana tiene una sinuoso en el sentido de las agujas del reloj si un objeto imaginario que sigue el trazado desde su primer vértice, su segundo vértice, y así sucesivamente, hasta su último vértice y, por último, hacia su primer vértice, se mueve en dirección en el sentido de las agujas del reloj sobre el interior del polígono. Se dice que la sinuoso del polígono es en sentido contrario a las agujas del reloj si el objeto imaginario que sigue el mismo trazado se mueve en una dirección en sentido contrario a las agujas del reloj sobre el interior del polígono. La **función glFrontFace** especifica si los polígonos con deserción en el sentido de las agujas del reloj en coordenadas de ventana, o en las coordenadas de ventana, se toman para que estén orientados hacia delante. Pasar CCW de GL al modo selecciona polígonos en sentido contrario a las agujas del \_ reloj como orientados hacia delante;  GL CW selecciona polígonos en el sentido de las \_ agujas del reloj como orientados hacia delante. De forma predeterminada, se toman polígonos en sentido contrario a las agujas del reloj para que estén orientados hacia delante.

La función siguiente recupera información sobre **glFrontface**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ FRONT \_ FACE

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





