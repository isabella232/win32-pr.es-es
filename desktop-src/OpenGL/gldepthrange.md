---
title: Función glDepthRange (Gl.h)
description: La función glDepthRange especifica la asignación de valores z de coordenadas de dispositivo normalizadas a coordenadas de ventana.
ms.assetid: 44aed5e5-4bd2-4e7f-ad05-1cf4be5254a5
keywords:
- Función glDepthRange OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362074"
---
# <a name="gldepthrange-function"></a>Función glDepthRange

La **función glDepthRange** especifica la asignación de valores *z* de coordenadas de dispositivo normalizadas a coordenadas de ventana.

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

Asignación del plano de recorte cercano a coordenadas de ventana. El valor predeterminado es cero.

</dd> <dt>

*zFar* 
</dt> <dd>

Asignación del plano de recorte lejano a coordenadas de ventana. El valor predeterminado es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Después del recorte y la división *por w*, las coordenadas *z* oscilan entre 0,0 y 1,0, correspondientes a los planos de recorte cercanos y lejanos. La **función glDepthRange** especifica una asignación lineal de las coordenadas *z* normalizadas de este intervalo a las *coordenadas z* de la ventana. Independientemente de la implementación real del búfer de profundidad, los valores de profundidad de coordenadas de ventana se tratan como si oscilase entre 0,0 y 1,0 (como los componentes de color). Por lo tanto, los valores aceptados por **glDepthRange** se fijan a este intervalo antes de que se acepten.

La asignación predeterminada de (0,1) asigna el plano cercano a 0 y el plano lejano a 1. Con esta asignación, el intervalo de búfer de profundidad se utiliza completamente.

No es necesario que *zNear* sea menor que *zFar.* Las asignaciones inversas como (1,0) son aceptables.

La función siguiente recupera información relacionada con **glDepthRange**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ DEPTH \_ RANGE

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

 





