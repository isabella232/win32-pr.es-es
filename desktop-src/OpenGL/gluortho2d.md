---
title: función gluOrtho2D (GLU. h)
description: La función gluOrtho2D define una matriz de proyección ortográfica 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- gluOrtho2D (función) OpenGL
topic_type:
- apiref
api_name:
- gluOrtho2D
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36b321f312a074a5dd78340968f1c9b2b844c6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421901"
---
# <a name="gluortho2d-function"></a>gluOrtho2D función)

La función **gluOrtho2D** define una matriz de proyección ortográfica 2D.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluOrtho2D(
   GLdouble left,
   GLdouble right,
   GLdouble top,
   GLdouble bottom
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*salido* 
</dt> <dd>

Coordenada del plano de recorte vertical izquierdo.

</dd> <dt>

*correcta* 
</dt> <dd>

Coordenada del plano de recorte vertical derecho.

</dd> <dt>

*top* 
</dt> <dd>

Coordenada del plano de recorte horizontal superior.

</dd> <dt>

*descendente* 
</dt> <dd>

Coordenada del plano de recorte horizontal inferior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluOrtho2D** configura una región de visualización ortográfica bidimensional. Esto es equivalente a llamar a [**glOrtho**](glortho.md) con Near = 1 y Far = 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





