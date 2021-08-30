---
title: Función glClearIndex (Gl.h)
description: La función glClearIndex especifica el valor claro para los búferes de índice de color.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- Función glClearIndex OpenGL
topic_type:
- apiref
api_name:
- glClearIndex
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6ed297ba30749d20d846055122f3ab12f77f8625450626a58fd15928172a207
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082055"
---
# <a name="glclearindex-function"></a>Función glClearIndex

La **función glClearIndex** especifica el valor claro para los búferes de índice de color.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glClearIndex(
   GLfloat c
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*c* 
</dt> <dd>

Índice utilizado cuando se borran los búferes de índice de color. El valor predeterminado es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glClearIndex** especifica el índice utilizado por [**glClear**](glclear.md) para borrar los búferes de índice de color. El *parámetro c* no está fija. En su lugar, *c* se convierte en un valor de punto fijo con precisión no especificada a la derecha del punto binario. A continuación, la parte entera de este valor se enmascara con 2 <sup>m</sup>  - 1, donde *m* es el número de bits de un índice de color almacenado en el búfer de fotogramas.

Las funciones siguientes recuperan información relacionada **con glClearIndex**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ INDEX CLEAR \_ \_ VALUE

**glGet con** el argumento GL \_ INDEX \_ BITS

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

 

 





