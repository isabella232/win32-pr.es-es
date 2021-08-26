---
title: Función glNormal3d (Gl.h)
description: Establece el vector normal actual. | Función glNormal3d (Gl.h)
ms.assetid: d256aef0-3ad5-4e70-b1c8-6402434b1e67
keywords:
- Función glNormal3d OpenGL
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
ms.openlocfilehash: 53eb5950b34b9f3fa838e773f7e3e6438caa603162ca8f8181534e67e8540191
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128195"
---
# <a name="glnormal3d-function"></a>Función glNormal3d

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

*Nx* 
</dt> <dd>

Especifica la coordenada x para el nuevo vector normal actual.

</dd> <dt>

*Ny* 
</dt> <dd>

Especifica la coordenada Y para el nuevo vector normal actual.

</dd> <dt>

*Nz* 
</dt> <dd>

Especifica la coordenada z para el nuevo vector normal actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La normal actual se establece en las coordenadas especificadas cada vez que se llama a la **función glNormal3d.**

Los argumentos byte, corto o entero se convierten al formato de punto flotante mediante una asignación lineal que asigna el valor entero representable más positivo a 1,0 y el valor entero representable más negativo a -1,0.

Las normales especificadas mediante **glNormal3d** no necesitan tener longitud de unidad. Si la normalización está habilitada, las normales especificadas **con glNormal3d** se normalizan después de la transformación. Puede controlar la normalización mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL \_ NORMALIZE. De forma predeterminada, la normalización está deshabilitada. Puede actualizar el normal actual en cualquier momento. En concreto, puede llamar a **glNormal3d** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). Las siguientes funciones recuperan información relacionada **con glNormal3d**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CURRENT \_ NORMAL

[**glIsEnable con**](glisenabled.md) el argumento GL \_ NORMALIZE

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

 

 





