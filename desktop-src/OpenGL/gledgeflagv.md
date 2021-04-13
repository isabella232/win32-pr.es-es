---
title: función glEdgeFlagv (GL. h)
description: Marca los bordes como límite o no límite. | función glEdgeFlagv (GL. h)
ms.assetid: 69b5ddbd-7c0c-47f0-a358-d8bf81755c88
keywords:
- glEdgeFlagv (función) OpenGL
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
ms.openlocfilehash: fe031ab3981e3daa2e6b1aefd51c9eaa62c84483
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362233"
---
# <a name="gledgeflagv-function"></a>glEdgeFlagv función)

Marca los bordes como límite o no límite.

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

Especifica un puntero a una matriz que contiene un único elemento booleano, que reemplaza el valor de la marca perimetral actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cada vértice de un polígono, un triángulo independiente o cuadrangular independientes especificados entre [](/windows/desktop/OpenGL/glbegin)un / par de [**glEnd**](/windows/desktop/OpenGL/glend) de glBegin se marca como el inicio de un límite o de un borde no enlazado. Si la marca de borde actual es **true** cuando se especifica el vértice, el vértice se marca como el inicio de un borde del límite. Si la marca de borde actual es **false**, el vértice se marca como el inicio de un borde no enlazado. La función **glEdgeFlagv** establece la marca perimetral en **true** si la marca es distinto de cero; de lo contrario, devuelve **false** .

Los vértices de los triángulos conectados y los quadrilaterals conectados siempre se marcan como límites, independientemente del valor de la marca de borde.

Los límites de límite y no límite en los vértices solo son significativos si el modo de polígono de contabilidad \_ \_ está establecido en el punto de contabilidad o en la \_ línea de contabilidad \_ . Vea [**glPolygonMode**](/windows/desktop/OpenGL/glpolygonmode).

Inicialmente, el bit de marca perimetral es **true**.

La marca perimetral actual se puede actualizar en cualquier momento. En concreto, se puede llamar a **glEdgeFlagv** entre una llamada a [**glBegin**](/windows/desktop/OpenGL/glbegin) y la llamada correspondiente a [**glEnd**](/windows/desktop/OpenGL/glend).

Las siguientes funciones recuperan información relacionada con **glEdgeFlagv**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con marcador de contabilidad de margen de argumento \_ \_

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

