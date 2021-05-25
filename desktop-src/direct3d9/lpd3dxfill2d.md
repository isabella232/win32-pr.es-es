---
description: 'LPD3DXFILL2D: tipo de función que usan las funciones de relleno de textura.'
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c341ccfcbcc566d65e7139813c676e2286e25cf
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342850"
---
# <a name="lpd3dxfill2d"></a>LPD3DXFILL2D

Tipo de función utilizado por las funciones de relleno de textura.

## <a name="syntax"></a>Sintaxis


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a>Parámetros

pOut: puntero a un vector, que la función usa para devolver su resultado. X, Y, Z y W se asignarán a R, G, B y A, respectivamente.

pTexCoord: puntero a un vector que contiene las coordenadas del texel que se está evaluando actualmente. Los componentes de coordenadas de textura para texturas y texturas de volumen oscilan entre 0 y 1. Los componentes de coordenadas de textura para texturas de cubo oscilan entre -1 y 1.

pTexelSize: puntero a un vector que contiene las dimensiones del texel actual.

pData: puntero a los datos de usuario.

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Asegúrese de especificar la convención de llamada tipos de datos de [**Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada. De lo contrario, pueden producirse desbordamientos de pila.



| Requisito                         | Value           |
|--------------------------|------------|
| Encabezado                   | d3dx9tex.h |
| Biblioteca de importación           | d3dx9.lib  |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de devolución de llamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[LPD3DXFILL3D](lpd3dxfill3d.md)
</dt> </dl>

 

 
