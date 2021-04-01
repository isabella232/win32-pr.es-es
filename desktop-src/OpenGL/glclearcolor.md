---
title: función glClearColor (GL. h)
description: La función glClearColor especifica valores claros para los búferes de color.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- glClearColor (función) OpenGL
topic_type:
- apiref
api_name:
- glClearColor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34005ce34900f5fee8a4c9b2f1b963b7fe4bb6d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802605"
---
# <a name="glclearcolor-function"></a>glClearColor función)

La función **glClearColor** especifica valores claros para los búferes de color.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glClearColor(
   GLclampf red,
   GLclampf green,
   GLclampf blue,
   GLclampf alpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*alerta* 
</dt> <dd>

Valor rojo que [**glClear**](glclear.md) usa para borrar los búferes de color. El valor predeterminado es cero.

</dd> <dt>

*verde* 
</dt> <dd>

Valor verde que [**glClear**](glclear.md) usa para borrar los búferes de color. El valor predeterminado es cero.

</dd> <dt>

*azul* 
</dt> <dd>

Valor azul que [**glClear**](glclear.md) usa para borrar los búferes de color. El valor predeterminado es cero.

</dd> <dt>

*alpha* 
</dt> <dd>

Valor alfa que [**glClear**](glclear.md) usa para borrar los búferes de color. El valor predeterminado es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glClearColor** especifica los valores rojo, verde, azul y alfa usados por [**glClear**](glclear.md) para borrar los búferes de color. Los valores especificados por **glClearColor** se fijan en el intervalo \[ 0, 1 \] .

Las siguientes funciones recuperan información relacionada con la función **glClearColor** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ valor Clear acumulado de GL \_

**glGet** con el argumento \_ GL \_ color \_ valor sin formato

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

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





