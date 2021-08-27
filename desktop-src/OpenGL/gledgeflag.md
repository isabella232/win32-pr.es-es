---
title: Función glEdgeFlag (Gl.h)
description: Marca los bordes como límites o no delimitadores. | Función glEdgeFlag (Gl.h)
ms.assetid: cebaa4af-a3bc-4396-9ee0-8cc10bcaf256
keywords:
- Función glEdgeFlag OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlag
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c7f78575c79b3da5b48125203d88c9b20e7eb1dc11ee860deea01dfa7dcea28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081595"
---
# <a name="gledgeflag-function"></a>Función glEdgeFlag

Marca los bordes como límites o no delimitadores.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEdgeFlag(
   GLboolean flag
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flag* 
</dt> <dd>

Especifica el valor de marca perimetral actual, **TRUE** o **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cada vértice de un polígono, triángulo independiente o cuadrículo independiente especificado entre un par [**glBegin**](/windows/desktop/OpenGL/glbegin)glEnd se marca como el inicio de un límite o un borde / [](/windows/desktop/OpenGL/glend) no delimitador. Si la marca de borde actual es **TRUE** cuando se especifica el vértice, el vértice se marca como el inicio de un borde de límite. Si la marca de borde actual **es FALSE,** el vértice se marca como el inicio de un borde no enlazar. La **función glEdgeFlag** establece la marca perimetral en **TRUE** si flag es distinto de cero, **FALSE** en caso contrario.

Los vértices de los triángulos conectados y los cuadríteros conectados siempre se marcan como límites, independientemente del valor de la marca de borde.

Las marcas de borde límites y no delimitadores en vértices solo son significativas si GL POLYGON MODE se establece en \_ GL POINT o GL \_ \_ \_ LINE. Vea [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).

Inicialmente, el bit de marca perimetral es **TRUE.**

La marca perimetral actual se puede actualizar en cualquier momento. En concreto, se puede llamar a **glEdgeFlag** entre una llamada a [**glBegin**](/windows/desktop/OpenGL/glbegin) y la llamada correspondiente [**a glEnd**](/windows/desktop/OpenGL/glend).

Las siguientes funciones recuperan información relacionada con **glEdgeFlag**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ EDGE \_ FLAG

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

