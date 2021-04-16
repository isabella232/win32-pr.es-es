---
description: Función de devolución de llamada para simulación y compresión precalculadas de Radiance Transfer (PRT).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895d6fd3a7d9f93e858c08d1aaae416f1bf3abad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495317"
---
# <a name="lpd3dxshprtsimcb"></a>LPD3DXSHPRTSIMCB

Función de devolución de llamada para simulación y compresión precalculadas de Radiance Transfer (PRT).

## <a name="syntax"></a>Sintaxis


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parámetros

fPercentDone: número de punto flotante entre 0 y 1,0 que representa el porcentaje de cálculos completados (entre 0 y 100 por ciento).

lpUserContext: puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada. lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

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

 

 
