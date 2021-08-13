---
description: Función de devolución de llamada para UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4473134d7ecf98c50d0c3a69085e7f46344d1d57ff2650c1adbc54c43dba266
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119458724"
---
# <a name="lpd3dxuvatlascb"></a>LPD3DVATLASCB

Función de devolución de llamada para UVAtlas.

## <a name="syntax"></a>Sintaxis


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parámetros

\[out fPercentDone: número de punto flotante entre 0 y 1,0 que representa el porcentaje de \] cálculos completados (entre 0 y 100 por ciento).

\[en lpUserContext: puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada; normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de \] llamada.

## <a name="return-value"></a>Valor devuelto

Esta función debe implementarse para devolver S \_ OK para seguir ejecutando el simulador. Cualquier otro valor detendrá el simulador.

## <a name="remarks"></a>Observaciones

Asegúrese de especificar la convención de llamada [**Windows tipos**](../winprog/windows-data-types.md) de datos al declarar la función de devolución de llamada. De lo contrario, pueden producirse desbordamientos de pila.



| Requisito                         | Value            |
|--------------------------|-------------|
| Encabezado                   | d3dx9mesh.h |
| Biblioteca de importación           | d3dx9.lib   |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de devolución de llamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
