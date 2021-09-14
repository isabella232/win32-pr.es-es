---
title: Función glTexCoord1i (Gl.h)
description: Establece las coordenadas de textura actuales. | Función glTexCoord1i (Gl.h)
ms.assetid: 910e5908-8c19-4c79-9744-a534bce03b20
keywords:
- Función GlTexCoord1i OpenGL
topic_type:
- apiref
api_name:
- glTexCoord1i
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6beb3bb6c452422c6ba28283bd9f9f3467bc9d86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260039"
---
# <a name="gltexcoord1i-function"></a>Función glTexCoord1i

Establece las coordenadas de textura actuales.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glTexCoord1i(
   GLint s
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*s* 
</dt> <dd>

Coordenada de textura de la .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La [**función glTexCoord**](gltexcoord-functions.md) establece las coordenadas de textura actuales que forman parte de los datos asociados a los vértices de polígono. La **función glTexCoord** especifica coordenadas de textura en una, dos, tres o cuatro dimensiones. La función glTexCoord1 establece las coordenadas de textura actuales en (s, 0, 0, 1); Una llamada a glTexCoord2 los establece en (s, t, 0, 1). De forma similar, glTexCoord3 especifica las coordenadas de textura como (s, t, r, 1) y glTexCoord4 define los cuatro componentes explícitamente como (s, t, r, q). Puede actualizar las coordenadas de textura actuales en cualquier momento. En concreto, puede llamar a glTexCoord entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md). La función siguiente recupera información relacionada con **glTexCoord**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ CURRENT \_ TEXTURE \_ COORDS

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





