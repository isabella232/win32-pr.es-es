---
description: Función de devolución de llamada para la simulación y compresión de transferencia de radiancia precalutadas (PRT).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a7c4911bf2a7b7fa2aa83422a206644f6eb747
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342810"
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

fPercentDone: número de punto flotante entre 0 y 1,0 que representa el porcentaje de cálculos completados (entre el 0 y el 100 %).

lpUserContext: puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

## <a name="return-value"></a>Valor devuelto

Esta función debe implementarse para devolver S \_ OK para seguir ejecutando el simulador. Cualquier otro valor detendrá el simulador.

## <a name="remarks"></a>Comentarios

Asegúrese de especificar la convención de llamada de tipos de datos de [**Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada. De lo contrario, pueden producirse desbordamientos de pila.



| Requisito                         | Value            |
|--------------------------|-------------|
| Encabezado                   | d3dx9mesh.h |
| Biblioteca de importación           | d3dx9.lib   |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de devolución de llamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
