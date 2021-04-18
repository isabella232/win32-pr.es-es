---
title: función gluUnProject (GLU. h)
description: La función gluUnProject asigna las coordenadas de la ventana a las coordenadas del objeto.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- gluUnProject (función) OpenGL
topic_type:
- apiref
api_name:
- gluUnProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f45311171dd3d71c9e699953c049e0813f2df361
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686194"
---
# <a name="gluunproject-function"></a>gluUnProject función)

La función **gluUnProject** asigna las coordenadas de la ventana a las coordenadas del objeto.

## <a name="syntax"></a>Sintaxis


```C++
int WINAPI gluUnProject(
         GLdouble winx,
         GLdouble winy,
         GLdouble winz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *objx,
         GLdouble *objy,
         GLdouble *objz
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*winx* 
</dt> <dd>

Coordenada x de la ventana que se va a asignar.

</dd> <dt>

*winy* 
</dt> <dd>

Coordenada de la ventana y que se va a asignar.

</dd> <dt>

*winz* 
</dt> <dd>

Coordenada de la ventana de z que se va a asignar.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

La matriz MODELVIEW (a partir de una llamada a [**glGetDoublev**](glgetdoublev.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

La matriz de proyección (a partir de una llamada a **glGetDoublev** ).

</dd> <dt>

*encuadre* 
</dt> <dd>

La ventanilla (a partir de una llamada a [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).

</dd> <dt>

*objx* 
</dt> <dd>

Coordenada x del objeto calculado.

</dd> <dt>

*objy* 
</dt> <dd>

Coordenada y del objeto calculado.

</dd> <dt>

*objz* 
</dt> <dd>

Coordenada z calculada del objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es GL \_ true.

Si se produce un error en la función, el valor devuelto es GL \_ false.

## <a name="remarks"></a>Observaciones

La función **gluUnProject** asigna las coordenadas de ventana especificadas a coordenadas de objeto mediante *modelMatrix*, *projMatrix* y *viewport*. El resultado se almacena en *objx*, *objy* y *objz*.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetDoublev**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluProject**](gluproject.md)
</dt> </dl>

 

 





