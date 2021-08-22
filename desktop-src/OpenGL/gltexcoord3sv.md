---
title: Función glTexCoord3sv (Gl.h)
description: Establece las coordenadas de textura actuales. | Función glTexCoord3sv (Gl.h)
ms.assetid: bd7970df-82b3-4ccd-960d-9c04a6726bab
keywords:
- Función GlTexCoord3sv OpenGL
topic_type:
- apiref
api_name:
- glTexCoord3sv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c41d010dd5ed3a770516a22e1e2c20df6a54cfa7e33413e1e5e69cf90da9399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490935"
---
# <a name="gltexcoord3sv-function"></a>Función glTexCoord3sv

Establece las coordenadas de textura actuales.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexCoord3sv(
   const GLshort *v
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*V* 
</dt> <dd>

Puntero a una matriz de tres elementos, que a su vez especifica las coordenadas de textura s, t y r.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La [**función glTexCoord**](gltexcoord-functions.md) establece las coordenadas de textura actuales que forman parte de los datos asociados a los vértices de polígono. La **función glTexCoord** especifica coordenadas de textura en una, dos, tres o cuatro dimensiones. La función glTexCoord1 establece las coordenadas de textura actuales en (s, 0, 0, 1); Una llamada a glTexCoord2 los establece en (s, t, 0, 1). De forma similar, glTexCoord3 especifica las coordenadas de textura como (s, t, r, 1) y glTexCoord4 define los cuatro componentes explícitamente como (s, t, r, q). Puede actualizar las coordenadas de textura actuales en cualquier momento. En concreto, puede llamar a glTexCoord entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). La función siguiente recupera información relacionada con **glTexCoord**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ CURRENT \_ TEXTURE \_ COORDS

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

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





