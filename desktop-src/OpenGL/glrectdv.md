---
title: función glRectdv (GL. h)
description: La función glRectdv dibuja un rectángulo.
ms.assetid: 53000734-bfc3-42c3-aa80-0a54e3dd36ec
keywords:
- glRectdv (función) OpenGL
topic_type:
- apiref
api_name:
- glRectdv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2956a1f658101a384ae69b05ed50418492d264
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421938"
---
# <a name="glrectdv-function"></a>glRectdv función)

La función **glRectdv** dibuja un rectángulo.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glRectdv(
   const GLdouble *v1,
   const GLdouble *v2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*v1* 
</dt> <dd>

Puntero a un vértice de un rectángulo.

</dd> <dt>

*v2* 
</dt> <dd>

puntero al vértice opuesto del rectángulo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glRectd** admite la especificación eficaz de rectángulos como dos puntos de vértice. Cada comando de rectángulo toma cuatro argumentos, organizados como dos pares consecutivos de coordenadas (*x*, *y*), o como dos punteros a matrices, cada una con un par (*x*, *y*). El rectángulo resultante se define en el plano *z* = 0.

La función **glRectd**(*x1,* *Y1,* *x2,* *Y2*) es exactamente equivalente a la secuencia siguiente:

**glBegin**(GL, \_ polígono);

**glVertex2**( *x1,* *Y1* );

**glVertex2**( *x2,* *Y1* );

**glVertex2**( *x2,* *Y2* );

**glVertex2**( *x1,* *Y2* );

**glEnd**();

Observe que si el segundo vértice está por encima y a la derecha del primer vértice, el rectángulo se construye con un bobinado en sentido contrario a las agujas del reloj.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





