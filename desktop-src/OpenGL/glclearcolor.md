---
title: Función glClearColor (Gl.h)
description: La función glClearColor especifica valores claros para los búferes de color.
ms.assetid: f938e3f4-9db3-4c24-97ae-531b6799224e
keywords:
- Función glClearColor OpenGL
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
ms.openlocfilehash: 1bd68590ab9221dd094265a54f3c69ca396f810fb1f716c194b627a675196edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061923"
---
# <a name="glclearcolor-function"></a>Función glClearColor

La **función glClearColor** especifica valores claros para los búferes de color.

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

*Rojo* 
</dt> <dd>

Valor rojo que [**glClear**](glclear.md) usa para borrar los búferes de color. El valor predeterminado es cero.

</dd> <dt>

*Verde* 
</dt> <dd>

Valor verde que [**glClear**](glclear.md) usa para borrar los búferes de color. El valor predeterminado es cero.

</dd> <dt>

*Azul* 
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
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glClearColor** especifica los valores rojo, verde, azul y alfa que [**usa glClear**](glclear.md) para borrar los búferes de color. Los valores especificados **por glClearColor** se fijan en el \[ intervalo 0,1 \] .

Las siguientes funciones recuperan información relacionada con **la función glClearColor:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ GL ACCUM \_ CLEAR \_ VALUE

**glGet con** el argumento GL \_ COLOR CLEAR \_ \_ VALUE

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

[**glClear**](glclear.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





