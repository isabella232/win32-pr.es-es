---
title: Función gluProject (Glu.h)
description: La función gluProject asigna coordenadas de objeto a coordenadas de ventana.
ms.assetid: cfd8bc5b-b684-4207-8bdb-bf086858da13
keywords:
- Función gluProject OpenGL
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
ms.openlocfilehash: 324f6c896c225453bfc8bf2ebb4b8619707c498c75e1309ea24fc6557cdd3deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488815"
---
# <a name="gluproject-function"></a>función gluProject

La **función gluProject** asigna coordenadas de objeto a coordenadas de ventana.

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

Coordenada del objeto x.

</dd> <dt>

*objy* 
</dt> <dd>

Coordenada del objeto y.

</dd> <dt>

*objz* 
</dt> <dd>

Coordenada del objeto z.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

La matriz modelview actual (a partir de una [**llamada a glGetDoublev).**](glgetdoublev.md)

</dd> <dt>

*projMatrix* 
</dt> <dd>

La matriz de proyección actual (a partir de **una llamada a glGetDoublev).**

</dd> <dt>

*Viewport* 
</dt> <dd>

La ventanilla actual (como desde una [**llamada a glGetIntegerv).**](glgetintegerv.md)

</dd> <dt>

*Winx* 
</dt> <dd>

Coordenada de ventana x calculada.

</dd> <dt>

*Winy* 
</dt> <dd>

Coordenada de ventana y calculada.

</dd> <dt>

*Winz* 
</dt> <dd>

Coordenada de ventana z calculada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es GL \_ TRUE.

Si se produce un error en la función, el valor devuelto es GL \_ FALSE.

## <a name="remarks"></a>Comentarios

La **función gluProject** transforma las coordenadas de objeto especificadas en coordenadas de ventana mediante *modelMatrix*, *projMatrix* y *viewport*. El resultado se almacena en *winx,* *winy* y *winz.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glGetDoublev**](glgetdoublev.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluUnProject**](gluunproject.md)
</dt> </dl>

 

 





