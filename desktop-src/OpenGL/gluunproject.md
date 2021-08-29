---
title: Función gluUnProject (Glu.h)
description: La función gluUnProject asigna coordenadas de ventana a coordenadas de objeto.
ms.assetid: 6a719fc2-ad40-4b22-9c99-5753f5dbb8a0
keywords:
- Función gluUnProject OpenGL
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
ms.openlocfilehash: f88c303e6a9471f0de38f891c7b376785d29b5052432ef234fa531861400841e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488405"
---
# <a name="gluunproject-function"></a>función gluUnProject

La **función gluUnProject** asigna coordenadas de ventana a coordenadas de objeto.

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

*Winx* 
</dt> <dd>

Coordenada de ventana x que se va a asignar.

</dd> <dt>

*Winy* 
</dt> <dd>

Coordenada de ventana y que se va a asignar.

</dd> <dt>

*Winz* 
</dt> <dd>

Coordenada de ventana z que se va a asignar.

</dd> <dt>

*modelMatrix* 
</dt> <dd>

La matriz modelview (como de una [**llamada a glGetDoublev).**](glgetdoublev.md)

</dd> <dt>

*projMatrix* 
</dt> <dd>

Matriz de proyección (a partir de una **llamada a glGetDoublev).**

</dd> <dt>

*Viewport* 
</dt> <dd>

Ventanilla (como desde una [**llamada a glGetIntegerv).**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)

</dd> <dt>

*objx* 
</dt> <dd>

Coordenada de objeto x calculada.

</dd> <dt>

*objy* 
</dt> <dd>

Coordenada del objeto y calculado.

</dd> <dt>

*objz* 
</dt> <dd>

Coordenada de objeto z calculada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es GL \_ TRUE.

Si se produce un error en la función, el valor devuelto es GL \_ FALSE.

## <a name="remarks"></a>Comentarios

La **función gluUnProject** asigna las coordenadas de ventana especificadas en coordenadas de objeto mediante *modelMatrix*, *projMatrix* y *viewport*. El resultado se almacena en *objx*, *objy* y *objz*.

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

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetDoublev**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluProject**](gluproject.md)
</dt> </dl>

 

 





