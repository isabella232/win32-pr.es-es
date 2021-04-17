---
description: Función de devolución de llamada para UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda7c58ef001a936b01f3af2027f9207c3d2770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714731"
---
# <a name="lpd3dxuvatlascb"></a>LPD3DXUVATLASCB

Función de devolución de llamada para UVAtlas.

## <a name="syntax"></a>Sintaxis


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parámetros

\[out \] fPercentDone: número de punto flotante entre 0 y 1,0 que representa el porcentaje de cálculos completados (entre 0 y 100 por ciento).

\[en \] lpUserContext: puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; normalmente se usa en una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

## <a name="return-value"></a>Valor devuelto

Esta función se debe implementar para que se devuelvan \_ los elementos correctos para seguir ejecutando el simulador. Cualquier otro valor detendrá el simulador.

## <a name="remarks"></a>Observaciones

Asegúrese de especificar la Convención de llamada de [**tipos de datos de Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada. De lo contrario, pueden producirse desbordamientos de pila.



|                          |             |
|--------------------------|-------------|
| Encabezado                   | d3dx9mesh. h |
| Biblioteca de importación           | d3dx9. lib   |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de devolución de llamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
