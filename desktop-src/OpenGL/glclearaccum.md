---
title: función glClearAccum (GL. h)
description: La función glClearAccum especifica los valores claros para el búfer de acumulación.
ms.assetid: 77d8f340-be47-43f4-96fc-31025a4c8b4e
keywords:
- glClearAccum (función) OpenGL
topic_type:
- apiref
api_name:
- glClearAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3098e87a47509b8c05035171a8f31e57d8618424
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150435"
---
# <a name="glclearaccum-function"></a>glClearAccum función)

La función **glClearAccum** especifica los valores claros para el búfer de acumulación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glClearAccum(
   GLfloat red,
   GLfloat green,
   GLfloat blue,
   GLfloat alpha
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*alerta* 
</dt> <dd>

El valor rojo que se utiliza cuando se borra el búfer de acumulación. El valor predeterminado es cero.

</dd> <dt>

*verde* 
</dt> <dd>

El valor verde que se utiliza cuando se borra el búfer de acumulación. El valor predeterminado es cero.

</dd> <dt>

*azul* 
</dt> <dd>

El valor azul que se utiliza cuando se borra el búfer de acumulación. El valor predeterminado es cero.

</dd> <dt>

*alpha* 
</dt> <dd>

Valor alfa que se utiliza cuando se borra el búfer de acumulación. El valor predeterminado es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glClearAccum** especifica los valores rojo, verde, azul y alfa usados por [**glClear**](glclear.md) para borrar el búfer de acumulación.

Los valores especificados por **glClearAccum** se fijan en el intervalo \[ 1, 1 \] .

La siguiente función recupera información relacionada con **glClearAccum**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ valor Clear acumulado de GL \_

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

 

 





