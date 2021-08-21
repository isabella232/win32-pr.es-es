---
description: Función de devolución de llamada para la simulación y compresión de transferencia de radiancia precalutadas (PRT).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81e510808dd2e14af1de0d9618591d8ea3b8587bb4015e72a3e01fa33157b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799338"
---
# <a name="lpd3dxshprtsimcb"></a>LPD3DXSHPRTSIMCB

Función de devolución de llamada para la simulación y compresión de transferencia de radiancia precalutadas (PRT).

## <a name="syntax"></a>Sintaxis


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parámetros

fPercentDone: número de punto flotante entre 0 y 1,0 que representa el porcentaje de cálculos completados (entre 0 y 100 por ciento).

lpUserContext: puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

## <a name="return-value"></a>Valor devuelto

Esta función debe implementarse para devolver S \_ OK para seguir ejecutando el simulador. Cualquier otro valor detendrá el simulador.

## <a name="remarks"></a>Comentarios

Asegúrese de especificar la convención de llamada [**Windows de llamada**](../winprog/windows-data-types.md) de tipos de datos al declarar la función de devolución de llamada. De lo contrario, pueden producirse desbordamientos de pila.



| Requisito                         | Value            |
|--------------------------|-------------|
| Encabezado                   | d3dx9mesh.h |
| Biblioteca de importación           | d3dx9.lib   |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de devolución de llamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
