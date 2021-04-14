---
title: función glDepthRange (GL. h)
description: La función glDepthRange especifica la asignación de valores z de coordenadas de dispositivo normalizadas a coordenadas de la ventana.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- glDepthRange (función) OpenGL
topic_type:
- apiref
api_name:
- glDepthRange
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0bd6a22ae91877c9b20fa5387edd9438942a07d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422111"
---
# <a name="gldepthrange-function"></a>glDepthRange función)

La función **glDepthRange** especifica la asignación de valores *z* de coordenadas de dispositivo normalizadas a coordenadas de la ventana.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glDepthRange(
   GLclampd zNear,
   GLclampd zFar
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*zNear* 
</dt> <dd>

Asignación del plano de recorte cercano a las coordenadas de la ventana. El valor predeterminado es cero.

</dd> <dt>

*zFar* 
</dt> <dd>

Asignación del plano de recorte lejano a las coordenadas de la ventana. El valor predeterminado es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Después del recorte y la división por *w*, las coordenadas *z* van de 0,0 a 1,0, correspondientes a los planos de recorte Near y Far. La función **glDepthRange** especifica una asignación lineal de las coordenadas *z* normalizadas en este intervalo a las coordenadas *z* de la ventana. Independientemente de la implementación del búfer de profundidad real, los valores de profundidad de coordenadas de la ventana se tratan como si fueran de 0,0 a 1,0 (como los componentes de color). Por lo tanto, los valores aceptados por **glDepthRange** se fijan a este intervalo antes de aceptarlos.

La asignación predeterminada de (0,0) asigna el plano cercano a 0 y el plano lejano a 1. Con esta asignación, el intervalo de búfer de profundidad se ha utilizado por completo.

No es necesario que *zNear* sea menor que *zFar*. Las asignaciones inversas como (1,0) son aceptables.

La siguiente función recupera información relacionada con **glDepthRange**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con rango de profundidad de contabilidad de argumentos \_ \_

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





