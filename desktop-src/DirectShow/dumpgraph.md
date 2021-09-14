---
description: La función DumpGraph envía información sobre un gráfico de filtro a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.
ms.assetid: c78f86bb-44d0-4904-b7f8-e756bda0151d
title: Función DumpGraph (Wxdebug.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DumpGraph
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55c3adf793982b7b00ab44e26e7c34e08a1ac42b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246621"
---
# <a name="dumpgraph-function"></a>Función DumpGraph

La `DumpGraph` función envía información sobre un gráfico de filtros a la ubicación de salida de depuración. Se omite en las compilaciones comerciales.

## <a name="syntax"></a>Sintaxis


```C++
void DumpGraph(
   IFilterGraph *pGraph,
   DWORD        dwLevel
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pgraph* 
</dt> <dd>

Puntero a la [**interfaz IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) en el administrador de gráficos de filtros.

</dd> <dt>

*dwLevel* 
</dt> <dd>

Nivel de registro. La función genera un mensaje LOG \_ TRACE con el nivel de registro especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Wxdebug.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de salida de depuración](debug-output-functions.md)
</dt> </dl>

 

 




