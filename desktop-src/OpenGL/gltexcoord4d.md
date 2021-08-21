---
title: Función glTexCoord4d (Gl.h)
description: Establece las coordenadas de textura actuales. | Función glTexCoord4d (Gl.h)
ms.assetid: d9045a2e-81f3-4f63-8eee-e882c586b8fe
keywords:
- Función glTexCoord4d OpenGL
topic_type:
- apiref
api_name:
- glTexCoord4d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fbdd49d6a760e3e1c43fddcd5bcce85418d34ca803569a4c22ab6bea89b266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613754"
---
# <a name="gltexcoord4d-function"></a>Función glTexCoord4d

Establece las coordenadas de textura actuales.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexCoord4d(
   GLdouble s,
   GLdouble t,
   GLdouble r,
   GLdouble q
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*s* 
</dt> <dd>

Coordenada de textura de la .

</dd> <dt>

*t* 
</dt> <dd>

Coordenada de textura t.

</dd> <dt>

*r* 
</dt> <dd>

Coordenada de textura r.

</dd> <dt>

*Q* 
</dt> <dd>

Coordenada de textura q.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La [**función glTexCoord**](gltexcoord-functions.md) establece las coordenadas de textura actuales que forman parte de los datos asociados a vértices de polígono. La **función glTexCoord** especifica coordenadas de textura en una, dos, tres o cuatro dimensiones. La función glTexCoord1 establece las coordenadas de textura actuales en (s, 0, 0, 1); Una llamada a glTexCoord2 los establece en (s, t, 0, 1). De forma similar, glTexCoord3 especifica las coordenadas de textura como (s, t, r, 1) y glTexCoord4 define los cuatro componentes explícitamente como (s, t, r, q). Puede actualizar las coordenadas de textura actuales en cualquier momento. En concreto, puede llamar a glTexCoord entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). La función siguiente recupera información relacionada con **glTexCoord**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ CURRENT \_ TEXTURE \_ COORDS

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

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





