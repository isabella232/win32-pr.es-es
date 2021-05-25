---
description: Función de devolución de llamada para UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3D LPVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe073b5e6a798ccb74421d42502b089d59be11f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342800"
---
# <a name="lpd3dxuvatlascb"></a>LPD3D LPVATLASCB

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

## <a name="remarks"></a>Comentarios

Asegúrese de especificar la convención de llamada tipos de datos de [**Windows**](../winprog/windows-data-types.md) al declarar la función de devolución de llamada. De lo contrario, pueden producirse desbordamientos de pila.



| Requisito                         | Value            |
|--------------------------|-------------|
| Encabezado                   | d3dx9mesh.h |
| Biblioteca de importación           | d3dx9.lib   |
| Sistema operativo mínimo | Windows 98  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de devolución de llamada](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
