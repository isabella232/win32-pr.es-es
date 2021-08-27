---
title: Función glClearDepth (Gl.h)
description: La función glClearDepth especifica el valor clear para el búfer de profundidad.
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
keywords:
- Función glClearDepth OpenGL
topic_type:
- apiref
api_name:
- glClearDepth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ed8efc8585da717349705bc13db920a707e16a66def2b026a3237b778f78575
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082065"
---
# <a name="glcleardepth-function"></a>función glClearDepth

La **función glClearDepth** especifica el valor clear para el búfer de profundidad.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glClearDepth(
   GLclampd depth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Profundidad* 
</dt> <dd>

Valor de profundidad utilizado cuando se borra el búfer de profundidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glClearDepth** especifica el valor de profundidad utilizado por [**glClear**](glclear.md) para borrar el búfer de profundidad. Los valores especificados **por glClearDepth** se fijan en el \[ intervalo 0,1 \] .

La función siguiente recupera información relacionada con la **función glClearDepth:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ DEPTH CLEAR \_ \_ VALUE

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





