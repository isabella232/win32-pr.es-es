---
title: función glFrontFace (GL. h)
description: La función glFrontFace define polígonos orientados delante y detrás.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- glFrontFace (función) OpenGL
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
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997083"
---
# <a name="glfrontface-function"></a>glFrontFace función)

La función **glFrontFace** define polígonos orientados delante y detrás.

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

Orientación de los polígonos orientados hacia delante. \_Se aceptan GL CW y contabilidad \_ CCW. El valor predeterminado es el \_ CCW de contabilidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *modo* no era un valor aceptado.<br/>                                                                                          |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

En una escena compuesta por completo de superficies cerradas opacas, los polígonos hacia delante nunca están visibles. La eliminación de estos polígonos invisibles tiene la ventaja obvia de acelerar la representación de la imagen. Puede habilitar y deshabilitar la eliminación de polígonos orientados al fondo con [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) mediante el argumento de la cara de selección de libro de contabilidad \_ \_ .

Se dice que la proyección de un polígono a coordenadas de la ventana tiene un bobinado en el sentido de las agujas del reloj si un objeto imaginario que sigue a la ruta de acceso desde su primer vértice, su segundo vértice, etc., al último vértice y, finalmente, de nuevo al primer vértice, se mueve en sentido de las agujas del reloj sobre el interior del polígono. Se dice que el bobinado del polígono está en sentido contrario a las agujas del reloj si el objeto imaginario que sigue a la misma ruta de acceso se mueve en sentido contrario a las agujas del reloj sobre el interior del polígono. La función **glFrontFace** especifica si polígonos con el bobinado en el sentido de las agujas del reloj en las coordenadas de la ventana o el bobinado en sentido contrario a las agujas del reloj en coordenadas de la ventana. Al pasar \_ el CCW de contabilidad al *modo* , se seleccionan los polígonos en sentido contrario a las agujas del reloj como anverso; GL \_ CW selecciona los polígonos en el sentido de las agujas del reloj como frontal. De forma predeterminada, los polígonos en sentido contrario a las agujas del reloj se toman delante.

La siguiente función recupera información sobre **glFrontface**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ cara frontal de libro de contabilidad \_

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

 

 





