---
title: Función glRectd (Gl.h)
description: La función glRectd dibuja un rectángulo.
ms.assetid: d5574c22-7ae1-4040-9b95-769693fa41e3
keywords:
- Función glRectd OpenGL
topic_type:
- apiref
api_name:
- glRectd
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 961b5b9ddf478475806d391d6499eed01fd43e14781f57dcd82e9ff6a1a55a72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492175"
---
# <a name="glrectd-function"></a>función glRectd

La **función glRectd** dibuja un rectángulo.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glRectd(
   GLdouble x1,
   GLdouble y1,
   GLdouble x2,
   GLdouble y2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x1* 
</dt> <dd>

*Coordenada x* del vértice de un rectángulo.

</dd> <dt>

*y1* 
</dt> <dd>

*Coordenada y* del vértice de un rectángulo.

</dd> <dt>

*x2* 
</dt> <dd>

Coordenada *x* del vértice opuesto del rectángulo.

</dd> <dt>

*y2* 
</dt> <dd>

*Coordenada y* del vértice opuesto del rectángulo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glRectd** admite la especificación eficaz de rectángulos como dos puntos de esquina. Cada comando de rectángulo toma cuatro argumentos, organizados como dos pares consecutivos de coordenadas (*x*, *y*) o como dos punteros a matrices, cada uno de los que contiene un par (*x*, *y*). El rectángulo resultante se define en el *plano z* = 0.

La **función glRectd**(*x1,* *y1,* *x2,* *y2*) es exactamente equivalente a la secuencia siguiente:

**glBegin**(GL \_ POLYGON);

**glVertex2**( *x1,* *y1* );

**glVertex2**( *x2,* *y1* );

**glVertex2**( *x2,* *y2* );

**glVertex2**( *x1,* *y2* );

**glEnd**( );

Tenga en cuenta que si el segundo vértice está por encima y a la derecha del primer vértice, el rectángulo se construye con una sinuoso en sentido contrario a las agujas del reloj.

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

 

 





