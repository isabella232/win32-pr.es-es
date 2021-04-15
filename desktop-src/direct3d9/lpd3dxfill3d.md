---
description: Tipo de función que usan las funciones de relleno de textura.
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97342895cb119a786aa71626aeea6d93650c6dc8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495293"
---
# <a name="lpd3dxfill3d"></a>LPD3DXFILL3D

Tipo de función que usan las funciones de relleno de textura.

## <a name="syntax"></a>Sintaxis


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a>Parámetros

pOut: puntero a un vector, que la función utiliza para devolver el resultado. X, Y, Z y W se asignarán a R, G, B y A, respectivamente.

pTexCoord: puntero a un vector que contiene las coordenadas de la textura que se está evaluando actualmente. Los componentes de coordenada de textura para texturas y texturas de volumen van de 0 a 1. Los componentes de coordenadas de textura para las texturas del cubo van de-1 a 1.

pTexelSize: puntero a un vector que contiene las dimensiones de la textura actual.

pData: puntero a los datos de usuario.

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Asegúrese de especificar la Convención de llamada de [**tipos de datos de Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada. De lo contrario, pueden producirse desbordamientos de pila.



|                          |            |
|--------------------------|------------|
| Encabezado                   | d3dx9tex. h |
| Biblioteca de importación           | d3dx9. lib  |
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de devolución de llamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[LPD3DXFILL2D](lpd3dxfill2d.md)
</dt> </dl>

 

 
