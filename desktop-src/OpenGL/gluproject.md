---
title: función gluProject (GLU. h)
description: La función gluProject asigna coordenadas de objeto a las coordenadas de la ventana.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- gluProject (función) OpenGL
topic_type:
- apiref
api_name:
- gluProject
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84972d95d381a630bf6caf7f0099ce740a4f2741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491915"
---
# <a name="gluproject-function"></a>gluProject función)

La función **gluProject** asigna coordenadas de objeto a las coordenadas de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
int WINAPI gluProject(
         GLdouble objx,
         GLdouble objy,
         GLdouble objz,
   const GLdouble modelMatrix[16],
   const GLdouble projMatrix[16],
   const GLint    viewport[4],
         GLdouble *winx,
         GLdouble *winy,
         GLdouble *winz
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*objx* 
</dt> <dd>

Coordenada x del objeto.

</dd> <dt>

*objy* 
</dt> <dd>

Coordenada y del objeto.

</dd> <dt>

*objz* 
</dt> <dd>

Coordenada z del objeto.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

La matriz de MODELVIEW actual (a partir de una llamada a [**glGetDoublev**](glgetdoublev.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

La matriz de proyección actual (a partir de una llamada a **glGetDoublev** ).

</dd> <dt>

*encuadre* 
</dt> <dd>

La ventanilla actual (a partir de una llamada a [**glGetIntegerv**](glgetintegerv.md) ).

</dd> <dt>

*winx* 
</dt> <dd>

Coordenada x calculada de la ventana.

</dd> <dt>

*winy* 
</dt> <dd>

Coordenada y de la ventana calculada.

</dd> <dt>

*winz* 
</dt> <dd>

Coordenada de la ventana z calculada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es GL \_ true.

Si se produce un error en la función, el valor devuelto es GL \_ false.

## <a name="remarks"></a>Observaciones

La función **gluProject** transforma las coordenadas del objeto especificado en coordenadas de la ventana mediante *modelMatrix*, *projMatrix* y *viewport*. El resultado se almacena en *Winx*, *Winy* y *Winz*.

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

[**glGetDoublev**](glgetdoublev.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluUnProject**](gluunproject.md)
</dt> </dl>

 

 





