---
title: función glNormal3d (GL. h)
description: Establece el vector normal actual. | función glNormal3d (GL. h)
ms.assetid: d256aef0-3ad5-4e70-b1c8-6402434b1e67
keywords:
- glNormal3d (función) OpenGL
topic_type:
- apiref
api_name:
- glNormal3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6ab158e298ff20cce635ab4002f38ca82fdaa2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083683"
---
# <a name="glnormal3d-function"></a>glNormal3d función)

Establece el vector normal actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glNormal3d(
   GLdouble nx,
   GLdouble ny,
   GLdouble nz
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

La normal actual se establece en las coordenadas especificadas siempre que se llama a la función **glNormal3d**.

Los argumentos byte, Short o Integer se convierten al formato de punto flotante mediante una asignación lineal que asigna el valor entero representable más positivo a 1,0 y el valor entero representable más negativo a-1,0.

Las normales especificadas mediante **glNormal3d** no necesitan tener una longitud de unidad. Si la normalización está habilitada, las normales especificadas con **glNormal3d** se normalizan después de la transformación. Puede controlar la normalización mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento libro de contabilidad \_ . De forma predeterminada, la normalización está deshabilitada. Puede actualizar la normal actual en cualquier momento. En concreto, puede llamar a **glNormal3d** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md). Las siguientes funciones recuperan información relacionada con **glNormal3d**:

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

 

 





