---
title: Función glNormal3fv (Gl.h)
description: Establece el vector normal actual. | Función glNormal3fv (Gl.h)
ms.assetid: 8e501de8-5877-4d77-9f32-4596d5217636
keywords:
- Función glNormal3fv OpenGL
topic_type:
- apiref
api_name:
- glNormal3fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33de53f6c5d363218f602319dbc71e7436e475ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375135"
---
# <a name="glnormal3fv-function"></a>Función glNormal3fv

Establece el vector normal actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glNormal3fv(
   const GLfloat *v
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*V* 
</dt> <dd>

Puntero a una matriz de tres elementos: las coordenadas x, y y z de la nueva normal actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La normal actual se establece en las coordenadas dadas cada vez que se llama a la **función glNormal3fv.**

Los argumentos byte, short o integer se convierten al formato de punto flotante con una asignación lineal que asigna el valor entero representable más positivo a 1,0 y el valor entero representable más negativo a -1,0.

Las normales especificadas mediante **glNormal3fv** no necesitan tener longitud de unidad. Si la normalización está habilitada, las normales especificadas **con glNormal3fv** se normalizan después de la transformación. Puede controlar la normalización mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL \_ NORMALIZE. De forma predeterminada, la normalización está deshabilitada. Puede actualizar la función normal actual en cualquier momento. En concreto, puede llamar a **glNormal3fv** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). Las siguientes funciones recuperan información relacionada **con glNormal3fv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ CURRENT \_ NORMAL

[**glIsEnable**](glisenabled.md) con el argumento GL \_ NORMALIZE

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

 

 





