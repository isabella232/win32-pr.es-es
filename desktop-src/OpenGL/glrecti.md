---
title: Función glRecti (Gl.h)
description: La función glRecti dibuja un rectángulo.
ms.assetid: 8f618b5e-5406-4342-8f7a-83a65bad8a6f
keywords:
- Función glRecti OpenGL
topic_type:
- apiref
api_name:
- glRecti
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fa1432cc74dc87165fcddfa5e28542434758e11606d186302fc2cfe3c6453a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491995"
---
# <a name="glrecti-function"></a>Función glRecti

La **función glRecti** dibuja un rectángulo.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glRecti(
   GLint x1,
   GLint y1,
   GLint x2,
   GLint y2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x1* 
</dt> <dd>

Coordenada *x* del vértice de un rectángulo.

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

La **función glRecti** admite una especificación eficaz de rectángulos como dos puntos de esquina. Cada comando de rectángulo toma cuatro argumentos, organizados como dos pares consecutivos de coordenadas *(x*, *y*) o como dos punteros a matrices, cada uno de los que contiene un par (*x*, *y*). El rectángulo resultante se define en el *plano z* = 0.

La **función glRecti**(*x1,* *y1,* *x2,* *y2*) es exactamente equivalente a la secuencia siguiente:

**glBegin**(GL \_ POLYGON);

**glVertex2**( *x1,* *y1* );

**glVertex2**( *x2,* *y1* );

**glVertex2**( *x2,* *y2* );

**glVertex2**( *x1,* *y2* );

**glEnd**( );

Observe que si el segundo vértice está por encima y a la derecha del primer vértice, el rectángulo se construye con una sinuoso en sentido contrario a las agujas del reloj.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





