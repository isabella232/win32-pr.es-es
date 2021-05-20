---
title: Función gluOrtho2D (Glu.h)
description: La función gluOrtho2D define una matriz de proyección ortográfica 2D.
ms.assetid: ba83fb5c-e5c7-4486-a815-a1aff0469757
keywords:
- Función gluOrtho2D OpenGL
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
ms.openlocfilehash: 1bf07fea583c5ae46680d888f6bf6c0a9c5aa9a0
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153558"
---
# <a name="gluortho2d-function"></a>Función gluOrtho2D

La **función gluOrtho2D** define una matriz de proyección ortográfica 2D.

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

*Izquierda* 
</dt> <dd>

Coordenada del plano de recorte vertical izquierdo.

</dd> <dt>

*Correcto* 
</dt> <dd>

Coordenada del plano de recorte vertical derecho.

</dd> <dt>

*top* 
</dt> <dd>

Coordenada del plano de recorte horizontal superior.

</dd> <dt>

*Parte inferior* 
</dt> <dd>

Coordenada del plano de recorte horizontal inferior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función gluOrtho2D** configura una región de visualización ortográfica bidimensional. Esto equivale a llamar [**a glOrtho**](glortho.md) con zNear = -1 y zFar = 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





