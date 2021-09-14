---
title: Función glNormal3b (Gl.h)
description: Establece el vector normal actual. | Función glNormal3b (Gl.h)
ms.assetid: b6976143-bc9a-4766-9f7e-5380c3a24173
keywords:
- Función glNormal3b OpenGL
topic_type:
- apiref
api_name:
- glNormal3b
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a09a92b718881670ed5625fd5aa94a23193cdd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375151"
---
# <a name="glnormal3b-function"></a>Función glNormal3b

Establece el vector normal actual.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glNormal3b(
   GLbyte nx,
   GLbyte ny,
   GLbyte nz
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

## <a name="remarks"></a>Observaciones

La normal actual se establece en las coordenadas dadas cada vez que se llama a la **función glNormal3b.**

Los argumentos byte, short o integer se convierten al formato de punto flotante mediante una asignación lineal que asigna el valor entero representable más positivo a 1,0 y el valor entero representable más negativo a -1,0.

Las normales especificadas **con glNormal3b** no necesitan tener longitud de unidad. Si la normalización está habilitada, las normales especificadas **con glNormal3b** se normalizan después de la transformación. Puede controlar la normalización mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL \_ NORMALIZE. De forma predeterminada, la normalización está deshabilitada. Puede actualizar la normal actual en cualquier momento. En concreto, puede llamar a **glNormal3b** entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). Las siguientes funciones recuperan información relacionada **con glNormal3b**:

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

 

 





