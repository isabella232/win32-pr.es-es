---
title: función glClearIndex (GL. h)
description: La función glClearIndex especifica el valor no cifrado de los búferes de índice de color.
ms.assetid: 87983d93-c5a1-445f-8621-1c2952d93a0f
keywords:
- glClearIndex (función) OpenGL
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
ms.openlocfilehash: 85b1ed90b017828e13d387e1e6db440c1d781cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491134"
---
# <a name="glclearindex-function"></a>glClearIndex función)

La función **glClearIndex** especifica el valor no cifrado de los búferes de índice de color.

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

Índice que se utiliza cuando se borran los búferes de índice de color. El valor predeterminado es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glClearIndex** especifica el índice usado por [**glClear**](glclear.md) para borrar los búferes de índice de color. El parámetro *c* no está fijado. En su lugar, *c* se convierte en un valor de punto fijo con una precisión no especificada a la derecha del punto binario. A continuación, la parte entera de este valor se enmascara con 2 <sup>m</sup>  -1, donde *m* es el número de bits de un índice de color almacenado en el fotogramas.

Las siguientes funciones recuperan información relacionada con **glClearIndex**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ valor sin formato de índice de contabilidad \_

**glGet** con argumento \_ bits de índice de GL \_

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

 

 





