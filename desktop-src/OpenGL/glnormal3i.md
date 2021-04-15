---
title: función glNormal3i (GL. h)
description: Establece el vector normal actual. | función glNormal3i (GL. h)
ms.assetid: ea14e5c6-a725-4d24-9a48-c138ee8b6cd1
keywords:
- glNormal3i (función) OpenGL
topic_type:
- apiref
api_name:
- glNormal3i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be4c368fcd93ef832bcdb9cf82abe82c5e02413d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362347"
---
# <a name="glnormal3i-function"></a>glNormal3i función)

Establece el vector normal actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glNormal3i(
   GLint nx,
   GLint ny,
   GLint nz
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NX* 
</dt> <dd>

Especifica la coordenada x del nuevo vector normal actual.

</dd> <dt>

*1002* 
</dt> <dd>

Especifica la coordenada y del nuevo vector normal actual.

</dd> <dt>

*Zelanda* 
</dt> <dd>

Especifica la coordenada z del nuevo vector normal actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La normal actual se establece en las coordenadas especificadas siempre que se llama a la función **glNormal3i**.

Los argumentos byte, Short o Integer se convierten al formato de punto flotante con una asignación lineal que asigna el valor entero representable más positivo a 1,0 y el valor entero representable más negativo a-1,0.

Las normales especificadas mediante **glNormal3i** no necesitan tener una longitud de unidad. Si la normalización está habilitada, las normales especificadas con **glNormal3i** se normalizan después de la transformación. Puede controlar la normalización mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento libro de contabilidad \_ . De forma predeterminada, la normalización está deshabilitada. Puede actualizar la normal actual en cualquier momento. En concreto, puede llamar a **glNormal3i** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md). Las siguientes funciones recuperan información relacionada con **glNormal3i**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ actual \_ normal

[**glIsEnable**](glisenabled.md) con el argumento \_ normalizar libro de contabilidad

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





