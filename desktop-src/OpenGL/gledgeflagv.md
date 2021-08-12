---
title: Función glEdgeFlagv (Gl.h)
description: Marca los bordes como límites o no delimitadores. | Función glEdgeFlagv (Gl.h)
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- Función glEdgeFlagv OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9622cb3c7d80d241d0f12957094a06980f5fcf7f28b4f95eaa0de1595b34d1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616537"
---
# <a name="gledgeflagv-function"></a>Función glEdgeFlagv

Marca los bordes como límites o no delimitadores.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glEdgeFlagv(
   const GLboolean *flag
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flag* 
</dt> <dd>

Especifica un puntero a una matriz que contiene un único elemento booleano, que reemplaza el valor de marca de borde actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cada vértice de un polígono, triángulo independiente o cuadrículo independiente especificado entre un par [**glBegin**](/windows/desktop/OpenGL/glbegin)glEnd se marca como el inicio de un límite o un borde / [](/windows/desktop/OpenGL/glend) no delimitador. Si la marca de borde actual es **TRUE** cuando se especifica el vértice, el vértice se marca como el inicio de un borde de límite. Si la marca de borde actual **es FALSE,** el vértice se marca como el inicio de un borde no enlazar. La **función glEdgeFlagv** establece la marca perimetral en **TRUE** si flag es distinto de cero, **FALSE** en caso contrario.

Los vértices de los triángulos conectados y los cuadríteros conectados siempre se marcan como límites, independientemente del valor de la marca de borde.

Las marcas de borde límite y no delimitador en vértices solo son significativas si GL POLYGON MODE está establecido en \_ GL POINT o GL \_ \_ \_ LINE. Vea [**glPolygonMode.**](/windows/desktop/OpenGL/glpolygonmode)

Inicialmente, el bit de marca perimetral es **TRUE.**

La marca perimetral actual se puede actualizar en cualquier momento. En concreto, se puede llamar a **glEdgeFlagv** entre una llamada a [**glBegin**](/windows/desktop/OpenGL/glbegin) y la llamada correspondiente [**a glEnd**](/windows/desktop/OpenGL/glend).

Las siguientes funciones recuperan información relacionada **con glEdgeFlagv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ EDGE \_ FLAG

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

