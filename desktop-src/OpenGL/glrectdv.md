---
title: Función glRectdv (Gl.h)
description: La función glRectdv dibuja un rectángulo.
ms.assetid: 53000734-bfc3-42c3-aa80-0a54e3dd36ec
keywords:
- Función glRectdv OpenGL
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
ms.openlocfilehash: 814638997c62b0248bae834f2acd1cd04f0723593533c2fc9237f84c1a4fcd11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036665"
---
# <a name="glrectdv-function"></a>Función glRectdv

La **función glRectdv** dibuja un rectángulo.

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

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glRectd** admite una especificación eficaz de rectángulos como dos puntos de esquina. Cada comando de rectángulo toma cuatro argumentos, organizados como dos pares consecutivos de coordenadas *(x*, *y*) o como dos punteros a matrices, cada uno de los que contiene un par (*x*, *y*). El rectángulo resultante se define en el *plano z* = 0.

La **función glRectd**(*x1,* *y1,* *x2,* *y2*) es exactamente equivalente a la secuencia siguiente:

**glBegin**(GL \_ POLYGON);

**glVertex2**( *x1,* *y1* );

**glVertex2**( *x2,* *y1* );

**glVertex2**( *x2,* *y2* );

**glVertex2**( *x1,* *y2* );

**glEnd**( );

Observe que si el segundo vértice está por encima y a la derecha del primer vértice, el rectángulo se construye con una sinuoso en sentido contrario a las agujas del reloj.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





